### setPolarAxis()

A chart with polar coordinate must have one `PolarAxis`.

```java
public Chart setPolarAxis();

public Chart setPolarAxis(String[] radius);

public Chart setPolarAxis(PolarAxis polarAxis);
```

For more APIs of `PolarAxis`, please refer to [PolarAxis](component-apis/polar-axis).

### setAngleAxis()

The angle axis in Polar Coordinate.

```java
public Chart setAngleAxis();

public Chart setAngleAxis(Number max);

public Chart setAngleAxis(String[] categories);

public Chart setAngleAxis(AngleAxisOption angleAxis);
```

`AngleAxisOption` is implemented by `ValueAngleAxis`, `CategoryAngleAxis`, `TimeAngleAxis`, and `LogAngleAxis`.

For more APIs of `AngleAxisOption`, please refer to [AngleAxisOption](component-apis/angle-axis-option).

### setRadiusAxis()

The radial axis of polar coordinate.

```java
public Chart setRadiusAxis();

public Chart setRadiusAxis(Number max);

public Chart setRadiusAxis(String[] categories);

public Chart setRadiusAxis(RadiusAxisOption radiusAxis);
```

`RadiusAxisOption` is implemented by `ValueRadiusAxis`, `CategoryRadiusAxis`, `TimeRadiusAxis`, and `LogRadiusAxis`.

For more APIs of `RadiusAxisOption`, please refer to [RadiusAxisOption](component-apis/radius-axis-option).
