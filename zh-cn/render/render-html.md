# engine.renderHtml()

### 概览
不像`render()`会将HTML保存到本地，`renderHtml()`会以**字符串**类型返回生成的HTML。生成的HTML字符串可用来进行服务器端渲染（SSR)。我们的[示例仓库](zh-cn/spring-boot/sb-template)展示了如何将ECharts Java集成到自定义的模板来渲染用户定义的内容。

```java
// No path to specify because it returns the resulted HTML as String
public String renderHtml(Chart<?, ?> chart)
```

### 其他选项

和`render()`相似，`renderHtml()`既能接收Chart对象也能接收Option对象，同时也支持自定义图表宽高。

?> 请注意宽高的单位为"px"或者"%"。

```java
public String renderHtml(Chart<?, ?> chart)

public String renderHtml(Option option)

public String renderHtml(Chart<?, ?> chart, String height, String width)

public String renderHtml(Option option, String height, String width)

```