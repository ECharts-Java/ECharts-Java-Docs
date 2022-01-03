```java
// data is a JsonObject from https://raw.githubusercontent.com/IcePear-Jzx/ECharts-Java/master/src/test/resources/mock/les-miserables.json
List<GraphNodeItem> nodes = new ArrayList<>();
for (JsonElement node : data.get("nodes").getAsJsonArray()) {
    nodes.add(new GraphNodeItem()
            .setId(node.getAsJsonObject().get("id").getAsString())
            .setName(node.getAsJsonObject().get("name").getAsString())
            .setSymbolSize(node.getAsJsonObject().get("symbolSize").getAsDouble())
            .setValue(node.getAsJsonObject().get("value").getAsDouble())
            .setCategory(node.getAsJsonObject().get("category").getAsInt()));
}
List<GraphEdgeItem> links = new ArrayList<>();
for (JsonElement link : data.get("links").getAsJsonArray()) {
    links.add(new GraphEdgeItem()
            .setSource(link.getAsJsonObject().get("source").getAsString())
            .setTarget(link.getAsJsonObject().get("target").getAsString()));
}
List<GraphCategoryItem> categories = new ArrayList<>();
for (JsonElement category : data.get("categories").getAsJsonArray()) {
    categories.add(new GraphCategoryItem()
            .setName(category.getAsJsonObject().get("name").getAsString()));
}
```

```java
Graph graph = new Graph()
        .setTitle("Les Miserables")
        .setTooltip("item")
        .setLegend(true)
        .addSeries(new GraphSeries().setName("Les Miserables")
                .setLayout("circular")
                .setCircular(new GraphCircular().setRotateLabel(true))
                .setData(nodes.toArray(new GraphNodeItem[0]))
                .setLinks(links.toArray(new GraphEdgeItem[0]))
                .setCategories(categories.toArray(new GraphCategoryItem[0]))
                .setLabel(new SeriesLabel().setShow(true).setPosition("right"))
                .setLineStyle(new GraphEdgeLineStyle().setColor("source").setCurveness(0.3)));
```
