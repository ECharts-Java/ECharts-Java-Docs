### setPolarAxis()

A chart with polar coordinate must have one `PolarAxis`.

```java
public T setPolarAxis();

public T setPolarAxis(String[] radius);

public T setPolarAxis(PolarAxis polarAxis);
```

?> `T` represents any chart type that extends `PolarCoordChart` (e.g., `PolarLine`, `PolarBar`). This is used to support method chaining.

For more APIs of `PolarAxis`, please refer to [PolarAxis](component-apis/polar-axis).

### setAngleAxis()

The angle axis in Polar Coordinate.

```java
public T setAngleAxis();

public T setAngleAxis(Number max);

public T setAngleAxis(String[] categories);

public T setAngleAxis(AngleAxisOption angleAxis);
```

?> `T` represents any chart type that extends `PolarCoordChart` (e.g., `PolarLine`, `PolarBar`). This is used to support method chaining.

`AngleAxisOption` is implemented by `ValueAngleAxis`, `CategoryAngleAxis`, `TimeAngleAxis`, and `LogAngleAxis`.

For more APIs of `AngleAxisOption`, please refer to [AngleAxisOption](component-apis/angle-axis-option).

### setRadiusAxis()

The radial axis of polar coordinate.

```java
public T setRadiusAxis();

public T setRadiusAxis(Number max);

public T setRadiusAxis(String[] categories);

public T setRadiusAxis(RadiusAxisOption radiusAxis);
```

?> `T` represents any chart type that extends `PolarCoordChart` (e.g., `PolarLine`, `PolarBar`). This is used to support method chaining.

`RadiusAxisOption` is implemented by `ValueRadiusAxis`, `CategoryRadiusAxis`, `TimeRadiusAxis`, and `LogRadiusAxis`.

For more APIs of `RadiusAxisOption`, please refer to [RadiusAxisOption](component-apis/radius-axis-option).
