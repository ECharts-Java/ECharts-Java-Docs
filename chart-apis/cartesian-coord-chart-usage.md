### addXAxis()

The x axis in cartesian (rectangular) coordinate. Usually, a single chart can place at most 2 x axes, one at the bottom and the other at the top.

```java
public Chart addXAxis();

public Chart addXAxis(String name);

public Chart addXAxis(String[] data);

public Chart addXAxis(String name, String[] data);

public Chart addXAxis(AxisOption xAxis);
```

`AxisOption` is implemented by `ValueAxis`, `CategoryAxis`, `TimeAxis`, and `LogAxis`.

For more APIs of `AxisOption`, please refer to [AxisOption](component-apis/axis-option).

### addYAxis()

The y axis in cartesian (rectangular) coordinate. Usually, a single chart can place at most 2 y axes, one on the left and the other on the right.

```java
public Chart addYAxis();

public Chart addYAxis(String name);

public Chart addYAxis(String[] data);

public Chart addYAxis(String name, String[] data);

public Chart addYAxis(AxisOption yAxis);
```

`AxisOption` is implemented by `ValueAxis`, `CategoryAxis`, `TimeAxis`, and `LogAxis`.

For more APIs of `AxisOption`, please refer to [AxisOption](component-apis/axis-option).
