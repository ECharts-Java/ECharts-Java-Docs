## setLayout()

```java
public SeriesOption setLayout(String layout);
```

Valid values of `layout`:
- `"horizontal"`: horizontally show all boxes
- `"vertical"`: vertically show all boxes

## setBoxWidth()

```java
public SeriesOption setBoxWidth(Number[] boxWidth);

public SeriesOption setBoxWidth(String[] boxWidth);
```

`boxWidth` determines the lower and upper boundary of box bix width. The array is in the form of `[min, max]`.

It could be absolute value in pixel, such as `[7, 50]`, or percentage, such as `["40%", "90%"]` which means the percentage to the maximum possible width.

## setItemStyle()

```java
public SeriesOption setItemStyle(ItemStyleOption itemStyle);
```

`itemStyle` determines the style of boxplot.

For more APIs of `ItemStyleOption`, please refer to [ItemStyleOption](component-apis/item-style-option).

## setEmphasis()

```java
public SeriesOption setEmphasis(BoxplotEmphasisOption emphasis);
```

`emphasis` is the highlight style of the chart.

TODO: For more APIs of `BoxplotEmphasisOption`, please refer to [BoxplotEmphasisOption](component-apis/boxplot-emphasis-option).

## setData()

```java
public BoxplotSeries setData(BoxplotDataItemOption[] data);

public BoxplotSeries setData(Number[][] data);
```

`data` can be a two-dimensional `Number` array where each line is in the form of `[min,  Q1,  median (or Q2),  Q3,  max]`.

TODO: For more APIs of `BoxplotDataItemOption`, please refer to [BoxplotDataItemOption](component-apis/boxplot-data-item-option).
