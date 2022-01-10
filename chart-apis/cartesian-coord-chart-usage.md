### addXAxis()

The x axis in cartesian (rectangular) coordinate. Usually, a single chart can place at most 2 x axes, one at the bottom and the other at the top.

```java
public T addXAxis();

public T addXAxis(String name);

public T addXAxis(String[] data);

public T addXAxis(String name, String[] data);

public T addXAxis(AxisOption xAxis);
```

?> `T` represents any chart type that extends `CartesianCoordChart` (e.g., `Line`, `Bar`). This is used to support method chaining.

`AxisOption` is implemented by `ValueAxis`, `CategoryAxis`, `TimeAxis`, and `LogAxis`.

For more APIs of `AxisOption`, please refer to [AxisOption](component-apis/axis-option).

### addYAxis()

The y axis in cartesian (rectangular) coordinate. Usually, a single chart can place at most 2 y axes, one on the left and the other on the right.

```java
public T addYAxis();

public T addYAxis(String name);

public T addYAxis(String[] data);

public T addYAxis(String name, String[] data);

public T addYAxis(AxisOption yAxis);
```

?> `T` represents any chart type that extends `CartesianCoordChart` (e.g., `Line`, `Bar`). This is used to support method chaining.

`AxisOption` is implemented by `ValueAxis`, `CategoryAxis`, `TimeAxis`, and `LogAxis`.

For more APIs of `AxisOption`, please refer to [AxisOption](component-apis/axis-option).