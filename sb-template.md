# Spring Boot - Template Rendering

?> This tutorial introduces how to use ECharts Java in a Spring Boot Application through a template rendering method.

ECharts Java uses Handlebars.java as a built-in template engine, which helps to render the html page. In a Spring Boot Application, you can write your own template with various template engines. To use ECharts Java in your templates, there are at least two ways.

1. Use `iframes` to make a sperate request in your template, and return the full html using `renderHtml` method in ECharts Java.
2. Import Echarts in your own templates, and use ECharts Java to write the Option object that is used in the Echart functions in Javascript.

The following example will show how to use **HandleBars** template engine to generate customized content with ECharts Java in the above two approaches.

The example repo can be found [here](https://github.com/incandescentxxc/ECharts-Java-Examples/tree/main/template-demo).

### Step 0: Initialization

1. [**Initialize a Spring Boot Application**](https://spring.io/guides/gs/spring-boot/#scratch)

2. [**Install ECharts Java Dependency**]()

Add below dependency in your pom.xml.
```
<dependency>
    TODO
</dependency>
```

3. [**Install Handlebars Dependency**](https://mvnrepository.com/artifact/com.github.jknack/handlebars)

Add below dependency in your pom.xml.
```
<dependency>
    <groupId>com.github.jknack</groupId>
    <artifactId>handlebars</artifactId>
    <version>4.2.1</version>
</dependency>
```

After the initialization, the project directory will look like this,
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

### Step 1: Write your templates

Add a template file in `src/main/resources/templates`, for example `index1.hbs` as follows:
```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Echarts-Java Demo</title>
</head>

<body>
    <h1>Welcome to {{ this }}</h1>
    {{!-- method 1: using iframe --}}
    <iframe id="c_iframe" height="600px" width="600px" frameborder="no" scrolling="no" src="linechart"></iframe>
</body>

</html>
```
Noted that in method 1, we use iframe to reference an echart, whose request (as src indicates) should be satisfied by a function in controller with a corresponding GetMapping.

If you want to use the Option object, you can add a template like below, e.g. `index2.hbs`:
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
    <title>Echarts-Java Demo</title>
</head>

<body>
    <h1>Welcome to Echarts Java</h1>

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


### Step 2: Add the controller

Add a controller class. 

If you want to use `iframes`, in the controller, specify one function to return the full html of homepage, and at least one function to render the echart, whose name should correspond to the iframe src in your template.

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

If you prefer to use Option object directly, turn to the second method as follows,

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

### Step 3: Run the application

run `./mvnw spring-boot:run ` in the terminal. To see the results of the second method, enter localhost:8080/option in the url field of the browser.

The output will look like the following,

[basic-area-html](../media/line/basic-area.html ':include :type=iframe')




