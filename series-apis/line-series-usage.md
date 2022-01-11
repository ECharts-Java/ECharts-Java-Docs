## setStep()

```java
public E setStep(Boolean step);

public E setStep(String step);
```

`step` determines whether to show the series as a step line. Valid values include `true`, `false` (default), or `"start"`, `"middle"`, `"end"` which configure the turn point of the step line.

## setItemStyle()

```java
public E setItemStyle(ItemStyleOption itemStyle);
```

`itemStyle` is the style of data points.

For more APIs of `ItemStyleOption`, please refer to [ItemStyleOption](component-apis/item-style-option).

## setLineStyle()

```java
public E setLineStyle(LineStyleOption lineStyle);
```

`lineStyle` is the style of the lines connecting data points.

For more APIs of `LineStyleOption`, please refer to [LineStyleOption](component-apis/line-style-option).

## setAreaStyle()

```java
public E setAreaStyle(LineAreaStyleOption areaStyle);
```

`areaStyle` is the style of the areas among lines and axes.

TODO: For more APIs of `LineAreaStyleOption`, please refer to [LineAreaStyleOption](component-apis/line-area-style-option).

## setEmphasis()

```java
public E setEmphasis(LineEmphasisOption emphasis);
```

`emphasis` is the highlight style of the chart.

## setSmooth()

```java
public E setSmooth(Boolean smooth);

public E setSmooth(Number smooth);
```

`smooth` determines whether to show the line as a smooth curve.

## setData()

```java
public E setData(LineDataItemOption[] data);

public E setData(Object[] data);
```
