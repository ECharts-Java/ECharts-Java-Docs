```java
// data is a JsonObject from https://raw.githubusercontent.com/IcePear-Jzx/ECharts-Java/master/src/test/resources/mock/punch-card.json
List<String> hours = new ArrayList<>();
for (JsonElement hour : data.get("hours").getAsJsonArray()) {
    hours.add(hour.getAsString());
}
List<String> days = new ArrayList<>();
for (JsonElement day : data.get("days").getAsJsonArray()) {
    days.add(day.getAsString());
}
List<ScatterDataItem> items = new ArrayList<>();
for (JsonElement item : data.get("data").getAsJsonArray()) {
    int item0 = item.getAsJsonArray().get(0).getAsInt();
    int item1 = item.getAsJsonArray().get(1).getAsInt();
    int item2 = item.getAsJsonArray().get(2).getAsInt();
    items.add(new ScatterDataItem().setValue(new Number[] { item0, item1, item2 }).setSymbolSize(item2 * 2));
}
```

```java
PolarScatter polarScatter = new PolarScatter()
        .setLegend(true)
        .setTooltip("item")
        .setPolarAxis()
        .setAngleAxis(new CategoryAngleAxis()
                .setData(hours.toArray())
                .setBoundaryGap(false)
                .setSplitLine(new SplitLine().setShow(true))
                .setAxisLine(new AxisLine().setShow(false)))
        .setRadiusAxis(new CategoryRadiusAxis()
                .setData(days.toArray())
                .setAxisLine(new AxisLine().setShow(false))
                .setAxisLabel(new CategoryAxisLabel().setRotate(45)))
        .addSeries(items.toArray());
```
