---
title: Docling
type: 项目卡
tags:
  - 开源项目
  - 文档解析
date: 2026-11-26
updated: 2026-11-26
status: evergreen
sources:
  - https://github.com/docling-project/docling
  - https://docling-project.github.io/docling/
publish: true
repo: https://github.com/docling-project/docling
license: MIT
stars: 71130
verdict: 格式覆盖最广、生态接入最好的通用文档解析工具；把文件转成 agent 好读的 Markdown 或 JSON 时的默认候选
---

# Docling

[Docling](https://github.com/docling-project/docling) 是 IBM 研究院发起、现托管在 LF AI & Data 基金会下的文档解析工具。它把 PDF、Word、PPT、Excel、HTML、图片、邮件、音频转写等格式统一转成干净的 Markdown、HTML 或无损 JSON，转换时识别版面、阅读顺序、表格结构、公式和代码，扫描件可以走 OCR。许可证 MIT，星标 71,130，截至 2026-11-26（太平洋时间）。

## 开源范围

完整开源，本地运行。它已经接好 LangChain、LlamaIndex 等框架，也提供 MCP 接口，agent 可以直接调用它解析文件。

## 判断

适合当 RAG 或 agent 知识库的第一步：先把文档变成结构清楚的文本，再决定怎么检索。格式覆盖面和生态是它的强项；中文扫描件和复杂版面上，[[MinerU]] 通常更有优势。两者在自己语料上的实际效果，最好拿几份样例实测后再定。

对照见 [[文档解析工具对照]]。入口：[[indexes/开源项目]]。
