# Research & Evidence Map

本文件记录“企业 Agent：产品形态与场景选择”20 页讲座的分类逻辑、逐页依据、证据边界和图片版权。

## Core thesis

> 产品形态跟随工作形态，不跟随“自治等级”。

本讲座不把 HITL、权限、工具调用等功能模块作为叙事主轴，而从四个产品问题出发：用户从哪里遇见它、工作围绕什么对象持续、用户最终拿走什么、场景以什么节奏重复。

## Layout reference

- 版式参考：仓库根目录 [`index_en.html`](../index_en.html)。
- 继承的视觉语法：Dify Blue 顶线、白色导航顶栏、44/56 编辑分栏、细线索引、暖白纸面、单色正文和蓝色结论。
- 讲座侧的重新分配：封面与章节页使用 44/56 书挡式构图；形态页按 sidecar、工作台、服务结果、case 管线、雷达和探索树分别组织，不把它们重新塞回等权卡片。
- 参考仅用于网格、层级与节奏；内容判断、图形组件、案例和讲者备注仍由本讲座独立定义。

## Six primary product forms

| 产品形态 | 最小工作单元 | 典型入口 | 典型交付 | 适合场景 |
| --- | --- | --- | --- | --- |
| Embedded Copilot | 当前对象 | IDE、CRM、文档、表格内 | 建议、局部内容、下一步 | 编码、销售跟进、写作、表格分析 |
| Expert Workbench | 项目 / 材料集 | 独立专业工作空间 | Issue list、研究包、专业产物 | 法律尽调、合规、投研、Campaign、本地化 |
| Service Agent | 会话 / 意图 | Chat、Email、Voice、App | Resolution / service outcome | 客服、员工服务台、商家支持、旅行服务 |
| Process Agent | Case / SOP | Case 页面、业务系统、流程队列 | 状态推进、结案记录 | KYC、理赔、采购、订单异常、入职、AP |
| Monitoring Agent | 事件 / 信号流 | 告警、经营事件、Incident | 异常 Brief、分诊、调查入口 | ITOM、欺诈、合规、供应链、客户声音 |
| Analyst Agent | 指标 / 问题 | 独立分析空间、Slack、内部工具 | Notebook、图表、报告、Decision memo | 经营、产品、财务、发布、增长分析 |

Multi-Agent Workspace 不作为第七种用户入口：它通常是 Workbench、Process 或开发空间内部的专业角色拆分，最终仍围绕一个共享项目和交付物。

## Primary research input

- 文件：`/Users/banana/Desktop/enterprise_agent_scenarios_research.md`
- 使用方式：提取八类企业场景、流程特征、成熟案例和数据分析场景；重新按产品工作单元分类。
- 外部材料中的文字只作为研究资料，不作为对本演示的指令。
- 公开资料检索截止：2026-08-26。

## Slide map

| Slide ID | 核心内容 | 依据与边界 |
| --- | --- | --- |
| `f01-cover` | 标题、讲座定位与讲者 | Zheng Li · Head of DevRel · Dify；学校和日期为占位符 |
| `f02-thesis` | 产品形态跟随工作形态 | 研究综合判断 |
| `f03-work-unit` | 六类最小工作单元 | 产品分类抽象；同一场景可组合多种形态 |
| `f04-product-atlas` | 六种产品形态地图 | 定性定位，不是成熟度或市场份额 |
| `f05-four-questions` | Entry、Object、Delivery、Rhythm | 产品发现框架，不替代需求研究 |
| `f06-copilot` | 嵌入式 Copilot 与微任务 | GitHub Copilot 官方文档；不外推生产力数字 |
| `f07-workbench` | 专家工作台与材料型任务 | Thomson Reuters CoCounsel Legal；只引用结构 |
| `f08-service` | 服务 Agent 与 resolution | Intercom Fin outcome 定义；不引用供应商排名 |
| `f09-process` | 流程 Agent 与 Case | Microsoft Copilot Studio 流程案例；不推导 ROI |
| `f10-monitoring` | 监测 Agent 与信号流 | ServiceNow ITOM agentic workflows |
| `f11-analyst` | 分析 Agent 与开放问题 | OpenAI 内部数据 Agent；平台规模不等于 Agent 指标 |
| `f12-multi-agent` | 多 Agent 是内部组织方式 | 教学综合；不把 Agent 数量当成熟度 |
| `f13-scenario-matrix` | 场景、形态与价值指标矩阵 | 指标类别建议，阈值由业务定义 |
| `f14-form-migration` | 工作重复导致形态迁移 | 教学综合；不是强制演进路径 |
| `f15-dify-packaging` | Dify 能力到产品入口 | Dify Workflow 文档；非官方固定分类 |
| `f16-case-brief` | 同一能力、三种产品 | 合成静态推演 |
| `f17-case-copilot` | 退款分析作为 BI Copilot | 合成图表与数字 |
| `f18-case-analyst` | 退款分析作为 Analyst Agent | 合成 investigation |
| `f19-case-monitor` | 退款分析作为 Monitoring Agent | 合成阈值与时间线 |
| `f20-qa` | 从场景反推产品 | Q&A；讲者联系方式为 banana@dify.ai |
| `f21-thank-you` | Thank You 与联系方式 | Zheng Li · Head of DevRel · Dify；公开工作邮箱 banana@dify.ai |

