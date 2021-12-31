# Chart

```java
public abstract class Chart<T extends Chart<?, ?>, E extends SeriesOption> {
    public Option getOption();

    public T setTitle(String title);

    public T setLegend(Boolean show);

    public T setTooltip(String trigger);

    public T addDataset(Object[] dataset);

    public T addDataset(Object[][] dataset);

    public T addDataset(Object[][][] dataset);

    public T setVisualMap(Number min, Number max);

    public T setVisualMap(VisualMapOption visualMap);

    public T addSeries(Object[] series);

    public T addSeries(Object[][] series);

    public T addSeries(Object[][][] series);

    public T addSeries(String name, Object[] series);

    public T addSeries(String name, Object[][] series);

    public T addSeries(String name, Object[][][] series);

    public T addSeries(E series);
}
```
