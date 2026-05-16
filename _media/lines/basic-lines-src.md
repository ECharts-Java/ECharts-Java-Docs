```java
LinesDataItem[] data = new LinesDataItem[] {
        new LinesDataItem().setCoords(new Number[][] { { 0, 0 }, { 50, 80 } }),
        new LinesDataItem().setCoords(new Number[][] { { 50, 80 }, { 120, 30 } }),
        new LinesDataItem().setCoords(new Number[][] { { 120, 30 }, { 200, 90 } })
};

Lines chart = new Lines()
        .addSeries(new LinesSeries()
                .setCoordinateSystem("cartesian2d")
                .setPolyline(false)
                .setEffect(new LinesEffect().setShow(true).setSymbol("arrow").setTrailLength(0.7))
                .setData(data));
```
