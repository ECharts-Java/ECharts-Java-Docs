## setCoordinateSystem()

```java
public SeriesOption setCoordinateSystem(String coordinateSystem);
```

Valid values of `coordinateSystem`:
- `"cartesian2d"`: two-dimensional rectangular coordinate (also known as Cartesian coordinate) (default)
- `"polar"`: polar coordinate
- `"geo"`: geographic coordinate (TODO: not supported)

## setData()

```java
public SeriesOption setData(ScatterDataItemOption[] data);

public SeriesOption setData(Object[] data);

public SeriesOption setData(Object[][] data);
```

`data` is an array of data points. `Object` can be `String` or `Number` or a mixure of `String` and `Number`.

TODO: For more APIs of `ScatterDataItemOption`, please refer to [ScatterDataItemOption](component-apis/scatter-data-item-option).
