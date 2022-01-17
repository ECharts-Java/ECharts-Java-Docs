## setClockwise()

```java
public SeriesOption setClockwise(Boolean clockwise);
```

`clockwise` determines whether the layout of sectors of pie chart is clockwise.

## setStartAngle()

```java
public SeriesOption setStartAngle(Number startAngle);
```

`startAngle` ranges from `0` to `360`. The default value is `90`.

## setMinAngle()

```java
public SeriesOption setMinAngle(Number minAngle);
```

`minAngle` is the minimum angle of a sector. It prevents some sectors from being too small when the value is small.

## setMinShowLabelAngle()

```java
public SeriesOption setMinShowLabelAngle(Number minShowLabelAngle);
```

If the angle of a sector is less than `minShowLabelAngle`, its `label` and `labelLine` will not be displayed.

## setRoseType()

```java
public SeriesOption setRoseType(String roseType);
```

`roseType` determines whether to show the pie chart as a rose chart and the type of the rose chart.

Valid values of `roseType`:
- `"radius"`: use central angle to show the percentage of data, radius to show data size
- `"area"`: all the sectors will share the same central angle, the data size is shown only through radiuses

## setAvoidLabelOverlap()

```java
public SeriesOption setAvoidLabelOverlap(Boolean avoidLabelOverlap);
```

`avoidLabelOverlap` determines whether to hide overlapped labels of sectors. The default value is `true`.

## setItemStyle()

```java
public SeriesOption setItemStyle(PieItemStyleOption itemStyle);
```

`itemStyle` is the style of each sector of the pie chart.

TODO: For more APIs of `PieItemStyleOption`, please refer to [PieItemStyleOption](component-apis/pie-item-style-option).

## setEmphasis()

```java
public SeriesOption setEmphasis(PieEmphasisOption emphasis);
```

`emphasis` is the highlight style of the chart.

TODO: For more APIs of `PieEmphasisOption`, please refer to [PieEmphasisOption](component-apis/pie-emphasis-option).

## setRadius()

```java
public SeriesOption setRadius(Number radius);

public SeriesOption setRadius(String radius);

public SeriesOption setRadius(Object[] radius);
```

`radius` can be absolute value in pixel (`Number`), percentage (`String`), or a two-element array (`Object[]`). `Object` can be `Number`, `String`, or a mixture of `Number` and `String`, such as `[0, "75%"]`. The default value is `[0, "75%"]`.

## setData()

```java
public SeriesOption setData(Number[] data);

public SeriesOption setData(PieDataItemOption[] data);
```

`data` can be an array of data points where each element is corresponding to `PieDataItem.value`.

TODO: For more APIs of `PieDataItemOption`, please refer to [PieDataItemOption](component-apis/pie-data-item-option).
