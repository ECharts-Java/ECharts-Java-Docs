# engine.render()

### 概览

`render()`能够将用户创建的图表以HTML格式渲染至本地。`render()`接收两个参数，分别是path（HTML存储的本地路径）和Chart对象。ECharts Java内置Handlebar.java为模板引擎，用以生成HTML。


```java
// path parameter specifies the path to save the generated HTML file
public void render(String path, Chart<?, ?> chart)
```

### 支持下载图片

`render()`生成的HTML文件内含下载图片的链接。用户在浏览器中打开该HTML文件后，可以点击相应按钮下载图片为PNG格式。

<img src="../../_media/imgs/multibar-render.gif" alt="multi-bar-render" style="width:50%;" />

### 支持Chart和Option对象

用户可以自由选择绘图方式：既可以选择ECharts Java重新设计的绘图API，也可以选择构建Option对象来作图。`render()`方法支持Chart和Option对象。


```java
// render from Chart
public void render(String path, Chart<?, ?> chart)

// render from Option
public void render(String path, Option option) 
```

### 支持自定义宽高和自动打开HTML文件

`render()`也接收额外参数来控制生成图表的宽高。另外，`render()`也支持willOpen参数，用以控制是否自动在浏览器中打开生成的HTML。为了方便，如果你需要频繁调整一个图表，我们推荐将willOpen设为`True`。

```java
// height and width support a String ends with "px" or "%"
// e.g. "600px", "60%"
public void render(String path, Chart<?, ?> chart, String height, String width, Boolean willOpen)

public void render(String path, Option option, String height, String width, Boolean willOpen)
```