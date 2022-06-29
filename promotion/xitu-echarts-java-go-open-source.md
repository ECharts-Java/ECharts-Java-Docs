发表于稀土掘金/知乎

---
theme: github
---                                        
<div align="center">
    <img src="https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/9eb1c57eff6742bfa7ba4a834271b4f5~tplv-k3u1fbpfcp-watermark.image?" alt="logo" width=150 height=150 />
    <br>
    <em>ECharts Java</em>
</div>
数据可视化库

由百度开发的大名鼎鼎的 [Apache ECharts](https://echarts.apache.org/en/index.html) 想必是当下最流行的数据可视化库之一，其支持的丰富的图表类型、炫酷的动画效果、以及简单易上手的代码，让人很难不心动。但对于广大的Java开发者而言，想要在后端支持Apache ECharts却是个幸福的难题——虽然Apache ECharts功能的强大让人十分眼馋，但是它本身采用TypeScript编写，后端没法直接使用。稍微了解ECharts一些的小伙伴可能知道，ECharts主要的参数是Option对象，该对象存储了所有和可视化相关的数据、图表类型和交互方法。那么在一些前后端不分离的场景下，怎么用Java构造Option对象呢？[ECharts Java](https://github.com/ECharts-Java/ECharts-Java)帮你解决了这个问题。

这里有人可能会说，现在都是前后端分离的时代了，为什么还要解决这个问题呢？诚然，前后端分离逐渐成为大势所趋，但无可否认，前后端不分离的需求也仍然大量存在。或许是旧的系统仍需要在后端支持数据可视化的渲染，或许是学生的学期项目的硬性要求，或许是一些后端开发者对前端语言不是很熟悉......如果你在github里搜索“ECharts Java”，排名第一的library拥有1k的star，其需求量可见一斑。但是很可惜，它仅支持2.x/3.x版本的Apache ECharts，而现在ECharts已经更新到了5.x版本。为了填补当下支持最新版本的ECharts的Java类库的空白，我们的[ECharts Java](https://github.com/ECharts-Java/ECharts-Java)诞生了。



### ✨安装
Maven项目
```xml
<dependency> 
    <groupId>org.icepear.echarts</groupId> 
    <artifactId>echarts-java</artifactId> 
    <version>1.0.3</version> 
</dependency>
```
Gradle项目

```xml
implementation 'org.icepear.echarts:echarts-java:1.0.3'
```

### 🌠特性
-   简单、整洁、高度组织化的 API 接口，支持链式调用
-   完整保存 Apache ECharts 的功能
-   快速集成至当前流行的 Web 框架
-   灵活的导出格式，支持 HTML、PNG 和 JSON
-   完整、详细的文档和示例库


### 🔭 使用

简简单单几行可以生成一个交互性很强的动态柱形图（还可以一键下载哦）
![get-started-bar-chart-java-codes.png](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/c0972a992870445ebb9cb851d699b52b~tplv-k3u1fbpfcp-watermark.image?)
生成的index.html如下，
![multibar-render.gif](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/36d799c7712d4e69b685e362ba05972a~tplv-k3u1fbpfcp-watermark.image?)






如果想生成JSON格式的Option对象怎么办呢？也只需要几行的功夫！
![get-started-option-json-java-codes.png](https://p1-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/d4ff8ba42280420eae6ef094deaeba0b~tplv-k3u1fbpfcp-watermark.image?)
生成的表示Option的JSON文件像这样，
![get-started-option-json.png](https://p9-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/340fb25486e545fa8f700029acb2bd46~tplv-k3u1fbpfcp-watermark.image?)

你以为这样就完了？NoNoNo，我们深知后端开发者的不容易，把ECharts Java和一些流行的后端框架像SpringBoot等巧妙地结合了起来。

![line-renderHtml.gif](https://p6-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/021f1291fabc44908b23f6c2248a4231~tplv-k3u1fbpfcp-watermark.image?)

更多使用指南请参阅我们的[文档](https://echarts.icepear.org/#/zh-cn/)和[代码仓库](https://github.com/incandescentxxc/ECharts-Java-Examples)。

### 🎇 Demo
![stacked-area.jpg](https://p6-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/2730dc869ce8425797f4a880f84e28db~tplv-k3u1fbpfcp-watermark.image?)

![stacked-line.jpg](https://p1-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/edc534e03dd446d5a784bfac04d45469~tplv-k3u1fbpfcp-watermark.image?)

![animation-gauge.jpg](https://p1-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/b14f99283c7c422ab3e26b86334c366e~tplv-k3u1fbpfcp-watermark.image?)

![basic-boxplot.jpg](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/4b5fa39b75e14611ab7ad175779b4f70~tplv-k3u1fbpfcp-watermark.image?)

![basic-candlestick.jpg](https://p9-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/77113a89904d4133a2bfaaa8514093ba~tplv-k3u1fbpfcp-watermark.image?)

![basic-funnel.jpg](https://p1-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/4fc29d072847485fa5668cb472baa9d0~tplv-k3u1fbpfcp-watermark.image?)

![basic-heatmap.jpg](https://p1-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/86af6f3fd37f4f418f6a7e0d5528aebd~tplv-k3u1fbpfcp-watermark.image?)

![basic-parallel.jpg](https://p9-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/6948c36467804fd08f87e19ed56c643d~tplv-k3u1fbpfcp-watermark.image?)

![basic-polar-line.jpg](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/26a796d1078a451a9d20eb906142f8d1~tplv-k3u1fbpfcp-watermark.image?)

![basic-polar-scatter.jpg](https://p1-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/a693a2fdaca7442b8f6c3417a5e6ddcc~tplv-k3u1fbpfcp-watermark.image?)

![basic-radar.jpg](https://p9-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/8292cb6f8de141729c7b0aedd5fc8372~tplv-k3u1fbpfcp-watermark.image?)

![basic-rose.jpg](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/f0003aefd6264342913b790f617d0c1b~tplv-k3u1fbpfcp-watermark.image?)

![basic-sankey.jpg](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/d8f3624e3bf041aaa9392cea46f0102c~tplv-k3u1fbpfcp-watermark.image?)

![basic-scatter.jpg](https://p9-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/769bfa8f28684f1081446d7efed1cf0d~tplv-k3u1fbpfcp-watermark.image?)

![basic-sunburst.jpg](https://p6-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/d83744c3e18d44258bfe2c47cca2f522~tplv-k3u1fbpfcp-watermark.image?)

![basic-theme-river.jpg](https://p9-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/9e88397515d64cf5963c26e5232c3d98~tplv-k3u1fbpfcp-watermark.image?)

![circular-layout-graph.jpg](https://p9-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/d8d02d5a7c8142bb83c7fb28ddf1b627~tplv-k3u1fbpfcp-watermark.image?)

![horizontal-stacked-bar.jpg](https://p6-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/12b1faf2573f4afa92dc2b5c03501e04~tplv-k3u1fbpfcp-watermark.image?)

![hide-overlapped-label-graph.jpg](https://p1-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/5cefde7ee49340f3bf1fda627207de2a~tplv-k3u1fbpfcp-watermark.image?)

![multiple-series-bar.jpg](https://p9-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/978099197c8c479ba4042b15267c87c3~tplv-k3u1fbpfcp-watermark.image?)

![nested-pie.jpg](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/a7b0dbd14e2a484abc14b01955693120~tplv-k3u1fbpfcp-watermark.image?)



## 💌 彩蛋

- 本项目灵感来源于[卡耐基梅隆大学](https://www.cmu.edu/)的课程，[Principles of Software Construction Objects, Design, and Concurrency](https://cmu-17-214.github.io/f2021/)。我们在此真诚地感谢 [Christian](https://www.cs.cmu.edu/~ckaestne/) 和 [Vincent](https://vhellendoorn.github.io/) 在 2021 秋天教授的这门课程。
- 在2022春天教授的该课程里，作者[@incandescentxxc](https://github.com/incandescentxxc)也作为助教，将该库作为推荐可视化库融入到课程的一个作业里，超过30人使用了该库，ECharts Java也受到大家一致的好评。
- 本项目同样也受到 [pyecharts](https://github.com/pyecharts/pyecharts) 和 [go-echarts](https://github.com/go-echarts/go-echarts) 的启发。

## 💡 作者

- [@IcePear-Jzx](https://github.com/IcePear-Jzx)
- [@incandescentxxc](https://github.com/incandescentxxc)

欢迎大家使用和提任何有关的改进建议！最后，别忘了给我们在Github上给该项目点一个star哟！



