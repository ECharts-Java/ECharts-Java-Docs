```java
Bar bar = new Bar()
        .addXAxis(new String[] { "Mon", "Tue", "Wed", "Thu", "Fri", "Sat", "Sun" })
        .addYAxis()
        .addSeries(new BarSeries().setData(new BarDataItem[] {
                new BarDataItem().setValue(120),
                new BarDataItem().setValue(200).setItemStyle(new BarItemStyle().setColor("#a90000")),
                new BarDataItem().setValue(150),
                new BarDataItem().setValue(80),
                new BarDataItem().setValue(70),
                new BarDataItem().setValue(110),
                new BarDataItem().setValue(130)
        }));
```
