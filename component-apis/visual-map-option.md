# VisualMapOption

`VisualMapOption` is implemented by `ContinousVisualMap` and `PiecewiseVisualMap` whose default types are "continuous" and "piecewise" respectively.

!> Do not use `setType()` to change the default type.

The two classes share most of their APIs:

```java
public class T implements VisualMapOption {
    public T setType(String type);

    public T setTop(Number top);

    public T setTop(String top);

    public T setRight(Number right);

    public T setRight(String right);

    public T setBottom(Number bottom);

    public T setBottom(String bottom);

    public T setLeft(Number left);

    public T setLeft(String left);

    public T setBorderColor(String borderColor);

    public T setBorderWidth(Number borderWidth);

    public T setShow(Boolean show);

    public T setMin(Number min);

    public T setMax(Number max);

    public T setItemWidth(Number itemWidth);

    public T setItemHeight(Number itemHeight);

    public T setInverse(Boolean inverse);

    public T setOrient(String orient);

    public T setPrecision(Number precision);

    public T setColor(String[] color);

    public T setFormatter(String formatter);

    public T setText(String[] text);

    public T setTextStyle(LabelOption textStyle);

    // More ...
}
```

?> `T` represents `ContinousVisualMap` or `PiecewiseVisualMap`.

For more APIs and detailed explanation, please refer to [source code](https://github.com/ECharts-Java/ECharts-Java/tree/master/src/main/java/org/icepear/echarts/components/visualMap) and [Apache ECharts docs](https://echarts.apache.org/en/option.html#visualMap).

## ContinousVisualMap

```java
public class ContinousVisualMap implements ContinousVisualMapOption {
    public ContinousVisualMap setCalculable(Boolean calculable);

    public ContinousVisualMap setRange(Number[] range);

    // More ...
}
```

## PiecewiseVisualMap

```java
public class PiecewiseVisualMap implements PiecewiseVisualMapOption {
    public PiecewiseVisualMap setCategories(String[] categories);

    public PiecewiseVisualMap setMinOpen(Boolean minOpen);

    public PiecewiseVisualMap setMaxOpen(Boolean maxOpen);

    public PiecewiseVisualMap setItemSymbol(String itemSymbol);

    public PiecewiseVisualMap setPieces(VisualPieceOption[] pieces);

    public PiecewiseVisualMap setSplitNumber(Number splitNumber);

    public PiecewiseVisualMap setShowLabel(Boolean showLabel);

    public PiecewiseVisualMap setHoverLink(Boolean hoverLink);

    // More ...
}
```
