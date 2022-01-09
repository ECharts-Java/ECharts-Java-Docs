## 设计理念

ECharts Java是一款基于[Apache ECharts](https://echarts.apache.org/en/index.html)的，简易但全面的数据可视化库。

论简易性，ECharts Java重新设计了一系列绘图有关的接口，使得绘图过程更加符合直觉。同时，由于Apache ECharts的接口过于复杂和繁琐，我们在ECharts Java的图表API中简化了部分原本的接口设计。

论全面，ECharts Java保留了Apache ECharts”一切皆Option“的设计理念。除了重新设计的图表APIs以外，我们还保留了自定义Option对象的方法。用户可以从零开始，按照ECharts的Option文档，自定义任何ECharts支持的Option。除此以外，我们还使用链式方法调用等方式，使得Java开发者在构建Option的过程中更加方便。

## 特性

- 简单，整洁，高度组织化的API接口，支持链式调用。
- 完整保存Apache ECharts的功能
- 快速集成至当前流行的Web框架
- 灵活的导出格式，支持HTML，PNG和JSON
- 完整、详细的文档和示例库
