### getOption()

Option contains all configurations of the chart.

```java
public Option getOption();
```

### setTitle()

Title includes a main title and a subtitle if specified. By default, it appears in the top left corner of the chart.

```java
public T setTitle(String text);

public T setTitle(Title title);
```

?> `T` represents any chart type that extends `Chart` (e.g., `LineChart`, `BarChart`). This is used to support method chaining.

For more APIs of `Title`, please refer to [Title](component-apis/title).

### setLegend()

Legend shows symbols, colors, and names of different series. You can click legends to toggle displaying series in the chart.

```java
public T setLegend();

public T setLegend(Legend legend);
```

?> `T` represents any chart type that extends `Chart` (e.g., `LineChart`, `BarChart`). This is used to support method chaining.

For more APIs of `Legend`, please refer to [Legend](component-apis/legend).

### setTooltip()

Tooltip will be triggered when your mouse focuses on data items or axes.

```java
public T setTooltip(String trigger);

public T setTooltip(Tooltip tooltip);
```

?> `T` represents any chart type that extends `Chart` (e.g., `LineChart`, `BarChart`). This is used to support method chaining.

For more APIs of `Tooltip`, please refer to [Tooltip](component-apis/tooltip).

### addDataset()

Dataset enables data reuse by different series and some simple data transforms (e.g., "filter", "sort").

```java
public T addDataset(Object[] source);

public T addDataset(Object[][] source);

public T addDataset(Object[][][] source);

public T addDataset(Dataset dataset);
```

?> `T` represents any chart type that extends `Chart` (e.g., `LineChart`, `BarChart`). This is used to support method chaining.

For more APIs of `Dataset`, please refer to [Dataset](component-apis/dataset).

### setVisualMap()

Visual Mapping maps data to visual channels including symbols, colors, opacity, etc.

```java
public T setVisualMap(Number min, Number max);

public T setVisualMap(VisualMapOption visualMap);
```

?> `T` represents any chart type that extends `Chart` (e.g., `LineChart`, `BarChart`). This is used to support method chaining.

`VisualMapOption` is implemented by `ContinousVisualMap` and `PiecewiseVisualMap`.

For more APIs of `VisualMapOption`, please refer to [VisualMapOption](component-apis/visual-map-option).

### addSeries()

Series contains data.

```java
public T addSeries(Object[] data);

public T addSeries(Object[][] data);

public T addSeries(Object[][][] data);

public T addSeries(String name, Object[] data);

public T addSeries(String name, Object[][] data);

public T addSeries(String name, Object[][][] data);

public T addSeries(E series);
```

?> `T` represents any chart type that extends `Chart` (e.g., `LineChart`, `BarChart`). This is used to support method chaining. 

?> `E` represents any class that extends `SeriesOption` (e.g., `LineSeries`, `BarSeries`).

TODO: For more APIs of `SeriesOption`, please refer to [SeriesOption]().
