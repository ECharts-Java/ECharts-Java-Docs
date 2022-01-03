```java
Graph graph = new Graph()
        .addSeries(new GraphSeries().setSymbolSize(50)
                .setLabel(new SeriesLabel().setShow(true))
                .setEdgeSymbol(new String[] { "circle", "arrow" })
                .setData(new GraphNodeItem[] {
                        new GraphNodeItem().setName("Node 1").setX(300).setY(300),
                        new GraphNodeItem().setName("Node 2").setX(800).setY(300),
                        new GraphNodeItem().setName("Node 3").setX(550).setY(100),
                        new GraphNodeItem().setName("Node 4").setX(550).setY(500)
                })
                .setLinks(new GraphEdgeItem[] {
                        new GraphEdgeItem().setSource("Node 1").setTarget("Node 2")
                                .setLineStyle(new GraphEdgeLineStyle().setCurveness(0.2)),
                        new GraphEdgeItem().setSource("Node 2").setTarget("Node 1")
                                .setLineStyle(new GraphEdgeLineStyle().setCurveness(0.2)),
                        new GraphEdgeItem().setSource("Node 1").setTarget("Node 3"),
                        new GraphEdgeItem().setSource("Node 2").setTarget("Node 3"),
                        new GraphEdgeItem().setSource("Node 2").setTarget("Node 4"),
                        new GraphEdgeItem().setSource("Node 1").setTarget("Node 4")
                })
                .setLineStyle(new GraphEdgeLineStyle().setOpacity(0.9).setWidth(2).setCurveness(0)));
```
