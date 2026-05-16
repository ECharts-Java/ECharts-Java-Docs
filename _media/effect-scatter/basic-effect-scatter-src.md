```java
EffectScatter chart = new EffectScatter()
        .addXAxis()
        .addYAxis()
        .addSeries(new EffectScatterSeries()
                .setSymbolSize(20)
                .setShowEffectOn("render")
                .setRippleEffect(new RippleEffect().setScale(2.5).setBrushType("stroke"))
                .setData(new Number[][] {
                        { 10, 80 }, { 20, 50 }, { 30, 70 }, { 40, 30 }, { 50, 90 }
                }));
```
