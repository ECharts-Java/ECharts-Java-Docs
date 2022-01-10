```java
Pie pie = new Pie()
        .setTooltip("item")
        .setLegend()
        .addSeries(new PieSeries().setRadius(new String[] { "40%", "70%" })
                .setItemStyle(new PieItemStyle()
                        .setBorderRadius(10)
                        .setBorderColor("#fff")
                        .setBorderWidth(2))
                .setLabel(new PieLabel().setShow(false).setPosition("center"))
                .setEmphasis(new PieEmphasis().setLabel(new PieLabel()
                        .setShow(true).setFontSize(20).setFontWeight("bold")))
                .setData(new PieDataItem[] {
                        new PieDataItem().setValue(1048).setName("Search Engine"),
                        new PieDataItem().setValue(735).setName("Direct"),
                        new PieDataItem().setValue(580).setName("Email"),
                        new PieDataItem().setValue(484).setName("Union Ads"),
                        new PieDataItem().setValue(300).setName("Video Ads")
                }));
```
