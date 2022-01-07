# RadiusAxisOption

`RadiusAxisOption` is implemented by `ValueRadiusAxis`, `CategoryRadiusAxis`, `TimeRadiusAxis`, and `LogRadiusAxis` whose default types are "value", "category", "time", and "log" respectively.

!> Do not use `setType()` to change the default type.

The four classes share most of their APIs:

```java
public class T implements RadiusAxisOption {
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

    // More ...
}
```

?> `T` represents one of `ValueRadiusAxis`, `CategoryRadiusAxis`, `TimeRadiusAxis`, and `LogRadiusAxis`.

For more APIs and detailed explanation, please refer to [source code](https://github.com/ECharts-Java/ECharts-Java/tree/master/src/main/java/org/icepear/echarts/components/coord/polar) and [Apache ECharts docs](https://echarts.apache.org/en/option.html#radiusAxis).

## ValueRadiusAxis

```java
public class ValueRadiusAxis implements ValueRadiusAxisOption {
    public ValueRadiusAxis setBoundaryGap(Number[] boundaryGap);

    public ValueRadiusAxis setBoundaryGap(String[] boundaryGap);

    public ValueRadiusAxis setSplitNumber(Number splitNumber);

    public ValueRadiusAxis setInterval(Number interval);

    public ValueRadiusAxis setMinInterval(Number minInterval);

    public ValueRadiusAxis setMaxInterval(Number maxInterval);

    public ValueRadiusAxis setScale(Boolean scale);

    // More ...
}
```

## CategoryRadiusAxis

```java
public class CategoryRadiusAxis implements CategoryRadiusAxisOption {
    public CategoryRadiusAxis setBoundaryGap(Boolean boundaryGap);

    public CategoryRadiusAxis setDeduplication(Boolean deduplication);

    // More ...
}
```

## TimeRadiusAxis

```java
public class TimeRadiusAxis implements TimeRadiusAxisOption {
    public TimeRadiusAxis setBoundaryGap(Number[] boundaryGap);

    public TimeRadiusAxis setBoundaryGap(String[] boundaryGap);

    public TimeRadiusAxis setSplitNumber(Number splitNumber);

    public TimeRadiusAxis setInterval(Number interval);

    public TimeRadiusAxis setMinInterval(Number minInterval);

    public TimeRadiusAxis setMaxInterval(Number maxInterval);

    // More ...
}
```

## LogRadiusAxis

```java
public class LogRadiusAxis implements LogRadiusAxisOption {
    public LogRadiusAxis setBoundaryGap(Number[] boundaryGap);

    public LogRadiusAxis setBoundaryGap(String[] boundaryGap);

    public LogRadiusAxis setSplitNumber(Number splitNumber);

    public LogRadiusAxis setInterval(Number interval);

    public LogRadiusAxis setMinInterval(Number minInterval);

    public LogRadiusAxis setMaxInterval(Number maxInterval);

    public LogRadiusAxis setLogBase(Number logBase);

    // More ...
}
```
