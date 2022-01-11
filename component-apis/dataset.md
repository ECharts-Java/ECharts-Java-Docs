# Dataset

```java
public class Dataset implements DatasetOption {
    public Dataset setId(Number id);

    public Dataset setId(String id);

    public Dataset setSource(Map<String, Object>[] source);

    public Dataset setSource(Map<String, Object[]> source);

    public Dataset setSource(Object[] source);

    public Dataset setSource(Object[][] source);

    public Dataset setSource(Object[][][] source);

    public Dataset setSource(OptionDataItemObject[] source);

    public Dataset setFromDatasetIndex(Number fromDatasetIndex);

    public Dataset setFromDatasetId(String fromDatasetId);

    public Dataset setTransform(DataTransformOption transform);

    public Dataset setTransform(DataTransformOption[] transform);

    public Dataset setFromTransformResult(Number fromTransformResult);

    // More ...
}
```

For more APIs and detailed explanation, please refer to [source code](https://github.com/ECharts-Java/ECharts-Java/blob/master/src/main/java/org/icepear/echarts/components/dataset/Dataset.java) and [Apache ECharts docs](https://echarts.apache.org/en/option.html#dataset).
