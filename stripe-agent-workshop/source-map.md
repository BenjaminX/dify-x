# From Scenario to System · Source Map

## Deck Contract

- English deck: 22 slides, 22 speaker-note blocks, 45:00 total.
- Product framing: slides `s01`–`s06`, 12:00.
- Static synthetic walkthrough: slides `s07`–`s10`, 7:00.
- Engineering architecture: slides `s11`–`s18`, 17:30.
- Product synthesis: slides `s19`–`s20`, 3:30.
- Q&A and close: slides `s21`–`s22`, 5:00.

## Product-Design Synthesis

Slides `s02`–`s06` and `s19` adapt the work-unit, product-form, four-question, and packaging framework from `enterprise-agent-campus/index_en.html`. The six forms are a teaching taxonomy, not a maturity model, market ranking, or fixed official Dify classification.

## Static Walkthrough

Slides `s07`–`s10` use a synthetic support workflow: ticket intake, account lookup, urgency classification, response drafting, and high-risk review. It contains no customer data, Stripe workflow, live product capture, or production performance claim.

## Engineering Sources

| Slides | Source | Use | Boundary |
|---|---|---|---|
| `s12` | [Dify workflow source tree](https://github.com/langgenius/dify/tree/main/api/core/workflow) | Responsibility and package context | Paths may evolve; responsibility split is the durable point. |
| `s13` | [PR #31944](https://github.com/langgenius/dify/pull/31944) | Early single-shot implementation | Repository history, not a benchmark. |
| `s16` | [PR #40611](https://github.com/langgenius/dify/pull/40611) | Tool routing, ranking, pinning, hydration | Thresholds and caps are implementation-specific. |
| `s17` | [PR #32130](https://github.com/langgenius/dify/pull/32130) | Repair and structural validation | Error labels may evolve. |
| `s18` | [PR #38975](https://github.com/langgenius/dify/pull/38975) | Prompt reduction and parallel builders | Engineering disclosure, not independently audited ROI. |
| `s19` | [Dify application orchestration docs](https://docs.dify.ai/en/guides/application-orchestrate/creating-an-application) | Models, knowledge, tools, workflow, API delivery | Packaging map is product-design guidance. |

## Image Credits

| Slides | Asset | Photographer | Original |
|---|---|---|---|
| `s01` | `../enterprise-agent-campus/assets/bg-enterprise-grid-timothee-duran.jpg` | Timothée Duran | [Unsplash original](https://unsplash.com/photos/dcLG-6DEPiQ) |
| `s07` | `../enterprise-agent-campus/assets/bg-architecture-shadow-declan-sun.jpg` | Declan Sun | [Unsplash original](https://unsplash.com/photos/n8UBJeKko3I) |
| `s21`, `s22` | `../enterprise-agent-campus/assets/bg-geometric-facade-arlind.jpg` | Arlind Photography | [Unsplash original](https://unsplash.com/photos/qk9KT1bcj70) |

## Speaker

Zheng Li · Head of DevRel · Dify  
[banana@dify.ai](mailto:banana@dify.ai)
