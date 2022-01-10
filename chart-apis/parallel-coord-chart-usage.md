### addParallelAxis()

The coordinate axis for parallel coordinate.

```java
public T addParallelAxis(Number dim);

public T addParallelAxis(String name, Number dim);

public T addParallelAxis(Number dim, String[] data);

public T addParallelAxis(String name, Number dim, String[] data);

public T addParallelAxis(ParallelAxisOption parallelAxis);
```

?> `T` represents any chart type that extends `ParallelCoordChart` (e.g., `Parallel`). This is used to support method chaining.

`ParallelAxisOption` is implemented by `ValueParallelAxis`, `CategoryParallelAxis`, `TimeParallelAxis`, and `LogParallelAxis`.

For more APIs of `ParallelAxisOption`, please refer to [ParallelAxisOption](component-apis/parallel-axis-option).
