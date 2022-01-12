## setCoordinateSystem()

```java
public SeriesOption setCoordinateSystem(String coordinateSystem);
```

Valid values of `coordinateSystem`:
- `"cartesian2d"`: two-dimensional rectangular coordinate (also known as Cartesian coordinate) (default)
- `"polar"`: polar coordinate

## setShowBackground()

```java
public SeriesOption setShowBackground(Boolean showBackground);
```

`showBackground` determines whether to show background behind each bar.

## setItemStyle()

```java
public SeriesOption setItemStyle(BarItemStyleOption itemStyle);
```

`itemStyle` is the style of data points.

TODO: For more APIs of `BarItemStyleOption`, please refer to [BarItemStyleOption](component-apis/bar-item-style-option).

## setEmphasis()

```java
public SeriesOption setEmphasis(BarEmphasisOption emphasis);
```

`emphasis` is the highlight style of the chart.

TODO: For more APIs of `BarEmphasisOption`, please refer to [BarEmphasisOption](component-apis/bar-emphasis-option).

## setBarWidth()

```java
public SeriesOption setBarWidth(Number barWidth);

public SeriesOption setBarWidth(String barWidth);
```

`barWidth` is the width of each bar which is adaptive when not specified. It be an absolute value like `40` or a percent value like `"60%"`.

## setBarGap()

```java
public SeriesOption setBarGap(Number barGap);

public SeriesOption setBarGap(String barGap);
```

`barGap` is the gap between bars of different series. If it is a percent value like `"30%"`, that means `30%` of `barWidth`.

Setting `barGap` as `"-100%"` can overlap bars of different series. The defaule value is `"30%"`.

## setBarCategoryGap()

```java
public SeriesOption setBarCategoryGap(Number barCategoryGap);

public SeriesOption setBarCategoryGap(String barCategoryGap);
```

`barCategoryGap` is the gap between categories of the category axis. The default value is `"20%"`.

## setData()

```java
public SeriesOption setData(BarDataItemOption[] data);

public SeriesOption setData(Object[] data);

public SeriesOption setData(Object[][] data);
```

`data` is an array of data points. `Object` can be `String` or `Number` or a mixure of `String` and `Number`.

TODO: For more APIs of `BarDataItemOption`, please refer to [BarDataItemOption](component-apis/bar-data-item-option).
