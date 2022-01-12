## setSymbol()

```java
public SeriesOption setSymbol(String symbol);
```

`symbol` is the icon to mark data point. Valid values include `"emptyCircle"` (default), `"circle"`, `"rect"`, `"roundRect"`, `"triangle"`, `"diamond"`, `"pin"`, `"arrow"`, `"none"`.

## setSymbolSize()

```java
public SeriesOption setSymbolSize(Number symbolSize);

public SeriesOption setSymbolSize(Number[] symbolSize);
```

`symbolSize` can be set to a single number like `10`, or an array to represent width and height respectively like `[20, 10]`.

## setShowSymbol()

```java
public SeriesOption setShowSymbol(Boolean showSymbol);
```

`showSymbol` determines whether to show symbols of data points.
