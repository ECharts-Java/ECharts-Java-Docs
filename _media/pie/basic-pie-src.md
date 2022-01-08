```java
Pie pie = new Pie()
        .setTitle("Basic Pie")
        .setTooltip("item")
        .setLegend()
        .addSeries(new PieDataItem[] {
                new PieDataItem().setValue(1048).setName("Search Engine"),
                new PieDataItem().setValue(735).setName("Direct"),
                new PieDataItem().setValue(580).setName("Email"),
                new PieDataItem().setValue(484).setName("Union Ads"),
                new PieDataItem().setValue(300).setName("Video Ads")
        });
```
