```java
Gauge gauge = new Gauge()
        .setTooltip("item")
        .addSeries(new GaugeSeries().setName("Pressure")
                .setProgress(new GaugeProgress().setShow(true))
                .setDetail(new GaugeDetail().setValueAnimation(true))
                .setData(new GaugeDataItem[] { new GaugeDataItem().setValue(50).setName("SCORE") }));
```
