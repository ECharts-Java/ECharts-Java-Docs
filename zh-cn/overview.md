# 概述

## 设计理念

ECharts Java 是一款基于 [Apache ECharts](https://echarts.apache.org/en/index.html) 的，简易但全面的数据可视化库。

论简易性，ECharts Java 重新设计了一系列和绘图有关的接口，使得绘图过程更加符合直觉和常理。同时，由于 Apache ECharts 的接口过于复杂和繁琐，我们在 ECharts Java 的图表 API 中简化了部分原本的接口设计。

论全面，ECharts Java 保留了 Apache ECharts “一切皆 Option” 的设计理念。因此，除了重新设计的图表 API 以外，我们还保留了自定义 Option 对象的方法。用户可以从零开始，按照 ECharts 的 Option 文档，自定义任何ECharts 支持的 Option。除此以外，我们还使用链式方法调用等方式，使得 Java 开发者在构建 Option 的过程中更加方便。

## 特性

- 简单、整洁、高度组织化的 API 接口，支持链式调用
- 完整保存 Apache ECharts 的功能
- 快速集成至当前流行的 Web 框架
- 灵活的导出格式，支持 HTML、PNG 和 JSON
- 完整、详细的文档和示例库
