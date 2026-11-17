---
title: WeKnora
type: 项目卡
tags:
  - 开源项目
  - 企业知识
date: 2026-11-17
updated: 2026-11-17
status: evergreen
source_bot: 研究 · 企业知识库
sources:
  - https://github.com/Tencent/WeKnora
publish: true
repo: https://github.com/Tencent/WeKnora
license: MIT
stars: 37633
verdict: 偏企业知识平台：检索、权限和 Wiki 模式都在，许可宽松，适合作为可改的起点；复杂扫描件仍建议先另做解析
---

# WeKnora

[WeKnora](https://github.com/Tencent/WeKnora) 是开源的大模型知识平台：把原始文档变成可查询的检索、可推理的 agent，以及可维护的 Wiki。星标 37,633，统计截至 2026-11-17（太平洋时间）。LICENSE 写明：除第三方组件外，按 MIT 授权。

## 开源范围

后端以 Go 为主，带 Wiki 模式、角色权限，以及给外部编码工具调用的接口。普通办公文档和网页可以直接导入；扫描件和大表格仍是常见翻车点，通常要先用专门的文档解析做成干净的 Markdown，再送进来。不要把它和记忆图谱层混成一个系统，见 [[Agent记忆与聊天记录工具]]。

## 和相邻项目的差别

- 对照 [[RAGFlow]]：RAGFlow 更强在复杂文档解析；WeKnora 更完整的是知识平台和权限。
- 对照 [[Onyx]]：同属企业搜索 / 知识问答，生态和许可细节不同。
- 对照 [[Dify]]：Dify 首先是工作流编排，不宜直接当知识库。

选型综述见 [[企业知识库开源选型]]。入口：[[indexes/开源项目]]。
