```java
Number[][] data = new Number[361][2];
for (int i = 0; i <= 360; i++) {
    Double t = (i / 180.0) * Math.PI;
    Double r = Math.sin(2 * t) * Math.cos(2 * t);
    data[i][0] = r;
    data[i][1] = i;
}
```

```java
PolarLine polarLine = new PolarLine()
        .setTooltip(new Tooltip().setType("axis")
                .setAxisPointer(new TooltipAxisPointer().setType("cross")))
        .setPolarAxis()
        .setAngleAxis()
        .setRadiusAxis(new DefaultRadiusAxis().setMin(0))
        .addSeries(new LineSeries().setCoordinateSystem("polar")
                .setShowSymbol(false).setData(data));
```
