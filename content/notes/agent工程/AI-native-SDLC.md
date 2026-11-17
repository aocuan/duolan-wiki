---
title: AI-native SDLC 不是一套东西
type: 主题综述
tags:
  - Agent工程
  - 综述
date: 2026-11-17
updated: 2026-11-17
status: evergreen
source_bot: 研究 · Agentic 工程实践
sources:
  - https://www.langchain.com/blog/the-agent-development-lifecycle
  - https://claude.com/blog/the-ai-native-sdlc-playbook
  - https://learn.chatgpt.com/guides/build-ai-native-engineering-team
publish: true
---

# AI-native SDLC 不是一套东西

2026 年有多份材料都在谈「AI 时代怎么做软件」，标题看起来像同一套生命周期，主语其实不同。混用「SDLC」会造成假共识。

## 结论

至少要分清四个主语：

| 材料 | 真正的对象 | 真正的病 | 开出的药 |
|---|---|---|---|
| Google 白皮书 *The New SDLC With Vibe Coding*（Osmani、Saboo、Kartakis，2026 年 5 月） | 工程文化与产线 | 把 AI 当高级补全，或把 vibe 当成生产方法 | 把 vibe、structured、agentic 看成一条光谱；分界是结构与验证，不是用不用 AI。强调 [[Harness]]、上下文工程、测试加评测、以及总拥有成本 |
| LangChain *The Agent Development Lifecycle*（Harrison Chase，2026-05-09） | **Agent 作为产品** | Demo 不等于可重复出货；看不见执行轨迹 | Build → Test → Deploy → Monitor，再用 Iterate / Govern 包住；核心是 trace 到 eval |
| Anthropic *The AI-Native SDLC playbook*（Louis Claxton，2026-08-21） | **软件变更作为产品，agent 当工人** | 代码不再是瓶颈，人速的计划、评审、发布跟不上 agent 的产出 | 用人和 agent 都能读的文件链交接（如 intent / spec / plan），用 skill 当顾问、用 hook 当硬闸门 |
| OpenAI *Building an AI-Native Engineering Team* | **工程团队的职责划分** | 还把编码 agent 当自动补全 | 不必推倒重来。按阶段问 Delegate / Review / Own；用小工作流叠加 |

前三份有稳定的公开网页或白皮书可核对；OpenAI 那份以 [ChatGPT Learn 指南页](https://learn.chatgpt.com/guides/build-ai-native-engineering-team) 为准，页面本身没有署作者和发布日期。

## 几条用得上的薄实践

这些直接来自上面材料的交集，不必先上重型框架：

- 一份短的 [[AGENTS-md|AGENTS.md]] 或同类规则文件，写清怎么测、什么不能碰。
- 需要专项流程时再装 [[Skills]]，不要把整本方法论塞进每次对话。
- **测试** 决定 agent 能不能自己打转，比任何规格框架都硬。
- 工具若支持 **hooks**，就把「不准提交密钥、不准直接发布生产」做成确定性拦截。
- 用人能读的计划或规格文件做交接，而不是只靠周会纪要。
- 生产闸门必须由人推开。开发环境可以宽松，生产不行。

OpenAI 给日常工作的口诀很短：每一步问 Delegate（这一稿交给 AI 吗）、Review（人要看什么）、Own（最终责任在谁）。架构、含糊需求和上线，责任通常仍在人。

还要分清 **tests** 和 **evals**：前者要求同一输入同一输出；后者在没有唯一正确答案时，看轨迹走得对不对。两边都需要，但不是同一个东西。

## 不必立刻照搬的部分

- LangChain 的 ADLC 解决的是「把一个 agent 应用运上线」，不是「用编码 agent 改写传统软件工厂」。
- Anthropic 的文件链和硬闸门，适合已经出现「人审不过来」的团队；小仓库先把手册、测试和 hooks 做好就行。
- Google 白皮书里的光谱有助于和管理者对齐语言：哪些任务允许 vibe，哪些必须有验证。它提供的是框架和例证，不是对照实验。
- Spec Kit、OpenSpec、BMAD 彼此并不兼容，星多不等于该上。见 [[薄技能与重框架]]。

相关入口：[[indexes/Agent工程]]。
