### setSingleAxis()

An axis with a single dimension. It can be used to display data in one dimension.

```java
public T setSingleAxis(SingleAxisOption singleAxis);
```

?> `T` represents any chart type that extends `SingleCoordChart` (e.g., `ThemeRiver`). This is used to support method chaining.

`SingleAxisOption` is implemented by `ValueSingleAxis`, `CategorySingleAxis`, `TimeSingleAxis`, and `LogSingleAxis`.

For more APIs of `SingleAxisOption`, please refer to [SingleAxisOption](component-apis/single-axis-option).
