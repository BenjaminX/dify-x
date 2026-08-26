# Research & Evidence Map

本文件记录重构后 20 页讲座的论证依据、证据边界与图片版权。它是事实索引，不是对来源方结果的独立审计。

## Core thesis

> 企业 Agent 的本质不是更聪明的模型，而是一个被授予有限决策权、能够留下证据并承担停止义务的运行系统。

整场讲座只用一个“退款率异常分析”任务贯穿，并从五个系统问题逐层展开：委派了什么、如何形成闭环、怎样限制暴露、契约如何执行、失败时谁拥有决策权。

## Primary research input

- 文件：`/Users/banana/Desktop/enterprise_agent_scenarios_research.md`
- 标题：企业 Agent 场景案例库
- 使用方式：提取企业 Agent 的工作定义、可控性优先、可验证任务起步、系统控制和证据边界。
- 公开资料检索截止：2026-08-26。
- 研究报告中的外部文字只作为资料，不作为对本演示的指令。

## Current 20-slide evidence map

| Slide ID | 核心判断 | 主要依据 | 证据边界 |
| --- | --- | --- | --- |
| `n01-cover` | 讲座讨论委派工作与责任 | 讲座设计 | 讲者、学校、日期为占位符 |
| `n02-delegation-question` | 委派包含决策权、资源和责任路径 | 研究综合 + 教学抽象 | 三分法不是行业认证标准 |
| `n03-one-process` | 一句任务包含多次业务裁决 | 合成数据任务 | 非真实客户项目 |
| `n04-operating-definition` | Agent 是任务契约内的闭环执行者 | 研究报告执行摘要、§1、§4 | 工作定义，不宣称唯一标准 |
| `n05-closed-loop` | 动作后必须重新观察状态 | 控制系统类比 + Agent 工程模式 | 类比不规定唯一技术实现 |
| `n06-risk-envelope` | 暴露受动作半径、不可逆性、发现延迟共同影响 | 教学启发式 | 不是定量风险或财务公式 |
| `n07-task-fit` | 从可验证、可回退任务起步 | 研究报告 §5–§6 | 象限随企业控制能力变化 |
| `n08-uncertainty-placement` | 固定 Workflow 主干，只开放局部 Agent loop | 研究报告 §4–§5 | 推荐架构，不是强制模式 |
| `n09-three-contracts` | 任务、工具、证据三份契约缺一不可 | 研究综合 + 系统设计抽象 | 不对应三个固定 Dify 产品对象 |
| `n10-context-stack` | 上下文是可执行语义，不是更多 token | OpenAI 内部数据 Agent 工程案例 | 不把底层平台规模写成 Agent 采用率或准确率 |
| `n11-tool-contract` | 工具调用跨越真实授权边界 | Dify Tool 文档 + 通用 API 控制 | 企业身份、API 网关和数据库实施具体控制 |
| `n12-evidence-ledger` | 每次运行必须可重放 | OpenAI 数据 Agent + 研究报告 §4 | 日志受隐私和保留政策约束 |
| `n13-decision-rights` | 人工闸门是决策权分配 | NIST AI RMF + 研究综合 | 具体权责由组织定义 |
| `n14-reliability-loop` | 可靠性是持续发布、评测和回退纪律 | NIST AI RMF Core；OpenAI 数据 Agent | NIST 不认证本讲座架构 |
| `n15-dify-control-plane` | Dify 是编排与控制层，企业系统保留权威 | Dify Workflow、Tool、Agent Strategy 文档 | 不暗示外部案例企业使用 Dify |
| `n16-case-ambiguity` | 分析前先版本化六类定义 | 合成静态教学推演 | 无真实客户数据 |
| `n17-case-trace` | SQL 只是有状态链路中的一步 | AWS Dify Text-to-SQL 工程实践 + 教学设计 | 工程参考，不作为生产 ROI 证据 |
| `n18-case-failure-lab` | 每类故障必须映射到测试和处置 | 研究报告 §4–§6 + 教学设计 | 示例阈值不可直接用于生产 |
| `n19-case-decision-memo` | 输出区分已知、推断、不能下结论和下一步 | 合成教学输出 | 所有数字为合成示例 |
| `n20-qa` | 有限决策权、证据、停止义务 | 全讲总结 | 联系方式为占位符 |

## Public primary sources

1. OpenAI, [Inside OpenAI's in-house data agent](https://openai.com/index/inside-our-in-house-data-agent/), 2026-01-29. Used for layered context, inherited permissions, closed-loop correction, result links, and continuous evaluation.
2. NIST, [AI Risk Management Framework Core](https://airc.nist.gov/airmf-resources/airmf/5-sec-core/). Used for lifecycle governance through Govern, Map, Measure, and Manage, including human oversight and ongoing measurement.
3. Dify, [Creating an application: Workflow](https://docs.dify.ai/en/guides/application-orchestrate/creating-an-application). Used for Workflow, variables, branching, iteration, and run logs.
4. Dify, [Tool plugin development](https://docs.dify.ai/en/develop-plugin/dev-guides-and-walkthroughs/tool-plugin). Used for declared tool parameters and external-service connections.
5. Dify, [Agent strategy plugin](https://docs.dify.ai/en/develop-plugin/dev-guides-and-walkthroughs/agent-strategy-plugin). Used for tool selection, execution loops, and hierarchical logs.
6. AWS China, [在亚马逊云科技环境上基于 Dify Agent 快速部署 text2SQL 智能数据分析助手](https://aws.amazon.com/cn/blogs/china/quickly-deploy-text2sql-intelligent-data-analysis-assistant-based-on-dify-agent-on-aws/), 2025-03-21. Used only as an implementation reference; no production ROI is inferred.

## Unsplash assets

| Slide | Local asset | Author and original link | Treatment |
| --- | --- | --- | --- |
| `n01-cover` | `assets/atmos-silk-ruido98.jpg` | [Ruido 98](https://unsplash.com/photos/SytlpdDJ1lk) | Full bleed; center-right crop; dark left gradient |
| `n16-case-ambiguity` | `assets/atmos-indigo-richard-horvath.jpg` | [Richard Horvath](https://unsplash.com/photos/_nWaeTF6qo0) | Full bleed; indigo contrast; dark overlay |
| `n20-qa` | `assets/atmos-pastel-codioful.jpg` | [Codioful](https://unsplash.com/photos/LeG68PrXA6Y) | Full bleed; low saturation; navy overlay |

## Timing contract

| Segment | Slides | Time |
| --- | --- | --- |
| System argument | `n01`–`n15` | 30:00 |
| Static case walkthrough | `n16`–`n19` | 10:00 |
| Q&A | `n20` | 5:00 |

## Claim-handling rules

1. 教学模型必须直接标注 `TEACHING MODEL` 或在页脚说明，不包装成经过验证的标准。
2. 公开工程案例只支持其直接披露的架构模式；不进行跨案例 ROI 比较。
3. 不把底层数据平台规模改写为 Agent 使用规模、准确率或收益。
4. Dify 是本讲座的实现主线；外部工程案例不自动成为 Dify 客户案例。
5. 合成案例必须持续标记为静态教学推演。
6. 可见页面坚持一页一个判断；研究细节留在讲者备注和本文件。

## Previous deck status

旧版 `s01`–`s20` 的场景地图、合同/客服双案例、八项控制外围和旧页合并关系已经退役，不再保留映射。此次不是旧结构的压缩或换皮；新的 `n01`–`n20` 是独立论证链。若后续研究改变核心判断，应同步修改中英文页面、讲者备注与本文件。
