# RadarAxis

```java
public class RadarAxis implements RadarOption {
    public RadarAxis setName(String name);

    public RadarAxis setCenter(Number[] center);

    public RadarAxis setCenter(String[] center);

    public RadarAxis setRadius(Number radius);

    public RadarAxis setRadius(Number[] radius);

    public RadarAxis setRadius(String radius);

    public RadarAxis setRadius(String[] radius);

    public RadarAxis setStartAngle(Number startAngle);

    public RadarAxis setShape(String shape);

    public RadarAxis setAxisLine(AxisLineOption axisLine);

    public RadarAxis setAxisTick(AxisTickOption axisTick);

    public RadarAxis setAxisLabel(AxisLabelBaseOption axisLabel);

    public RadarAxis setSplitLine(SplitLineOption splitLine);

    public RadarAxis setSplitArea(SplitAreaOption splitArea);

    public RadarAxis setAxisName(RadarAxisNameOption axisName);

    public RadarAxis setAxisNameGap(Number axisNameGap);

    public RadarAxis setScale(Boolean scale);

    public RadarAxis setSplitNumber(Number splitNumber);

    public RadarAxis setBoundaryGap(Boolean boundaryGap);

    public RadarAxis setBoundaryGap(Number[] boundaryGap);

    public RadarAxis setBoundaryGap(String[] boundaryGap);

    public RadarAxis setIndicator(RadarIndicatorOption[] indicator);

    // More ...
}
```

For more APIs and detailed explanation, please refer to [source code](https://github.com/ECharts-Java/ECharts-Java/blob/master/src/main/java/org/icepear/echarts/components/coord/radar/RadarAxis.java) and [Apache ECharts docs](https://echarts.apache.org/en/option.html#radar).
