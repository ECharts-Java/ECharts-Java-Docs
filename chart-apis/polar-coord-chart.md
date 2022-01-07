# PolarCoordChart

```java
public abstract class PolarCoordChart<T extends Chart<?, ?>, E extends SeriesOption> extends Chart<T, E> {
    public T setPolarAxis();

    public T setPolarAxis(String[] radius);

    public T setPolarAxis(PolarAxis polarAxis);

    public T setAngleAxis();

    public T setAngleAxis(Number max);

    public T setAngleAxis(String[] categories);

    public T setAngleAxis(AngleAxisOption angleAxis);

    public T setRadiusAxis();

    public T setRadiusAxis(Number max);

    public T setRadiusAxis(String[] categories);

    public T setRadiusAxis(RadiusAxisOption radiusAxis);
}
```
