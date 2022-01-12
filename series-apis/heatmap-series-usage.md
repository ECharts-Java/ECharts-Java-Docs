## setCoordinateSystem()

```java
public SeriesOption setCoordinateSystem(String coordinateSystem);
```

Valid values of `coordinateSystem`:
- `"cartesian2d"`: two-dimensional rectangular coordinate (also known as Cartesian coordinate) (default)
- `"geo"`: geographic coordinate

## setItemStyle()

```java
public SeriesOption setItemStyle(ItemStyleOption itemStyle);
```

`itemStyle` is the style of data points.

For more APIs of `ItemStyleOption`, please refer to [ItemStyleOption](component-apis/item-style-option).

## setEmphasis()

```java
public SeriesOption setEmphasis(HeatmapEmphasisOption emphasis);
```

`emphasis` is the highlight style of the chart.

TODO: For more APIs of `HeatmapEmphasisOption`, please refer to [HeatmapEmphasisOption](component-apis/heatmap-emphasis-option).

## setData()

```java
public SeriesOption setData(HeatmapDataItemOption[] data);

public SeriesOption setData(Object[][] data);
```

`data` can be a two-dimensional array of data points. `Object` can be `String` or `Number` or a mixure of `String` and `Number`.

TODO: For more APIs of `HeatmapDataItemOption`, please refer to [HeatmapDataItemOption](component-apis/heatmap-data-item-option).
