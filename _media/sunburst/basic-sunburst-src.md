```java
Sunburst sunburst = new Sunburst()
        .setTooltip("item")
        .addSeries(new SunburstSeries()
                .setRadius(new String[] { "0", "90%" })
                .setLabel(new SunburstLabel().setShow(false))
                .setData(new SunburstNodeItem[] {
                        new SunburstNodeItem().setName("Grandpa")
                                .setChildren(new SunburstNodeItem[] {
                                        new SunburstNodeItem().setName("Uncle Leo").setValue(15)
                                                .setChildren(new SunburstNodeItem[] {
                                                        new SunburstNodeItem().setName("Cousin Jack")
                                                                .setValue(2),
                                                        new SunburstNodeItem().setName("Cousin Mary")
                                                                .setValue(5)
                                                                .setChildren(new SunburstNodeItem[] {
                                                                        new SunburstNodeItem()
                                                                                .setName("Jackson").setValue(2)
                                                                }),
                                                        new SunburstNodeItem().setName("Cousin Ben")
                                                                .setValue(4)
                                                }),
                                        new SunburstNodeItem().setName("Father").setValue(10)
                                                .setChildren(new SunburstNodeItem[] {
                                                        new SunburstNodeItem().setName("Me").setValue(5),
                                                        new SunburstNodeItem().setName("Brother Peter")
                                                                .setValue(1)
                                                })
                                }),
                        new SunburstNodeItem().setName("Nancy")
                                .setChildren(new SunburstNodeItem[] {
                                        new SunburstNodeItem().setName("Uncle Nike")
                                                .setChildren(new SunburstNodeItem[] {
                                                        new SunburstNodeItem().setName("Cousin Betty")
                                                                .setValue(1),
                                                        new SunburstNodeItem().setName("Cousin Jenny")
                                                                .setValue(2)
                                                })
                                })
                }));
```
