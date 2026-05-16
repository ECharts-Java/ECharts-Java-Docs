```java
PictorialBar chart = new PictorialBar()
        .addXAxis(new String[] { "Mon", "Tue", "Wed", "Thu", "Fri" })
        .addYAxis()
        .addSeries(new PictorialBarSeries()
                .setSymbol("circle")
                .setSymbolRepeat(true)
                .setSymbolSize(new Number[] { 16, 16 })
                .setSymbolMargin("10%")
                .setData(new Number[] { 8000, 9500, 12000, 11000, 15000 }));
```
