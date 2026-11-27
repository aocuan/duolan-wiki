---
title: 给 Agent 用的知识库项目地图
type: 主题综述
tags:
  - 品类
  - 企业知识
  - 记忆
date: 2026-11-26
updated: 2026-11-26
status: evergreen
sources:
  - https://github.com/vectorize-io/hindsight
  - https://github.com/volcengine/OpenViking
  - https://github.com/infiniflow/ragflow
  - https://github.com/Tencent/WeKnora
  - https://github.com/obsidianmd/obsidian-skills
  - https://github.com/VectifyAI/PageIndex
  - https://github.com/khoj-ai/khoj
publish: true
---

# 给 Agent 用的知识库项目地图

「给 agent 配知识库」至少指四种不同的东西。先分层，再比项目，不要把记忆层和文档平台放进同一张竞品表。星标截至 2026-11-26（太平洋时间），只作热度参考。

## 一、记忆层：让 agent 记住事实、偏好和经验

| 项目 | 许可证 | 星标 | 一句话 |
|---|---|---|---|
| [[Hindsight]] | MIT | 约 6.4 万 | 主打从使用中学习，2026 年下半年最热 |
| [[Mem0]] | Apache-2.0 | 约 7.0 万 | 默认的轻量记忆层，存偏好和关键事实 |
| [[OpenViking]] | AGPL-3.0 | 约 4.3 万 | 知识、记忆、Skills 放进同一个虚拟文件系统 |
| [[Cognee]] | Apache-2.0 | 约 3.4 万 | 自动抽取并合并事实，偏结构化记忆 |
| [[Graphiti]] | Apache-2.0 | 约 3.3 万 | 带有效期的记忆图谱 |
| [[Letta]] | Apache-2.0 | 约 2.6 万 | 有状态 agent 平台，前身 MemGPT |
| [[claude-mem]] | Apache-2.0 | 约 12 万 | 记编码 agent 的工作轨迹，跨会话注入 |
| [[Basic-Memory]] | AGPL-3.0 | 约 4,700 | 普通 Markdown 当跨会话记忆 |

## 二、知识库与 RAG 平台：给 agent 配文档检索

| 项目 | 一句话 |
|---|---|
| [[RAGFlow]] | 扫描件、手册、表格解析最强，有 API 和 MCP |
| [[WeKnora]] | 中文支持好，近一年往 agent 平台扩，功能面很宽 |
| [[Dify]] | 体量最大，强项是工作流编排，不是知识库本身 |
| [[LightRAG]] | 需要图检索时的轻量选择 |
| [[Onyx]]、[[FastGPT]]、[[MaxKB]] | 可选；MaxKB 是 GPL，FastGPT 有附加条款 |

选型细节见 [[企业知识库开源选型]]。

## 三、给 agent 读写的 Markdown 与 wiki

- [[obsidian-skills]]：Obsidian 官方技能包，教 agent 读写笔记库，成本最低。
- [[claude-obsidian]]：把资料丢进收件箱，由模型整理成双链 wiki。
- [Khoj](https://github.com/khoj-ai/khoj)（AGPL-3.0，约 3.8 万星）：自托管的「AI 第二大脑」，但主仓自 2026 年 8 月起没有推送，用起来也偏重，不建议新上。

思路见 [[LLM知识库]]，落地见 [[个人知识库怎么搭]]。

## 四、不用向量的检索

- [[PageIndex]]：让模型沿目录树定位长文档，适合单份长文档；2026 年 11 月起热度降温。
- 更一般的做法是让 agent 在循环里用 BM25 或 grep 自己查，见 [[Agentic搜索]]。

## 怎么选

1. 先把原始材料变成干净的文本（见 [[文档解析工具对照]]），放进有目录、有说明文件的文件夹。agent 用文件搜索就能取到内容，可追溯、不锁平台。
2. 文档多到文件搜索不够用，再接 [[RAGFlow]] 这类平台，或加 [[PageIndex]] 做长文档定位。
3. 想让 agent 跨会话记住东西，先试 [[Basic-Memory]] 或 [[Mem0]]，再看 [[Hindsight]]。任何记忆层上线前，先跑原始记录检索基线，见 [[RAW-RAG]]。
4. 最值得持续盯的是 [[Hindsight]]、[[WeKnora]]、[[PageIndex]]、[[OpenViking]]。

入口：[[indexes/品类]]、[[indexes/企业知识与本体]]。
