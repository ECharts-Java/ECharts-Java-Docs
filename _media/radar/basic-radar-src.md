```java
Radar radar = new Radar()
        .setTitle("Basic Radar")
        .setLegend(true)
        .setRadarAxis(new RadarIndicator[] {
                new RadarIndicator().setName("Sales").setMax(6500),
                new RadarIndicator().setName("Administration").setMax(16000),
                new RadarIndicator().setName("Information Technology").setMax(30000),
                new RadarIndicator().setName("Customer Support").setMax(38000),
                new RadarIndicator().setName("Development").setMax(52000),
                new RadarIndicator().setName("Marketing").setMax(25000) })
        .addSeries(new RadarDataItem[] {
                new RadarDataItem()
                        .setValue(new Number[] { 4200, 3000, 20000, 35000, 50000, 18000 })
                        .setName("Allocated Budget"),
                new RadarDataItem()
                        .setValue(new Number[] { 5000, 14000, 28000, 26000, 42000, 21000 })
                        .setName("Actual Spending") });
```
