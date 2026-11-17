---
title: Harness
type: 概念卡
tags:
  - 概念
  - Agent工程
date: 2026-11-17
updated: 2026-11-17
status: evergreen
source_bot: 研究 · Agentic 工程实践
sources:
  - https://claude.com/blog/the-ai-native-sdlc-playbook
  - https://www.langchain.com/blog/the-agent-development-lifecycle
publish: true
---

# Harness

Agent 不是「一个更聪明的模型」。模型只是脑子；让它能连续干活的，是套在外面的 **harness（套件）**。

## 定义

可以把 harness 想成给实习生配好的工位，通常包括：

- **规则文件**：例如 [[AGENTS-md|AGENTS.md]] 或 `CLAUDE.md`，说明这个项目用什么技术、测试怎么跑、什么绝对不能做。
- **工具**：读文件、跑命令、查网页、改代码。没有工具，模型只能空谈。
- **沙箱**：允许它跑代码，但跑坏了不要伤到真实环境。
- **Hooks（钩子）**：用确定性的规则拦危险动作，例如禁止提交密钥、禁止直接推到生产，而不是再求模型「请注意安全」。
- **按需加载的说明**：也就是 [[Skills]]。上下文有限，不能把整本方法论一次塞进去。

Agent 出错，多数时候不是模型笨，而是套件没配好：缺工具、规则含糊，或没有围栏。

## 和相近概念的差别

- 和「提示词技巧」不同：harness 是可检查的工程配置，不是把一句话写得更花。
- 和重型流程框架不同：先把上述薄层做好，再考虑要不要上规格驱动的整套仪式。取舍见 [[薄技能与重框架]]。
- 和「把 agent 当产品来运」也不同。LangChain 谈的 ADLC 主语是面向用户的 agent 应用；这里的 harness 主语是「编码 agent 在一个代码仓库里怎么干活」。对照见 [[AI-native-SDLC]]。

相关入口：[[indexes/Agent工程]]。
