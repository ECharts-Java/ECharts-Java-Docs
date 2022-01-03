```java
Parallel parallel = new Parallel()
        .addParallelAxis("Price", 0)
        .addParallelAxis("Net Weight", 1)
        .addParallelAxis("Amount", 2)
        .addParallelAxis("Score", 3, new String[] { "Excellent", "Good", "OK", "Bad" })
        .addSeries(new ParallelSeries()
                .setLineStyle(new LineStyle().setWidth(4))
                .setData(new Object[][] {
                        { 12.99, 100, 82, "Good" },
                        { 9.99, 80, 77, "OK" },
                        { 20, 120, 60, "Excellent" }
                }));
```
