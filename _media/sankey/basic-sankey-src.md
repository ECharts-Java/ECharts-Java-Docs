```java
Sankey sankey = new Sankey()
        .addSeries(new SankeySeries()
                .setEmphasis(new SankeyEmphasis().setFocus("adjacency"))
                .setData(new SankeyNodeItem[] {
                        new SankeyNodeItem().setName("a"),
                        new SankeyNodeItem().setName("b"),
                        new SankeyNodeItem().setName("a1"),
                        new SankeyNodeItem().setName("a2"),
                        new SankeyNodeItem().setName("b1"),
                        new SankeyNodeItem().setName("c")
                })
                .setLinks(new SankeyEdgeItem[] {
                        new SankeyEdgeItem().setSource("a").setTarget("a1").setValue(5),
                        new SankeyEdgeItem().setSource("a").setTarget("a2").setValue(3),
                        new SankeyEdgeItem().setSource("b").setTarget("b1").setValue(8),
                        new SankeyEdgeItem().setSource("a").setTarget("b1").setValue(3),
                        new SankeyEdgeItem().setSource("b1").setTarget("a1").setValue(1),
                        new SankeyEdgeItem().setSource("b1").setTarget("c").setValue(2)
                }));
```
