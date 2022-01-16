## setLineStyle()

```java
public SeriesOption setLineStyle(LineStyleOption lineStyle);
```

`lineStyle` is the style of lines.

For more APIs of `LineStyleOption`, please refer to [LineStyleOption](component-apis/line-style-option).

## setEmphasis()

```java
public SeriesOption setEmphasis(ParallelEmphasisOption emphasis);
```

`emphasis` is the highlight style of the chart.

TODO: For more APIs of `ParallelEmphasisOption`, please refer to [ParallelEmphasisOption](component-apis/parallel-emphasis-option).

## setSmooth()

```java
public SeriesOption setSmooth(Boolean smooth);

public SeriesOption setSmooth(Number smooth);
```

`smooth` determines whether to show the line as a smooth curve. It can be a `Boolean` or a `Number` ranging from `0` to `1` which indicates the smoothness.

## setData()

```java
public ParallelSeries setData(Object[][] data);

public ParallelSeries setData(ParallelDataItemOption[] data);
```

`data` can be a two-dimensional array where each row is corresponding to `ParallelDataItem.value`. `Object` can be `String` or `Number` or a mixure of `String` and `Number`.

TODO: For more APIs of `ParallelDataItemOption`, please refer to [ParallelDataItemOption](component-apis/parallel-data-item-option).
