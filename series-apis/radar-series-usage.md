## setItemStyle()

```java
public SeriesOption setItemStyle(ItemStyleOption itemStyle);
```

`itemStyle` is the style of the inflection point of the lines.

For more APIs of `ItemStyleOption`, please refer to [ItemStyleOption](component-apis/item-style-option).

## setLineStyle()

```java
public SeriesOption setLineStyle(LineStyleOption lineStyle);
```

`lineStyle` is the style of lines.

For more APIs of `LineStyleOption`, please refer to [LineStyleOption](component-apis/line-style-option).

## setAreaStyle()

```java
public SeriesOption setAreaStyle(AreaStyleOption areaStyle);
```

`areaStyle` is the style of filling area.

For more APIs of `AreaStyleOption`, please refer to [AreaStyleOption](component-apis/area-style-option).

## setEmphasis()

```java
public SeriesOption setEmphasis(RadarEmphasisOption emphasis);
```

`emphasis` is the highlight style of the chart.

TODO: For more APIs of `RadarEmphasisOption`, please refer to [RadarEmphasisOption](component-apis/radar-emphasis-option).

## setData()

```java
public SeriesOption setData(Object[][] data);

public SeriesOption setData(RadarDataItemOption[] data);
```

`data` can be a two-dimensional array where a data point of each row is corresponding to an indicator of the radar chart. `Object` can be `String` or `Number`.

TODO: For more APIs of `RadarDataItemOption`, please refer to [RadarDataItemOption](component-apis/radar-data-item-option).
