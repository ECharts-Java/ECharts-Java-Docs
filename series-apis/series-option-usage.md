## setName()

```java
public E setName(String name);
```

The `name` of this series will be displayed in [Tooltip](component-apis/tooltip) and [Legend](component-apis/legend).

## setColorBy()

```java
public E setColorBy(String colorBy);
```

Valid values of `colorBy`:
- `"series"`: all data in the same series are in the same color (default)
- `"data"`: each data item uses a different color

## setSymbol()

```java
public E setSymbol(String symbol);
```

`symbol` is the icon to mark data point. Valid values include `"emptyCircle"` (default), `"circle"`, `"rect"`, `"roundRect"`, `"triangle"`, `"diamond"`, `"pin"`, `"arrow"`, `"none"`.

## setSymbolSize()

```java
public E setSymbolSize(Number symbolSize);

public E setSymbolSize(Number[] symbolSize);
```

`symbolSize` can be set to a single number like `10`, or an array to represent width and height respectively like `[20, 10]`.

## setShowSymbol()

```java
public E setShowSymbol(Boolean showSymbol);
```

`showSymbol` determines whether to show symbols of data points.

## setLabel()

```java
public E setLabel(SeriesLabelOption label);
```

`label` is used to show some information about data points like `value`, `name`, and so on.

For more APIs of `SeriesLabelOption`, please refer to [SeriesLabelOption](component-apis/series-label-option).

## setLabelLine()

```java
public E setLabelLine(LabelLineOption labelLine);
```

`labelLine` is the configuration of the line pointing to `label`.


