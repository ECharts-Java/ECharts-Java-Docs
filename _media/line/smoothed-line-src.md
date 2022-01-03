```java
Line line = new Line()
        .addXAxis(new String[] { "Mon", "Tue", "Wed", "Thu", "Fri", "Sat", "Sun" })
        .addYAxis()
        .addSeries(new LineSeries()
                .setData(new Number[] { 820, 932, 901, 934, 1290, 1330, 1320 })
                .setSmooth(true));
```
