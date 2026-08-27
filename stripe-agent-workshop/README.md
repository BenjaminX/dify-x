# Dify × Stripe Workshop：From Scenario to System

这是一套中英双语、45 分钟、面向产品与工程混合听众的 Workshop：先从工作单元、产品形态、交付物和使用节奏判断 Agent 应该成为怎样的产品，再用 Dify Workflow Generator 拆解如何把一句自然语言需求变成可检查的计划、可运行的图和可增量修改的系统。

中文版不是英文版的逐字翻译，而是按中文演讲习惯重新断句、压缩标题和调整信息密度；两种语言共享同一套页序、证据、计时和 `data-slide-id`。

## Title

**From Scenario to System**<br>
**Designing Enterprise Agents That Actually Run**

> Choose the product form. Generate the workflow. Engineer the guarantees.

## Topic Introduction

Most enterprise-agent projects start with model capability. This session starts with the work: where users meet the system, what object persists, what outcome matters, and how often the work repeats. We then follow Dify Workflow Generator from a one-sentence request to a plan, a runnable graph, and an incremental refinement. Along the way, we unpack the production architecture behind reliable structured generation—planning, focused node building, dynamic context injection, deterministic assembly, validation, and parallel execution—and show how product form and engineering guarantees must reinforce each other.

## Audience Takeaways

- Select an agent product form from the work unit, entry point, deliverable, and usage rhythm.
- Turn a vague agent idea into a product brief and workflow topology.
- Understand the responsibility split across Planner, Node Builders, Assembler, and Validator.
- Decide what belongs to the model and what must remain deterministic.
- Recognize production failure modes involving tools, graph structure, validation, refinement, and latency.

## 结构与计时（45 分钟）

| 章节 | 页码 | 内容 | 时间 |
|---|---:|---|---:|
| Choose the Product | 01–06 | 工作主张、工作单元、六种产品形态、四个问题、Workflow 适用条件 | 12:00 |
| Sentence to Graph | 07–10 | 静态教学任务、Prompt → Plan → Graph → Refine | 7:00 |
| Engineer the Guarantees | 11–18 | 结构化输出、流水线、v1、Planner、Builder、工具上下文、Validator、并行构建 | 17:30 |
| Return to the Product | 19–20 | Dify packaging 与最终工程原则 | 3:30 |
| Q&A + Thank You | 21–22 | 讨论题、联系方式、图片署名 | 5:00 |

总计：40:00 主讲 + 4:30 Q&A + 0:30 Thank You。

## 文件与版本边界

- `index.html`：22 页中文版演示。
- `index_en.html`：22 页英文版演示。
- `editorial-en.css`：中英文共享的编辑式网格与组件基础。
- `editorial-zh.css`：只作用于中文版的断句、字号、间距与文字方向校准。
- `source-map.md`：工程来源、证据边界、图片版权和计时映射。
- `qa/contact-sheet-en.png`：22 页完整展开后的 4 × 6 视觉巡检图。
- `qa/contact-sheet-zh.png`：中文版 22 页完整展开后的 4 × 6 视觉巡检图。
- `styles.css`：旧版遗留样式，不再由新中英文演示加载。
- `starter/stripe-billing`：保留已有 Sandbox skill，不参与本次通用 Workflow 静态推演。

## 演示与证据边界

- 第 07–10 页为无网络依赖的通用静态教学推演，不是客户案例或产品录屏。
- Dify × Stripe 仅表示活动联合品牌，不表示 Stripe 使用 Dify。
- PR 中的工程数字只说明实现变化，不解释为业务 ROI 或客户效果。
- 背景图来自 Unsplash，作者为 Timothée Duran、Declan Sun 与 Arlind Photography。

## 参考工程来源

- [PR #31944](https://github.com/langgenius/dify/pull/31944) — Workflow Generator 早期实现。
- [PR #32130](https://github.com/langgenius/dify/pull/32130) — Graph postprocessor 与 Validator。
- [PR #38975](https://github.com/langgenius/dify/pull/38975) — 并行 Node Builder。
- [PR #40611](https://github.com/langgenius/dify/pull/40611) — 动态工具注入与工具路由。
