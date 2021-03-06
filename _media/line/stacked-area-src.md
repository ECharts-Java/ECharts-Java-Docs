```java
LineSeries createSeries(String name, Object[] data) {
    return new LineSeries()
            .setName(name)
            .setStack("Total")
            .setSmooth(true)
            .setLineStyle(new LineStyle().setWidth(0))
            .setShowSymbol(false)
            .setAreaStyle(new LineAreaStyle())
            .setData(data);
}
```

```java
Line line = new Line()
        .setTitle("Stacked Area")
        .setTooltip("axis")
        .setLegend()
        .addXAxis(new CategoryAxis().setBoundaryGap(false)
                .setData(new String[] { "Mon", "Tue", "Wed", "Thu", "Fri", "Sat", "Sun" }))
        .addYAxis()
        .addSeries(createSeries("Line 1", new Number[] { 140, 232, 101, 264, 90, 340, 250 }))
        .addSeries(createSeries("Line 2", new Number[] { 120, 282, 111, 234, 220, 340, 310 }))
        .addSeries(createSeries("Line 3", new Number[] { 320, 132, 201, 334, 190, 130, 220 }))
        .addSeries(createSeries("Line 4", new Number[] { 220, 402, 231, 134, 190, 230, 120 }))
        .addSeries(createSeries("Line 5", new Number[] { 220, 302, 181, 234, 210, 290, 150 }));
```
