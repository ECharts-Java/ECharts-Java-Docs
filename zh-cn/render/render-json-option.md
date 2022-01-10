# engine.renderJsonOption()

### 概览
`renderJsonOption()`会返回一个JSON格式的，表示Option对象的字符串。该方法可以在服务器端渲染(SSR)或者前后端分离APP的RESTful APIs中广泛使用。我们的示例仓库里包括对应的[SSR示例项目](zh-cn/spring-boot/sb-template)和[RESTful APIs项目](zh-cn/spring-boot/sb-restful)。

```java
// renderJsonOption supports a parameter of Chart or Option
public String renderJsonOption(Chart<?, ?> chart)

public String renderJsonOption(Option option)
```


### Q&A
Q: 能否不用`renderJsonOption()`而直接返回Option对象？

A: 为了返回结果的简便性，我们推荐使用`renderJsonOption()`。如果直接返回Option对象，该Option对象的所有属性均会被展开，不论是否为`null`。

比如，
E.g. 
```json
{
  "animation": null,
  "animationThreshold": null,
  "animationDuration": null,
  ...
  "series": [
    {
      "mainType": null,
      "type": "line",
      "id": null,
      "name": null,
      "z": null,
      "cursor": null,
      "dataGroupId": null,
      "data": [820, 932, 901, 934, 1290, 1330, 1320],
      ...
    }
  ],
  "xaxis": [
    {
      "gridIndex": null,
      "gridId": null,
      "position": null,
      "offset": null,
      "categorySortInfo": null,
      "mainType": null,
      "type": "category",
      "id": null,
      ...
    }
  ],
  "yaxis": [
    {
      "gridIndex": null,
      "gridId": null,
      "position": null,
      "offset": null,
      "categorySortInfo": null,
      ...
    }
  ]
}

```

`renderJsonOption()`会把为null的属性消去，返回如下的JSON字符串。
```json
{
  "xAxis": [
    {
      "type": "category",
      "data": ["Mon", "Tue", "Wed", "Thu", "Fri", "Sat", "Sun"],
      "boundaryGap": false
    }
  ],
  "yAxis": [{ "type": "value" }],
  "series": [
    {
      "type": "line",
      "data": [820, 932, 901, 934, 1290, 1330, 1320],
      "areaStyle": {}
    }
  ]
}

```

