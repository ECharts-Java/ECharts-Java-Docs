# Spring Boot - 模板渲染

?> 本节文档将介绍如何在Spring Boot应用中集成ECharts Java用于模板渲染。

ECharts Java使用Handlebars.java作为内置的模板引擎，用以生成HTML页面。在Spring Boot应用中，你可以使用各种不同的模板引擎，如[HandleBars](https://github.com/jknack/handlebars.java), [Thymeleaf](https://www.thymeleaf.org/), [Apache Velocity](https://velocity.apache.org/)。

在自定义模板中使用ECharts Java至少有两种方式。

1. 在HTML模板中使用`iframe`。因为`iframe`会额外发送一个HTTP请求，所以后端的Controller需要对该请求做出响应，即用`renderHtml`返回完整的HTML。
2. 在模板中import ECharts，调用相应的init方法。并且使用ECharts Java构建和返回Option对象。

下面的例子将以HandleBars为例，展示如何在Maven项目使用模板引擎和ECharts来生成自定义的页面内容。你也可以参考我们的[示例仓库](https://github.com/incandescentxxc/ECharts-Java-Examples/tree/main/template-demo).

### Step 0: 初始化

1. [**初始化Spring Boot应用**](https://spring.io/guides/gs/spring-boot/#scratch)

2. [**安装ECharts Java依赖**](https://search.maven.org/artifact/org.icepear.echarts/echarts-java/1.0.3/jar)

Maven项目请将如下代码复制粘贴至pom.xml。
```
<dependency>
  <groupId>org.icepear.echarts</groupId>
  <artifactId>echarts-java</artifactId>
  <version>1.0.3</version>
</dependency>
```

3. [**Install Handlebars Dependency**](https://mvnrepository.com/artifact/com.github.jknack/handlebars)

在pom.xml中添加如下代码。
```
<dependency>
    <groupId>com.github.jknack</groupId>
    <artifactId>handlebars</artifactId>
    <version>4.2.1</version>
</dependency>
```

After the initialization, the project directory will look like this,
初始化之后，你的项目结构应该大概如下
```
├── HELP.md
├── mvnw
├── mvnw.cmd
├── pom.xml
└── src
    ├── main
    │   ├── java
    │   │   └── org
    │   │       └── icepear
    │   │           └── echarts
    │   │               └── example
    │   │                   └── springboot
    │   │                       └── templatedemo
    │   │                           └── TemplateDemoApplication.java
    │   └── resources
    │       ├── application.properties
    │       ├── static
    │       └── templates
    └── test
```
### Step 1: 创建你的模板

下面先展示用以上提到的`iframe`方法。

在`src/main/resources/templates`中添加如下模板文件，例如，`index1.hbs`。
```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ECharts-Java Demo</title>
</head>

<body>
    <h1>Welcome to {{ this }}</h1>
    {{!-- method 1: using iframe --}}
    <iframe id="c_iframe" height="600px" width="600px" frameborder="no" scrolling="no" src="linechart"></iframe>
</body>

</html>
```
注意，在该方法中，我们使用`iframe`来引用EChart图表，该`iframe`会按照其src属性标注的地址，向该地址发送请求。所以，后端需要对该请求做出应答。

第二种方法是使用Option，例如你可以在`src/main/resources/templates`中添加如下模板文件，例如，`index2.hbs`。
```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <script src="https://cdnjs.cloudflare.com/ajax/libs/echarts/5.2.2/echarts.min.js"
        integrity="sha512-ivdGNkeO+FTZH5ZoVC4gS4ovGSiWc+6v60/hvHkccaMN2BXchfKdvEZtviy5L4xSpF8NPsfS0EVNSGf+EsUdxA=="
        crossorigin="anonymous" referrerpolicy="no-referrer"></script>
    <title>ECharts-Java Demo</title>
</head>

<body>
    <h1>Welcome to ECharts Java</h1>

    {{!-- method 2: using Option object--}}
    <div id="display-container" style="height: 600px; width: 600px"></div>
    </div>
    <script>
        let chart = echarts.init(document.getElementById("display-container"));
        let option = {{{ this }}}
        chart.setOption(option);
    </script>
</body>

</html>
```


### Step 2: 添加controller

下面，我们将在`src/main/java/org/icepear/echarts/example/springboot/templatedemo/`目录下添加controller类。

如之前提到的，`iframe`方法中，你需要创建一个函数，用来返回`iframe`请求的完整HTML。
```java
@RestController
public class Controller {
    
    @GetMapping("/")
    public String index(){
        Handlebars handlebars = new Handlebars();
        String html = "";
        try {
            Template template = handlebars.compile("templates/index1");
            html = template.apply("ECharts Java");
        } catch (IOException e) {
            System.out.println("template file not found");
        }
        return html;
    }

    @GetMapping("/linechart")
    public ResponseEntity<String> getChart() {
        Line line = new Line()
                .addXAxis(new CategoryAxis()
                        .setData(new String[] { "Mon", "Tue", "Wed", "Thu", "Fri", "Sat", "Sun" })
                        .setBoundaryGap(false))
                .addYAxis()
                .addSeries(new LineSeries()
                        .setData(new Number[] { 820, 932, 901, 934, 1290, 1330, 1320 })
                        .setAreaStyle(new LineAreaStyle()));
        Engine engine = new Engine();
        // return the full html of the echarts, used in iframes in your own template
        String json = engine.renderHtml(line);
        return ResponseEntity.ok(json);
    }
}
```

如果你使用的是Option方法，可以添加如下代码。
```java
@RestController
public class ControllerMethod2 {
    // The GetMapping is to differiate with the first method
    @GetMapping("/option")
    public String index() {
        Line lineChart = new Line()
                .addXAxis(new CategoryAxis()
                        .setData(new String[] { "Mon", "Tue", "Wed", "Thu", "Fri", "Sat", "Sun" })
                        .setBoundaryGap(false))
                .addYAxis()
                .addSeries(new LineSeries()
                        .setData(new Number[] { 820, 932, 901, 934, 1290, 1330, 1320 })
                        .setAreaStyle(new LineAreaStyle()));
        Engine engine = new Engine();
        Handlebars handlebars = new Handlebars();
        String html = "";
        try {
            Template template = handlebars.compile("templates/index2");
            html = template.apply(engine.renderJsonOption(lineChart));
        } catch (IOException e) {
            System.out.println("template file not found");
        }
        return html;
    }
}

```

### Step 3: 运行应用

在terminal中输入 `./mvnw spring-boot:run `

如果想查看本示例的方法二，在浏览器地址栏中输入localhost:8080/option

你看到的结果将和下图相似。

[basic-area-html](../../_media/line/basic-area.html ':include :type=iframe')
