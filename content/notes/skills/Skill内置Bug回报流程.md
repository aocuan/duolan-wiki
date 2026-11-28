---
title: Skill 内置 bug 回报流程
type: 主题综述
tags:
  - skills
  - 前端设计
date: 2026-11-27
updated: 2026-11-27
status: seedling
source_bot: 研究 · 前端设计 Skills
sources:
  - https://github.com/vercel-labs/ui/pull/1417
publish: true
---

# Skill 内置 bug 回报流程

组件库的官方 skill 不只教 agent 怎么用库，也可以让 agent 在发现库本身的 bug 时，按固定格式回报给上游。一个公开的样本是 [vercel-labs/ui](https://github.com/vercel-labs/ui)（Apache-2.0，星标 7,795，截至 2026-11-27 太平洋时间）的 [PR #1417](https://github.com/vercel-labs/ui/pull/1417)，2026-11-27 合入，给 ui-sdk skill 加了「Report a Bug」一节。

## 流程

1. **触发条件写死**：组件行为和文档页说的不一样、报错来自库内部、类型和文档对不上。
2. **先绕过，再问**：agent 先想办法把手头任务做完，然后只问一次要不要回报。用户没有对确切的 issue 文本说「可以」，就不发 issue，也不发评论。
3. **确认是库的问题**：重读文档页，用只含该库组件的最小测试复现，比对已装版本和最新版本。
4. **查重**：搜索已有的 open 和 closed issue，有匹配的 open issue 就停。
5. **固定格式**：包和版本、框架、一个失败的测试作为复现、被违背的文档原句和实际行为、已经核查过的项目。写怎么验证，不写怎么修。
6. **安全问题不公开**：能让人越权读写的 bug 走 security policy。

仓库同时加了字段一致的 issue 模板，维护方自己的分诊 agent 也能直接读。

## 判断

- 关键是两道闸：发帖前的同意闸门，以及「先复现，再下结论」。没有这两道，agent 回报很容易变成噪音。
- 其他组件库和设计系统的 skill 可以照搬这套流程。和用 skill 串设计流程的做法对照，见 [[前端设计Skills怎么串]]。

相关：[[Skills]]、[[Skill供应链风险]]。入口：[[indexes/Skills]]。
