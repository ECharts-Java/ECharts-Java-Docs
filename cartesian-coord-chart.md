# CartesianCoordChart

```java
public abstract class CartesianCoordChart<T extends Chart<?, ?>, E extends SeriesOption> extends Chart<T, E> {
    public T addXAxis();

    public T addXAxis(String name);

    public T addXAxis(String[] xAxis);

    public T addXAxis(String name, String[] xAxis);

    public T addXAxis(AxisOption xAxis);

    public T addYAxis();

    public T addYAxis(String name);

    public T addYAxis(String[] yAxis);

    public T addYAxis(String name, String[] yAxis);

    public T addYAxis(AxisOption yAxis);
}
```
