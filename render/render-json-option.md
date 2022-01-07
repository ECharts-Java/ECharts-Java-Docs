# engine.renderJsonOption()

### Overview
`renderJsonOption()` may be one of the most popular API in ECharts Java, if not the most. `renderJsonOption()` will return a string, which represents an Option object in JSON format. This can be broadly used in SSR or RESTful APIs. We provide corresponding examples [SSR](spring-boot/sb-template) and [RESTful APIs](spring-boot/sb-restful).

```java
// renderJsonOption supports a parameter of Chart or Option
public String renderJsonOption(Chart<?, ?> chart)

public String renderJsonOption(Option option)
```

### Q&A
Q: Can I directly return an Option object instead of use renderJsonOption?

A: we don't recommend you to do that because of simplicity. If you directly return an Option object, it will show all fields, the majority of which are `null`. 

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

`renderJsonOption()` will eliminate those unnecessary fields and return the object as follows,

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