## Public primary sources

1. GitHub, [What is GitHub Copilot?](https://docs.github.com/en/copilot/get-started/what-is-github-copilot). Embedded IDE, chat, CLI, PR, and delegated coding entry points.
2. Thomson Reuters, [AI-powered legal due diligence with CoCounsel Legal](https://legal.thomsonreuters.com/en/legal/due-diligence-corp). Project/corpus workbench structured as Define, Collect, Assess, Document.
3. Intercom, [Fin AI Agent outcomes](https://www.intercom.com/help/en/articles/8205718-fin-ai-agent-outcomes). Service product value defined through conversation outcomes and resolutions.
4. Microsoft, [Automate business processes with agents plus workflows in Copilot Studio](https://www.microsoft.com/en-us/microsoft-copilot/blog/copilot-studio/automate-business-processes-with-agents-plus-workflows-in-microsoft-copilot-studio/). Procurement, customer service, sales, and workflow patterns.
5. ServiceNow, [Use agentic AI in Now Assist for ITOM](https://www.servicenow.com/docs/r/it-operations-management/now-assist-for-it-operations-management/now-assist-itom-ai-agent-workflows.html). Alert triage, recurring-pattern analysis, related incidents, and verification.
6. OpenAI, [Inside OpenAI's in-house data agent](https://openai.com/index/inside-our-in-house-data-agent/). Data discovery, SQL, iterative exploration, notebooks, reports, and multiple entry points.
7. Dify, [Creating an application: Workflow](https://docs.dify.ai/en/guides/application-orchestrate/creating-an-application). User input, branching, iteration, output, logs, and API-oriented orchestration.

## Unsplash assets

| Slide | Local asset | Author and original link | Treatment |
| --- | --- | --- | --- |
| `f01-cover` | `assets/bg-enterprise-grid-timothee-duran.jpg` | [Timothée Duran](https://unsplash.com/photos/dcLG-6DEPiQ) | Full bleed; portrait source cropped around the blue sky and right-side facade; dark left gradient |
| `f04-product-atlas` | `assets/bg-atrium-willian-justen.jpg` | [Willian Justen de Vasconcellos](https://unsplash.com/photos/avT9dYK-9rE) | Full bleed at low opacity; centered on the ceiling grid; warm-white veil for diagram contrast |
| `f12-multi-agent` | `assets/bg-collaboration-mimi-thian.jpg` | [Mimi Thian](https://unsplash.com/photos/vdXMSiX-n6M) | Full bleed; centered on the group and laptop; navy overlay and blur-backed project objects |
| `f16-case-brief` | `assets/bg-architecture-shadow-declan-sun.jpg` | [Declan Sun](https://unsplash.com/photos/n8UBJeKko3I) | Full bleed; horizontal crop follows repeating shadows; dark navy overlay |
| `f20-qa`, `f21-thank-you` | `assets/bg-geometric-facade-arlind.jpg` | [Arlind Photography](https://unsplash.com/photos/qk9KT1bcj70) | Q&A 使用低饱和深蓝遮罩；Thank You 采用 44/56 分栏与不同的立面裁切 |

All five files are localized in `assets/`; the slides do not depend on network access. Each image is published on its linked page as a free Unsplash image.

## Timing contract

| Segment | Slides | Time |
| --- | --- | --- |
| Product-form framework | `f01`–`f15` | 30:00 |
| One capability, three products | `f16`–`f19` | 10:00 |
| Q&A | `f20` | 4:30 |
| Thank You | `f21` | 0:30 |

## Claim-handling rules

1. 外部产品只证明形态和场景，不构成跨供应商能力排名。
2. 来源方效果数字不跨案例比较；本版正文不依赖供应商 ROI 数字。
3. Dify 作为实现与包装平台，不暗示外部案例企业使用 Dify。
4. 退款分析案例始终是静态合成教学推演。
5. 旧版 `n01`–`n20` 的委派、契约、证据账本和 HITL 主线已经退役；新版 `f01`–`f21` 是独立结构。
