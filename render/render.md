# engine.render()

### Overview

`render()` method is used to render a chart into a local HTML file, provided with path and chart object. In ECharts Java, we use Handlebars.java as our template engine to generate these HTML files.

```java
// path parameter specifies the path to save the generated HTML file
public void render(String path, Chart<?, ?> chart)
```

### Download images supported

Users can use `render()` method to generate HTML and open it in the browser to actually see their charts. Moreover, our rendered HTML also supports downloading function. Users can save their charts into images in PNG formats.

<img src="_media/imgs/multibar-render.gif" alt="multi-bar-render" style="width:50%;" />


### Rendering from both Chart object and Option object

In ECharts Java, users can choose to use our simplified APIs to make a plot, or advanced APIs to construct an Option object. In either way, you can render them into HTML through `render()`. 

```java
// render from Chart
public void render(String path, Chart<?, ?> chart)

// render from Option
public void render(String path, Option option) 
```

### Rendering with customized height, weight, and willOpen options

`render()` also supports the parameters to specify the height, weight, and willOpen options of the chart. willOpen refers to whether to allow ECharts Java to open the generated HTML file in your default browser once it has been rendered. It is recommended to set it to `True` when you are adjusting the visual effects of a particular chart because of convenience.

```java
// height and width support a String ends with "px" or "%"
// e.g. "600px", "60%"
public void render(String path, Chart<?, ?> chart, String height, String width, Boolean willOpen)

public void render(String path, Option option, String height, String width, Boolean willOpen)
```