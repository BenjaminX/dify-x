# Research & Evidence Map

本文件记录 20 页讲座的研究依据、证据边界、旧页合并关系与图片版权。它是事实索引，不是对来源方结果的独立审计。

## Evidence labels

| 标签 | 含义 | 使用规则 |
| --- | --- | --- |
| `A` | 实名企业案例，原始来源披露明确结果指标 | 可说明生产成熟度；数字旁必须注明“来源方披露、未独立审计” |
| `B` | 实名企业或官方工程实践，但缺少可比较结果指标 | 只说明流程、架构或技术可行性，不推导生产 ROI |
| `Internal Signal` | 内部访谈、内部需求研究或其综合信号 | 说明需求和约束，不当作经过审计的生产结果 |

研究综合判断不强行附加证据徽章。旧版的 `REPORT` 徽章已经移除。

## Primary research input

- 文件：`/Users/banana/Desktop/enterprise_agent_scenarios_research.md`
- 标题：企业 Agent 场景案例库
- 范围：企业内部及面向客户的可控 Agentic Workflow
- 公开资料检索截止：2026-08-26

## Current 20-slide mapping

| Slide ID | 内容 | 主要依据 | 证据边界 |
| --- | --- | --- | --- |
| `s01-cover` | 标题、讲座定位 | 讲座设计 | 讲者、学校、日期为占位符 |
| `s02-opening-thesis` | 从回答到推进 | 报告执行摘要、§1.1 | 是讲座核心判断，不宣称行业唯一标准 |
| `s03-three-questions` | 场景、系统、停止条件 | 讲座结构 | 30/10/5 为建议现场节奏 |
| `s04-agent-threshold` | 企业 Agent 工作定义 | 报告 §1.1 | 工作口径，不是认证标准 |
| `s05-automation-spectrum` | Q&amp;A 到 Multi-Agent | 报告执行摘要、§4 | 概念光谱，不是成熟度等级 |
| `s06-system-anatomy` | 目标、上下文、工具、状态、控制、证据 | 报告 §1、§4 | 教学模型，不对应产品菜单 |
| `s07-scenario-atlas` | 八类场景的三种流程模式 | 报告 §2–§3 | 公开成熟度为定性判断，不是产品分数 |
| `s08-start-stop-gates` | 高频、数据、SOP、验证、回退 | 报告 §5–§6 | 未通过表示暂不放权，不代表永久不可用 |
| `s09-contract-case` | 合同结构化与专家验证 | OpenAI 原始案例 | `A`；来源方披露；不暗示使用 Dify |
| `s10-service-case` | 多语种服务、受限动作与转人工 | AWS / Ryanair 原始案例 | `A`；来源方披露；指标不可跨案例比较 |
| `s11-dify-system` | Models、Knowledge、Tools、Workflow、Agent、API、Logs | Dify 实现主线 | 说明系统位置，不是功能排名 |
| `s12-boundary-flow` | Workflow 主干、受限 Agent loop、Human gate | 报告 §4–§5 | 推荐架构，不要求所有流程都使用 Agent loop |
| `s13-context-permission` | 语义上下文与动作权限 | 报告 §3.8、§4 | 权限轨道为风险设计示意 |
| `s14-control-perimeter` | 八项企业控制能力 | 报告 §4；内部研究信号 | `Internal Signal`；综合框架，不是成熟度认证 |
| `s15-autonomy-runway` | 三阶段放权 | 报告 §5 | 第三阶段仅覆盖稳定、低风险、可回退动作 |
| `s16-acceptance-summary` | 业务与安全两组验收 | 报告 §5 | 指标类别通用，阈值由业务定义 |
| `s17-data-case` | 退款率异常分析任务 | 报告 §3.8、教学设计 | 合成静态推演，不是真实 Dify 客户案例 |
| `s18-analysis-pipeline` | Dify 数据 Agent 链路 | 报告 §3.8；AWS Dify 工程实践 | `B`；工程参考，无生产 ROI |
| `s19-fault-proof` | 故障路由、上线证据、真实案例边界 | 报告 §4–§6；OpenAI 数据 Agent | `B`；平台规模不等于 Agent 使用量、准确率或 ROI |
| `s20-qa-sources` | 讨论题、联系方式、图片署名 | 讲座设计 | 联系方式为占位符 |

## Old 27 slides → current 20 slides

