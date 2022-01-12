### addParallelAxis()

The coordinate axis for parallel coordinate.

```java
public Chart addParallelAxis(Number dim);

public Chart addParallelAxis(String name, Number dim);

public Chart addParallelAxis(Number dim, String[] data);

public Chart addParallelAxis(String name, Number dim, String[] data);

public Chart addParallelAxis(ParallelAxisOption parallelAxis);
```

`ParallelAxisOption` is implemented by `ValueParallelAxis`, `CategoryParallelAxis`, `TimeParallelAxis`, and `LogParallelAxis`.

For more APIs of `ParallelAxisOption`, please refer to [ParallelAxisOption](component-apis/parallel-axis-option).
