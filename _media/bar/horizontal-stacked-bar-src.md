```java
BarSeries createSeries(String name, Object[] data) {
    return new BarSeries().setName(name).setStack("total")
            .setLabel(new BarSeriesLabel().setShow(true))
            .setEmphasis(new BarEmphasis().setFocus("series"))
            .setData(data);
}
```

```java
Bar bar = new Bar()
        .setTooltip(new Tooltip().setTrigger("axis")
                .setAxisPointer(new TooltipAxisPointer().setType("shadow")))
        .setLegend()
        .addXAxis()
        .addYAxis(new String[] { "Mon", "Tue", "Wed", "Thu", "Fri", "Sat", "Sun" })
        .addSeries(createSeries("Direct", new Number[] { 320, 302, 301, 334, 390, 330, 320 }))
        .addSeries(createSeries("Mail Ad", new Number[] { 120, 132, 101, 134, 90, 230, 210 }))
        .addSeries(createSeries("Affiliate Ad", new Number[] { 220, 182, 191, 234, 290, 330, 310 }))
        .addSeries(createSeries("Video Ad", new Number[] { 150, 212, 201, 154, 190, 330, 410 }))
        .addSeries(createSeries("Search Engine", new Number[] { 820, 832, 901, 934, 1290, 1330, 1320 }));
```
