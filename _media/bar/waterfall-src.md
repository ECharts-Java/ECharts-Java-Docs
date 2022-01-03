```java
Bar bar = new Bar()
        .setTitle("Waterfall")
        .addXAxis(new String[] { "Total", "Rent", "Utilities", "Transportation", "Meals", "Other" })
        .addYAxis()
        .addSeries(new BarSeries().setName("Placeholder").setStack("Total")
                .setItemStyle(new BarItemStyle().setBorderColor("transparent").setColor("transparent"))
                .setData(new Number[] { 0, 1700, 1400, 1200, 300, 0 }))
        .addSeries(new BarSeries().setName("Life Cost").setStack("Total")
                .setLabel(new BarSeriesLabel().setShow(true).setPosition("inside"))
                .setData(new Number[] { 2900, 1200, 300, 200, 900, 300 }));
```
