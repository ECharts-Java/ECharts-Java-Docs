## setCoordinateSystem()

```java
public SeriesOption setCoordinateSystem(String coordinateSystem);
```

Valid values of `coordinateSystem`:
- `"cartesian2d"`: two-dimensional rectangular coordinate (also known as Cartesian coordinate) (default)
- `"polar"`: polar coordinate

## setStep()

```java
public SeriesOption setStep(Boolean step);

public SeriesOption setStep(String step);
```

`step` determines whether to show the series as a step line. Valid values include `true`, `false` (default), or `"start"`, `"middle"`, `"end"` which configure the turn point of the step line.

## setItemStyle()

```java
public SeriesOption setItemStyle(ItemStyleOption itemStyle);
```

`itemStyle` is the style of data points.

For more APIs of `ItemStyleOption`, please refer to [ItemStyleOption](component-apis/item-style-option).

## setLineStyle()

```java
public SeriesOption setLineStyle(LineStyleOption lineStyle);
```

`lineStyle` is the style of the lines connecting data points.

For more APIs of `LineStyleOption`, please refer to [LineStyleOption](component-apis/line-style-option).

## setAreaStyle()

```java
public SeriesOption setAreaStyle(LineAreaStyleOption areaStyle);
```

`areaStyle` is the style of the areas among lines and axes.

TODO: For more APIs of `LineAreaStyleOption`, please refer to [LineAreaStyleOption](component-apis/line-area-style-option).

## setEmphasis()

```java
public SeriesOption setEmphasis(LineEmphasisOption emphasis);
```

`emphasis` is the highlight style of the chart.

TODO: For more APIs of `LineEmphasisOption`, please refer to [LineEmphasisOption](component-apis/line-emphasis-option).

## setSmooth()

```java
public SeriesOption setSmooth(Boolean smooth);

public SeriesOption setSmooth(Number smooth);
```

`smooth` determines whether to show the line as a smooth curve.  It can be a `Boolean` or a `Number` ranging from `0` to `1` which indicates the smoothness.

## setData()

```java
public SeriesOption setData(LineDataItemOption[] data);

public SeriesOption setData(Object[] data);
```

`data` is an array of data points. `Object` can be `String` or `Number` or a mixure of `String` and `Number`.

TODO: For more APIs of `LineDataItemOption`, please refer to [LineDataItemOption](component-apis/line-data-item-option).
