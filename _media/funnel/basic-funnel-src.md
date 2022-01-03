```java
Funnel funnel = new Funnel()
        .setTitle("Funnel")
        .setTooltip("item")
        .setLegend(true)
        .addSeries(new FunnelSeries()
                .setLabel(new FunnelLabel().setShow(true).setPosition("inside"))
                .setData(new FunnelDataItem[] {
                        new FunnelDataItem().setValue(60).setName("Visit"),
                        new FunnelDataItem().setValue(40).setName("Inquiry"),
                        new FunnelDataItem().setValue(20).setName("Order"),
                        new FunnelDataItem().setValue(80).setName("Click"),
                        new FunnelDataItem().setValue(100).setName("Show")
                }));
```
