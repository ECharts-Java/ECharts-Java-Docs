# Spring Boot
?> This tutorial introduces how to use Echarts-Java in a Spring-boot Application

## Template Rendering
Echarts-Java uses Handlebars.java as a built-in template engine, which helps to render the html page. In a Spring Boot Application, you can write your own template with various template engines, and includes the returned html in your template using iframes. The following example will show how to use HandleBars template engine to generate customized content with Echarts-Java.

### Step 0: Initialization
1. [**initialize a spring boot application**](https://spring.io/guides/gs/spring-boot/#scratch)

2. [**install Echarts-Java Dependency**]()
```
<dependency>
    TODO
</dependency>
```

3. [**Install Handlebars Dependency**](https://mvnrepository.com/artifact/com.github.jknack/handlebars)
```
<dependency>
    <groupId>com.github.jknack</groupId>
    <artifactId>handlebars</artifactId>
    <version>4.2.1</version>
</dependency>
```

### Step 1: Write your templates
Add a template file in `src/main/resources/templates`, for example `index.hbs` as follows:
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
    <iframe id="c_iframe" height="600px" width="600px" frameborder="no" scrolling="no" src="linechart"></iframe>
</body>
</html>
```
Noted that we use iframe to reference an echart, whose request (as src indicates) should be satisfied by a function in controller with a corresponding GetMapping.


### Step 2: Add the controller
Add a controller class. In the controller, specify one function to return the full html of homepage, and at least one function to render the echart, whose name should correspond to the iframe src in your template.

```java
@RestController
public class Controller {
    
    @GetMapping("/")
    public String index(){
        Handlebars handlebars = new Handlebars();
        String html = "";
        try {
            Template template = handlebars.compile("templates/index");
            html = template.apply("Echarts-Java");
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
                        .setAreaStyle(new AreaStyle()));
        Engine engine = new Engine();
        // return the full html of the echarts, used in iframes in your own template
        String json = engine.renderHtml(line);
        return ResponseEntity.ok(json);
    }
}
```

### Step 3: Run the application
run `./mvnw spring-boot:run ` in the terminal

images to add here TODO


## Restful APIs
TODO