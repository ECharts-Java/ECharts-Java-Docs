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
List<Number[]> punchcard = new ArrayList<>();
for (JsonElement item : data.get("data").getAsJsonArray()) {
    int item0 = item.getAsJsonArray().get(0).getAsInt();
    int item1 = item.getAsJsonArray().get(1).getAsInt();
    int item2 = item.getAsJsonArray().get(2).getAsInt();
    punchcard.add(new Number[] { item1, item0, item2 == 0 ? null : item2 });
}
```

```java
Heatmap heatmap = new Heatmap()
        .addXAxis(hours.toArray(new String[0]))
        .addYAxis(days.toArray(new String[0]))
        .setVisualMap(0, 10)
        .addSeries(new HeatmapSeries().setName("Punch Card")
                .setData(punchcard.toArray())
                .setLabel(new SeriesLabel().setShow(true)));
```
