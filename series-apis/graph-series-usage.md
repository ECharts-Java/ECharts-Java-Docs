## setLayout()

```java
public SeriesOption setLayout(String layout);
```

Valid values of `layout`:
- `"none"`: nodes are arranged by their specified position `GraphNodeItem.x` and `GraphNodeItem.y` (default)
- `"circular"`: nodes are arranged in circle
- `"force"`: nodes are arranged like there is repulsion and attraction between each other

## setCircular()

```java
public SeriesOption setCircular(GraphCircularOption circular);
```

`circular` is the configuration of `"circular"` layout.

For more APIs of `GraphCircularOption`, please refer to [GraphCircularOption](component-apis/graph-circular-option).

## setForce()

```java
public SeriesOption setForce(GraphForceOption force);
```

`force` is the configuration of `"force"` layout.

For more APIs of `GraphForceOption`, please refer to [GraphForceOption](component-apis/graph-force-option).

## setItemStyle()

```java
public SeriesOption setItemStyle(ItemStyleOption itemStyle);
```

`itemStyle` is the style of nodes.

For more APIs of `ItemStyleOption`, please refer to [ItemStyleOption](component-apis/item-style-option).

## setLineStyle()

```java
public SeriesOption setLineStyle(GraphEdgeLineStyleOption lineStyle);
```

`lineStyle` is the style of edges.

TODO: For more APIs of `GraphEdgeLineStyleOption`, please refer to [GraphEdgeLineStyleOption](component-apis/graph-edge-line-style-option).

## setEdgeLabel()

```java
public SeriesOption setEdgeLabel(SeriesLineLabelOption edgeLabel);
```

`edgeLabel` is used to show some information about edges of the graph.

## setEmphasis()

```java
public SeriesOption setEmphasis(GraphEmphasisOption emphasis);
```

`emphasis` is the highlight style of the chart.

TODO: For more APIs of `GraphEmphasisOption`, please refer to [GraphEmphasisOption](component-apis/graph-emphasis-option).

## setCategories()

```java
public SeriesOption setCategories(GraphCategoryItemOption[] categories);
```

`categories` contain the style of each category.

For more APIs of `GraphCategoryItemOption`, please refer to [GraphCategoryItemOption](component-apis/graph-category-item-option).

## setData()

```java
public SeriesOption setData(GraphNodeItemOption[] data);

public SeriesOption setData(Object[] data);

public SeriesOption setData(Object[][] data);
```

`data` contains nodes of the graph. `Object` can be `Number` or `String`.

TODO: For more APIs of `GraphNodeItemOption`, please refer to [GraphNodeItemOption](component-apis/graph-node-item-option).

## setLinks()

```java
public SeriesOption setLinks(GraphEdgeItemOption[] links);
```

`links` contain edges of the graph.

TODO: For more APIs of `GraphEdgeItemOption`, please refer to [GraphEdgeItemOption](component-apis/graph-edge-item-option).
