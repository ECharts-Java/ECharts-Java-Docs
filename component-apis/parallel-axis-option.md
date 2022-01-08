# ParallelAxisOption

`ParallelAxisOption` is implemented by `ValueParallelAxis`, `CategoryParallelAxis`, `TimeParallelAxis`, and `LogParallelAxis` whose default types are "value", "category", "time", and "log" respectively.

!> Do not use `setType()` to change the default type.

The four classes share most of their APIs:

```java
public class T implements ParallelAxisOption {
    public T setType(String type);

    public T setData(Object[] data);

    public T setName(String name);

    public T setNameLocation(String nameLocation);

    public T setNameRotate(Number nameRotate);

    public T setNameTextStyle(AxisNameTextStyleOption nameTextStyle);

    public T setNameGap(Number nameGap);    

    public T setInverse(Boolean inverse);

    public T setAxisLabel(AxisLabelBaseOption axisLabel);

    public T setAxisLine(AxisLineOption axisLine);

    public T setAxisTick(AxisTickOption axisTick);

    public T setMinorTick(MinorTickOption minorTick);

    public T setSplitLine(SplitLineOption splitLine);

    public T setSplitLine(MinorSplitLineOption minorSplitLine);

    public T setSplitArea(SplitAreaOption splitArea);

    public T setMin(Number min);

    public T setMin(String min);

    public T setMax(Number max);

    public T setMax(String max);

    public T setDim(Number dim);

    public T setDim(Number[] dim);

    // More ...
}
```

?> `T` represents one of `ValueParallelAxis`, `CategoryParallelAxis`, `TimeParallelAxis`, and `LogParallelAxis`.

For more APIs and detailed explanation, please refer to [source code](https://echarts.apache.org/en/option.html#parallelAxis) and [Apache ECharts docs](https://github.com/ECharts-Java/ECharts-Java/tree/master/src/main/java/org/icepear/echarts/components/coord/parallel).

## ValueParallelAxis

```java
public class ValueParallelAxis implements ValueParallelAxisOption {
    public ValueParallelAxis setBoundaryGap(Number[] boundaryGap);

    public ValueParallelAxis setBoundaryGap(String[] boundaryGap);

    public ValueParallelAxis setSplitNumber(Number splitNumber);

    public ValueParallelAxis setInterval(Number interval);

    public ValueParallelAxis setMinInterval(Number minInterval);

    public ValueParallelAxis setMaxInterval(Number maxInterval);

    public ValueParallelAxis setScale(Boolean scale);

    // More ...
}
```

## CategoryParallelAxis

```java
public class CategoryParallelAxis implements CategoryParallelAxisOption {
    public CategoryParallelAxis setBoundaryGap(Boolean boundaryGap);

    public CategoryParallelAxis setDeduplication(Boolean deduplication);

    // More ...
}
```

## TimeParallelAxis

```java
public class TimeParallelAxis implements TimeParallelAxisOption {
    public TimeParallelAxis setBoundaryGap(Number[] boundaryGap);

    public TimeParallelAxis setBoundaryGap(String[] boundaryGap);

    public TimeParallelAxis setSplitNumber(Number splitNumber);

    public TimeParallelAxis setInterval(Number interval);

    public TimeParallelAxis setMinInterval(Number minInterval);

    public TimeParallelAxis setMaxInterval(Number maxInterval);

    // More ...
}
```

## LogParallelAxis

```java
public class LogParallelAxis implements LogParallelAxisOption {
    public LogParallelAxis setBoundaryGap(Number[] boundaryGap);

    public LogParallelAxis setBoundaryGap(String[] boundaryGap);

    public LogParallelAxis setSplitNumber(Number splitNumber);

    public LogParallelAxis setInterval(Number interval);

    public LogParallelAxis setMinInterval(Number minInterval);

    public LogParallelAxis setMaxInterval(Number maxInterval);

    public LogParallelAxis setLogBase(Number logBase);

    // More ...
}
```
