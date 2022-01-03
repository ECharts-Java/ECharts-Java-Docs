```java
Pie pie = new Pie()
        .setLegend(true)
        .addSeries(new PieSeries()
                .setRadius(new Number[] { 20, 150 })
                .setRoseType("area")
                .setItemStyle(new PieItemStyle().setBorderRadius(8))
                .setData(new PieDataItem[] {
                        new PieDataItem().setValue(40).setName("rose 1"),
                        new PieDataItem().setValue(38).setName("rose 2"),
                        new PieDataItem().setValue(32).setName("rose 3"),
                        new PieDataItem().setValue(30).setName("rose 4"),
                        new PieDataItem().setValue(28).setName("rose 5"),
                        new PieDataItem().setValue(26).setName("rose 6"),
                        new PieDataItem().setValue(22).setName("rose 7"),
                        new PieDataItem().setValue(18).setName("rose 8")
                }));
```
