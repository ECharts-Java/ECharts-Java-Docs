# AngleAxisOption

`AngleAxisOption` is implemented by `ValueAngleAxis`, `CategoryAngleAxis`, `TimeAngleAxis`, and `LogAngleAxis` whose default types are "value", "category", "time", and "log" respectively.

!> Do not use `setType()` to change the default type.

The four classes share most of their APIs:

```java
public class T implements AngleAxisOption {
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

    public T setStartAngle(Number startAngle);

    public T setClockwise(Boolean clockwise);

    // More ...
}
```

?> `T` represents one of `ValueAngleAxis`, `CategoryAngleAxis`, `TimeAngleAxis`, and `LogAngleAxis`.

For more APIs and detailed explanation, please refer to [source code](https://github.com/ECharts-Java/ECharts-Java/tree/master/src/main/java/org/icepear/echarts/components/coord/polar) and [Apache ECharts docs](https://echarts.apache.org/en/option.html#angleAxis).

## ValueAngleAxis

```java
public class ValueAngleAxis implements ValueAngleAxisOption {
    public ValueAngleAxis setBoundaryGap(Number[] boundaryGap);

    public ValueAngleAxis setBoundaryGap(String[] boundaryGap);

    public ValueAngleAxis setSplitNumber(Number splitNumber);

    public ValueAngleAxis setInterval(Number interval);

    public ValueAngleAxis setMinInterval(Number minInterval);

    public ValueAngleAxis setMaxInterval(Number maxInterval);

    public ValueAngleAxis setScale(Boolean scale);

    // More ...
}
```

## CategoryAngleAxis

```java
public class CategoryAngleAxis implements CategoryAngleAxisOption {
    public CategoryAngleAxis setBoundaryGap(Boolean boundaryGap);

    public CategoryAngleAxis setDeduplication(Boolean deduplication);

    // More ...
}
```

## TimeAngleAxis

```java
public class TimeAngleAxis implements TimeAngleAxisOption {
    public TimeAngleAxis setBoundaryGap(Number[] boundaryGap);

    public TimeAngleAxis setBoundaryGap(String[] boundaryGap);

    public TimeAngleAxis setSplitNumber(Number splitNumber);

    public TimeAngleAxis setInterval(Number interval);

    public TimeAngleAxis setMinInterval(Number minInterval);

    public TimeAngleAxis setMaxInterval(Number maxInterval);

    // More ...
}
```

## LogAngleAxis

```java
public class LogAngleAxis implements LogAngleAxisOption {
    public LogAngleAxis setBoundaryGap(Number[] boundaryGap);

    public LogAngleAxis setBoundaryGap(String[] boundaryGap);

    public LogAngleAxis setSplitNumber(Number splitNumber);

    public LogAngleAxis setInterval(Number interval);

    public LogAngleAxis setMinInterval(Number minInterval);

    public LogAngleAxis setMaxInterval(Number maxInterval);

    public LogAngleAxis setLogBase(Number logBase);

    // More ...
}
```