| 旧页 | 新页 | 合并或变更 |
| --- | --- | --- |
| `s01-cover`–`s07-scenario-atlas` | `s01-cover`–`s07-scenario-atlas` | 保留主题，重构为大字、连续路径和场景交通图 |
| `s08-six-dimensions` | `s07-scenario-atlas`、`s08-start-stop-gates` | 六维比较不再制作示意分数条；判断方法进入场景地图和讲者备注 |
| `s09-start-here` + `s10-dont-start-here` | `s08-start-stop-gates` | 合并为五道通过/停止阶段门 |
| `s11-production-snapshots` | `s09-contract-case` + `s10-service-case` | 拆为两张编辑叙事案例页，避免双卡并列 |
| `s12-dify-system` | `s11-dify-system` | 七层卡片改为三层系统剖面 |
| `s13-workflow-agent-boundary` | `s12-boundary-flow` | 双面板改为单一运行路径 |
| `s14-context-layers` + `s15-permission-ladder` | `s13-context-permission` | 合并为上下文与权限双轨 |
| `s16-eight-controls` | `s14-control-perimeter` | 八卡矩阵改为控制边界 |
| `s17-three-stage-autonomy` | `s15-autonomy-runway` | 三卡改为放权跑道 |
| `s18-two-scoreboards` + `s19-main-summary` | `s16-acceptance-summary` | 双组指标和主讲总结合并 |
| `s20-case-brief` + `s21-not-just-text-to-sql` | `s17-data-case` + `s18-analysis-pipeline` | 任务开场独立；SQL 局限进入端到端管线 |
| `s22-dify-data-agent-architecture` | `s18-analysis-pipeline` | 七卡架构改为连续管线 |
| `s23-failure-injection` + `s24-prove-before-launch` + `s25-real-case-boundary` | `s19-fault-proof` | 故障、验收和真实案例口径合并为一张异常主流程 |
| `s26-qa` + `s27-credits` | `s20-qa-sources` | Q&amp;A、联系方式、来源入口和图片署名合并 |

## Public primary sources

### A-level named cases

- OpenAI, [Turning contracts into searchable data at OpenAI](https://openai.com/index/openai-contract-data-agent/), 2025-09-29. Used on `s09-contract-case`.
- AWS, [Transforming customer service with agentic AI and Amazon Nova at Ryanair](https://aws.amazon.com/solutions/case-studies/innovators/ryanair-agentic-ai/). Used on `s10-service-case`.

### B-level engineering practices

- AWS China, [在亚马逊云科技环境上基于 Dify Agent 快速部署 text2SQL 智能数据分析助手](https://aws.amazon.com/cn/blogs/china/quickly-deploy-text2sql-intelligent-data-analysis-assistant-based-on-dify-agent-on-aws/), 2025-03-21. Used on `s18-analysis-pipeline`.
- AWS China, [集成 Dify 和 AWS Service 实现更具灵活性的翻译工作流](https://aws.amazon.com/cn/blogs/china/integrate-dify-and-aws-services-to-enable-more-flexible-translation-workflows/), 2024-09-18. Supporting orchestration reference.
- OpenAI, [Inside OpenAI's in-house data agent](https://openai.com/index/inside-our-in-house-data-agent/), 2026-01-29. Used on `s19-fault-proof`.

## Unsplash assets

| Slide | Local asset | Author and original link | Crop / treatment |
| --- | --- | --- | --- |
| `s01-cover` | `assets/atmos-silk-ruido98.jpg` | [Ruido 98](https://unsplash.com/photos/SytlpdDJ1lk) | Full bleed; center-right crop; dark left gradient |
| `s07-scenario-atlas` | `assets/atmos-prism-darkhan-basshybayev.jpg` | [Darkhan Basshybayev](https://unsplash.com/photos/o6uvtosEZeo) | Full bleed at low opacity beneath the transit map |
| `s17-data-case` | `assets/atmos-indigo-richard-horvath.jpg` | [Richard Horvath](https://unsplash.com/photos/_nWaeTF6qo0) | Full bleed; dark left gradient |
| `s20-qa-sources` | `assets/atmos-pastel-codioful.jpg` | [Codioful](https://unsplash.com/photos/LeG68PrXA6Y) | Full bleed; dark navy overlay |

`assets/atmos-teal-pawel-czerwinski.jpg` remains localized for future use but is not displayed in the current 20-slide talk.

## Claim-handling rules

1. 保留来源组织、发布日期、任务口径和证据等级。
2. 供应商数字必须与“来源方披露、未独立审计”同时出现。
3. 不把不同企业的准确率、containment、周期或成本合并成统一 ROI。
4. 不把底层平台规模改写为 Agent 使用规模或质量指标。
5. Dify 仅作为实现主线；外部案例不自动成为 Dify 客户案例。
6. 核心结论改变时，同步更新中英文页面、讲者备注和本文件。
