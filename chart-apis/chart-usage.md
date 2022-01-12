### getOption()

Option contains all configurations of the chart.

```java
public Option getOption();
```

### setTitle()

Title includes a main title and a subtitle if specified. By default, it appears in the top left corner of the chart.

```java
public Chart setTitle(String text);

public Chart setTitle(Title title);
```

For more APIs of `Title`, please refer to [Title](component-apis/title).

### setLegend()

Legend shows symbols, colors, and names of different series. You can click legends to toggle displaying series in the chart.

```java
public Chart setLegend();

public Chart setLegend(Legend legend);
```

For more APIs of `Legend`, please refer to [Legend](component-apis/legend).

### setTooltip()

Tooltip will be triggered when your mouse focuses on data items or axes.

```java
public Chart setTooltip(String trigger);

public Chart setTooltip(Tooltip tooltip);
```

For more APIs of `Tooltip`, please refer to [Tooltip](component-apis/tooltip).

### addDataset()

Dataset enables data reuse by different series and some simple data transforms (e.g., `"filter"`, `"sort"`).

```java
public Chart addDataset(Object[] source);

public Chart addDataset(Object[][] source);

public Chart addDataset(Object[][][] source);

public Chart addDataset(Dataset dataset);
```

For more APIs of `Dataset`, please refer to [Dataset](component-apis/dataset).

### setVisualMap()

Visual Mapping maps data to visual channels including symbols, colors, opacity, etc.

```java
public Chart setVisualMap(Number min, Number max);

public Chart setVisualMap(VisualMapOption visualMap);
```

`VisualMapOption` is implemented by `ContinousVisualMap` and `PiecewiseVisualMap`.

For more APIs of `VisualMapOption`, please refer to [VisualMapOption](component-apis/visual-map-option).

### addSeries()

Series contains data.

```java
public Chart addSeries(Object[] data);

public Chart addSeries(Object[][] data);

public Chart addSeries(Object[][][] data);

public Chart addSeries(String name, Object[] data);

public Chart addSeries(String name, Object[][] data);

public Chart addSeries(String name, Object[][][] data);

public Chart addSeries(SeriesOption series);
```

For more APIs of `SeriesOption`, please refer to [SeriesOption](series-apis/series-option).
