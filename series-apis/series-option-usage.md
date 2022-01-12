## setName()

```java
public SeriesOption setName(String name);
```

The `name` of this series will be displayed in [Tooltip](component-apis/tooltip) and [Legend](component-apis/legend).

## setColorBy()

```java
public SeriesOption setColorBy(String colorBy);
```

Valid values of `colorBy`:
- `"series"`: all data in the same series are in the same color (default)
- `"data"`: each data item uses a different color

## setLabel()

```java
public SeriesOption setLabel(SeriesLabelOption label);
```

`label` is used to show some information about data points like `value`, `name`, and so on.

For more APIs of `SeriesLabelOption`, please refer to [SeriesLabelOption](component-apis/series-label-option).

## setLabelLine()

```java
public SeriesOption setLabelLine(LabelLineOption labelLine);
```

`labelLine` is the configuration of the line pointing to `label`.

For more APIs of `LabelLineOption`, please refer to [LabelLineOption](component-apis/label-line-option).
