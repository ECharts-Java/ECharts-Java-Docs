# AxisOption

`AxisOption` is implemented by `ValueAxis`, `CategoryAxis`, `TimeAxis`, and `LogAxis` whose default types are `"value"`, `"category"`, `"time"`, and `"log"` respectively.

!> Do not use `setType()` to change the default type.

The four classes share most of their APIs:

```java
public class T implements AxisOption {
    public T setType(String type);

    public T setShow(Boolean show);

    public T setData(Object[] data);

    public T setPosition(String position);

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

?> `T` represents one of `ValueAxis`, `CategoryAxis`, `TimeAxis`, and `LogAxis`.

For more APIs and detailed explanation, please refer to [source code](https://github.com/ECharts-Java/ECharts-Java/tree/master/src/main/java/org/icepear/echarts/components/coord/cartesian) and [Apache ECharts docs](https://echarts.apache.org/en/option.html#xAxis).

## ValueAxis

```java
public class ValueAxis implements ValueAxisOption {
    public ValueAxis setBoundaryGap(Number[] boundaryGap);

    public ValueAxis setBoundaryGap(String[] boundaryGap);

    public ValueAxis setSplitNumber(Number splitNumber);

    public ValueAxis setInterval(Number interval);

    public ValueAxis setMinInterval(Number minInterval);

    public ValueAxis setMaxInterval(Number maxInterval);

    public ValueAxis setScale(Boolean scale);

    // More ...
}
```

## CategoryAxis

```java
public class CategoryAxis implements CategoryAxisOption {
    public CategoryAxis setBoundaryGap(Boolean boundaryGap);

    public CategoryAxis setDeduplication(Boolean deduplication);

    // More ...
}
```

## TimeAxis

```java
public class TimeAxis implements TimeAxisOption {
    public TimeAxis setBoundaryGap(Number[] boundaryGap);

    public TimeAxis setBoundaryGap(String[] boundaryGap);

    public TimeAxis setSplitNumber(Number splitNumber);

    public TimeAxis setInterval(Number interval);

    public TimeAxis setMinInterval(Number minInterval);

    public TimeAxis setMaxInterval(Number maxInterval);

    // More ...
}
```

## LogAxis

```java
public class LogAxis implements LogAxisOption {
    public LogAxis setBoundaryGap(Number[] boundaryGap);

    public LogAxis setBoundaryGap(String[] boundaryGap);

    public LogAxis setSplitNumber(Number splitNumber);

    public LogAxis setInterval(Number interval);

    public LogAxis setMinInterval(Number minInterval);

    public LogAxis setMaxInterval(Number maxInterval);

    public LogAxis setLogBase(Number logBase);

    // More ...
}
```
