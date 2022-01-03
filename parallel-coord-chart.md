# ParallelCoordChart

```java
public abstract class ParallelCoordChart<T extends Chart<?, ?>, E extends SeriesOption> extends Chart<T, E> {
    public T addParallelAxis(Number dim);

    public T addParallelAxis(String name, Number dim);

    public T addParallelAxis(Number dim, String[] parallelAxis);

    public T addParallelAxis(String name, Number dim, String[] parallelAxis);

    public T addParallelAxis(ParallelAxisOption parallelAxis);
}
```
