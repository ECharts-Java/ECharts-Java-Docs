```java
Tree tree = new Tree()
        .setTooltip("item")
        .addSeries(new TreeSeries()
                .setLabel(new SeriesLabel().setPosition("left").setAlign("right"))
                .setLeaves(new TreeLeaves()
                        .setLabel(new SeriesLabel().setPosition("right").setAlign("left")))
                .setEmphasis(new TreeEmphasis().setFocus("descendant"))
                .setData(new TreeNodeItem[] {
                        new TreeNodeItem().setName("flare")
                                .setChildren(new TreeNodeItem[] {
                                        new TreeNodeItem().setName("analytics")
                                                .setChildren(new TreeNodeItem[] {
                                                        new TreeNodeItem().setName("cluster").setValue(3938),
                                                        new TreeNodeItem().setName("graph").setValue(3534)
                                                }),
                                        new TreeNodeItem().setName("animate").setValue(17010)
                                })
                }));
```
