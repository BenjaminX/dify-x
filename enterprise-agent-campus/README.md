# 企业 Agent：产品形态与场景选择

面向大一与研一新生的 45 分钟 Reveal.js 双语讲座。新版从“工作形态决定产品形态”出发，解释六种 Agent 产品形态分别适合哪些企业场景。

## 演示入口

- 中文：`index.html`
- English: `index_en.html`
- 讲者模式：按 `S`
- 总览：按 `Esc`
- PDF：URL 后添加 `?print-pdf`

从仓库根目录运行 `python3 -m http.server 8000`，访问 `http://localhost:8000/enterprise-agent-campus/`。

## 内容主线

1. 产品形态跟随工作形态，不跟随自治等级。
2. 用 Entry、Object、Delivery、Rhythm 四问从场景反推产品。
3. 六种主形态：Embedded Copilot、Expert Workbench、Service Agent、Process Agent、Monitoring Agent、Analyst Agent。
4. Multi-Agent 通常是这些产品内部的专业分工，不是第七个聊天入口。
5. 用场景矩阵对齐工作单元、产品形态、典型场景和价值指标。
6. 用同一个退款率问题比较 BI Copilot、Analyst Agent 和 Refund Monitor。

## 时间分配

- `f01`–`f15`：30:00，产品形态框架。
- `f16`–`f19`：10:00，同一能力的三种产品化方式。
- `f20`：5:00，Q&A。

## 文件结构

- `index.html`：中文 20 页。
- `index_en.html`：英文等义 20 页。
- `styles.css`：1920×1080 共享视觉系统。
- `source-map.md`：分类逻辑、逐页依据、公开来源和图片版权。
- `assets/`：本地化 Unsplash 图片。
- `qa/`：中英文 contact sheet。

## 视觉原则

- 一页一个产品判断；每种形态使用不同视觉隐喻，不用卡片矩阵重复铺陈。
- Copilot 使用 sidecar，Workbench 使用项目画布，Service 使用 outcome 波形，Process 使用 case 管线，Monitoring 使用雷达，Analyst 使用探索树。
- Dify Blue 表示主产品路径，绿色表示交付结果，琥珀表示流程或事件，红色表示异常信号。
- 图片仅用于封面、案例转场和结尾；正文保持暖白高对比。
- 打印和减少动态效果模式完整呈现所有 fragment。

## 后续研究接入

新增材料优先回答：

1. 最小工作单元是什么？
2. 用户从哪里遇见产品？
3. 用户最终拿走什么？
4. 场景是按需、按项目、按请求、按 case、按事件还是按经营周期重复？
5. 最合理的价值指标是什么？

不要把新的案例恢复成行业清单；优先把它放入六种产品形态之一。完整依据见 `source-map.md`。
