## setLayout()

```java
public SeriesOption setLayout(String layout);
```

Valid values of `layout`:
- `"horizontal"`: horizontally show all boxes
- `"vertical"`: vertically show all boxes

## setBarWidth()

```java
public SeriesOption setBarWidth(Number barWidth);

public SeriesOption setBarWidth(String barWidth);
```

`barWidth` is the width of each bar which is adaptive when not specified. It be an absolute value like `10` or a percent value like `"20%"`.

## setItemStyle()

```java
public SeriesOption setItemStyle(CandlestickItemStyleOption itemStyle);
```

`itemStyle` is the style of candlesticks.

TODO: For more APIs of `CandlestickItemStyleOption`, please refer to [CandlestickItemStyleOption](component-apis/candlestick-item-style-option).

## setEmphasis()

```java
public SeriesOption setEmphasis(CandlestickEmphasisOption emphasis);
```

`emphasis` is the highlight style of the chart.

TODO: For more APIs of `CandlestickEmphasisOption`, please refer to [CandlestickEmphasisOption](component-apis/candlestick-emphasis-option).

## setData()

```java
public CandlestickSeries setData(CandlestickDataItemOption[] data);

public CandlestickSeries setData(Number[][] data);
```

`data` can be a two-dimensional `Number` array where each line is in the form of `[open, close, lowest, highest]`.

TODO: For more APIs of `CandlestickDataItemOption`, please refer to [CandlestickDataItemOption](component-apis/candlestick-data-item-option).
