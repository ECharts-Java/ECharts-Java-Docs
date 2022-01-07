# engine.renderHtml()

### Overview
Unlike `render()`, `renderHtml()` will return the generated HTML as a **String** instead of directly save it in the local directory. The resulted HTML string can be easily used for Server Side Rendering (SSR). Our [example](spring-boot/sb-template) shows how to use and integrate it into a customized template to render user-defined contents.

```java
// No path to specify because it returns the resulted HTML as String
public String renderHtml(Chart<?, ?> chart)
```

### Other Options

`renderHtml()` can also be used through a Chart object or an Option object. Simlar with `render()`, it also supports customized height and width feature.

?> Please note the unit of height and width: they both ends with "px" or "%".

```java
public String renderHtml(Chart<?, ?> chart)

public String renderHtml(Option option)

public String renderHtml(Chart<?, ?> chart, String height, String width)

public String renderHtml(Option option, String height, String width)

```