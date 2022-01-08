# SingleAxisOption

`SingleAxisOption` is implemented by `ValueSingleAxis`, `CategorySingleAxis`, `TimeSingleAxis`, and `LogSingleAxis` whose default types are "value", "category", "time", and "log" respectively.

!> Do not use `setType()` to change the default type.

The four classes share most of their APIs:

```java
public class T implements SingleAxisOption {
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

    public T setWidth(Number width);

    public T setWidth(String width);

    public T setHeight(Number height);

    public T setHeight(String height);

    public T setTop(Number top);

    public T setTop(String top);

    public T setRight(Number right);

    public T setRight(String right);

    public T setBottom(Number bottom);

    public T setBottom(String bottom);

    public T setLeft(Number left);

    public T setLeft(String left);

    public T setPosition(String position);

    public T setOrient(String orient);

    // More ...
}
```

?> `T` represents one of `ValueSingleAxis`, `CategorySingleAxis`, `TimeSingleAxis`, and `LogSingleAxis`.

For more APIs and detailed explanation, please refer to [source code](https://echarts.apache.org/en/option.html#singleAxis) and [Apache ECharts docs](https://github.com/ECharts-Java/ECharts-Java/tree/master/src/main/java/org/icepear/echarts/components/coord/single).

## ValueSingleAxis

```java
public class ValueSingleAxis implements ValueSingleAxisOption {
    public ValueSingleAxis setBoundaryGap(Number[] boundaryGap);

    public ValueSingleAxis setBoundaryGap(String[] boundaryGap);

    public ValueSingleAxis setSplitNumber(Number splitNumber);

    public ValueSingleAxis setInterval(Number interval);

    public ValueSingleAxis setMinInterval(Number minInterval);

    public ValueSingleAxis setMaxInterval(Number maxInterval);

    public ValueSingleAxis setScale(Boolean scale);

    // More ...
}
```

## CategorySingleAxis

```java
public class CategorySingleAxis implements CategorySingleAxisOption {
    public CategorySingleAxis setBoundaryGap(Boolean boundaryGap);

    public CategorySingleAxis setDeduplication(Boolean deduplication);

    // More ...
}
```

## TimeSingleAxis

```java
public class TimeSingleAxis implements TimeSingleAxisOption {
    public TimeSingleAxis setBoundaryGap(Number[] boundaryGap);

    public TimeSingleAxis setBoundaryGap(String[] boundaryGap);

    public TimeSingleAxis setSplitNumber(Number splitNumber);

    public TimeSingleAxis setInterval(Number interval);

    public TimeSingleAxis setMinInterval(Number minInterval);

    public TimeSingleAxis setMaxInterval(Number maxInterval);

    // More ...
}
```

## LogSingleAxis

```java
public class LogSingleAxis implements LogSingleAxisOption {
    public LogSingleAxis setBoundaryGap(Number[] boundaryGap);

    public LogSingleAxis setBoundaryGap(String[] boundaryGap);

    public LogSingleAxis setSplitNumber(Number splitNumber);

    public LogSingleAxis setInterval(Number interval);

    public LogSingleAxis setMinInterval(Number minInterval);

    public LogSingleAxis setMaxInterval(Number maxInterval);

    public LogSingleAxis setLogBase(Number logBase);

    // More ...
}
```
