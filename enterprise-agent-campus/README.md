# 企业 Agent：产品形态与场景选择

面向大一与研一新生的 45 分钟 Reveal.js 双语讲座。新版先讲清工作怎么发生，再解释六种 Agent 产品分别适合哪些企业场景。

## 演示入口

- 中文：`index.html`
- English: `index_en.html`
- 讲者模式：按 `S`
- 总览：按 `Esc`
- PDF：URL 后添加 `?print-pdf`

从仓库根目录运行 `python3 -m http.server 8000`，访问 `http://localhost:8000/enterprise-agent-campus/`。

## 内容主线

1. 先弄清工作怎么发生，再决定 Agent 应该做成什么产品。
2. 用 Entry、Object、Delivery、Rhythm 四问从场景反推产品。
3. 六种主形态：Embedded Copilot、Expert Workbench、Service Agent、Process Agent、Monitoring Agent、Analyst Agent。
4. Multi-Agent 通常是这些产品内部的专业分工，不是第七个聊天入口。
5. 用场景矩阵对齐工作单元、产品形态、典型场景和价值指标。
6. 用同一个退款率问题比较 BI Copilot、Analyst Agent 和 Refund Monitor。

## 时间分配

- `f01`–`f15`：30:00，产品形态框架。
- `f16`–`f19`：10:00，同一能力的三种产品化方式。
- `f20`：4:30，Q&A。
- `f21`：0:30，Thank You 与联系方式。

## 文件结构

- `index.html`：中文 21 页。
- `index_en.html`：英文等义 21 页。
- `styles.css`：基础 1920×1080 视觉与组件。
- `editorial.css`：参考仓库双语索引页重构的编辑式网格与页面分布。
- `editorial-zh.css`：中文标题断句、字级和页面间距的独立校准层。
- `source-map.md`：分类逻辑、逐页依据、公开来源和图片版权。
- `assets/`：本地化 Unsplash 图片。
- `qa/`：中英文 contact sheet。

## 视觉原则

- 沿用仓库双语索引页的编辑系统：3px 顶线、52px 白色顶栏、43/57 主分栏、细分隔线、单色正文和蓝色索引。
- 页面先建立左→右或上→下的唯一阅读路径；标题负责结论，右侧或下方只放支持判断的产品界面、流程或证据。
- 不使用圆角卡片、悬浮阴影和等权矩阵作为默认容器；页面结构由留白、网格、细线、序号和字体层级完成。
- 中文版按中文字符密度单独控制断句与垂直节奏，不用英文自然换行高度驱动版面。
- 一页一个产品判断；每种形态使用不同视觉隐喻，不用卡片矩阵重复铺陈。
- Copilot 使用 sidecar，Workbench 使用项目画布，Service 使用 outcome 波形，Process 使用 case 管线，Monitoring 使用雷达，Analyst 使用探索树。
- Dify Blue 表示主产品路径，绿色表示交付结果，琥珀表示流程或事件，红色表示异常信号。
- 图片用于封面、产品地图、多 Agent 协作、案例转场和结尾；内容层统一加高对比遮罩，正文仍保持清晰的暖白 / 深蓝阅读面。
- 氛围图以建筑秩序、协作现场和结构光影为主，不使用机器人、人形 AI 或廉价科技蓝；全部本地化并在 `source-map.md` 记录作者、原始链接与裁切方式。
- 打印和减少动态效果模式完整呈现所有 fragment。

版式参考：[Dify X bilingual index](../index.html)。讲座复用其视觉语法，但不复制首页的内容结构。

## 后续研究接入

新增材料优先回答：

1. 最小工作单元是什么？
2. 用户会在哪里遇到它？
3. 用户最后要拿到什么？
4. 这项工作是随用随开、按项目推进、由请求或事件触发，还是按经营周期反复发生？
5. 最合理的价值指标是什么？

不要把新的案例恢复成行业清单；优先把它放入六种产品形态之一。完整依据见 `source-map.md`。
