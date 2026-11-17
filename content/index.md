---
title: duolan-wiki
tags:
  - index
date: 2026-11-17
publish: true
---

这是一套公开的个人知识库。本地用 Obsidian 写，这个 GitHub 仓库是唯一的内容来源。以后可以用 Quartz 做成网站，目前先不发布站点。

## 目录

- [[notes/index|笔记]]：按主题分类的常青笔记
  - [[notes/概念/index|概念]]、[[notes/品类/index|品类]]、[[notes/开源项目/index|开源项目]]、[[notes/agent工程/index|Agent 工程]]、[[notes/skills/index|Skills]]、[[notes/rag/index|RAG 与检索]]、[[notes/企业知识/index|企业知识]]、[[notes/论文/index|论文]]、[[notes/趋势/index|趋势]]
- [[sources/index|来源]]：摘录、引用和外部资料
- [[indexes/index|索引]]：主题索引和 MOC

日记、未脱敏草稿和不宜公开的内容放在仓库根目录的 `private/`，不要放进 `content/`。笔记模板在仓库根目录的 `templates/`，不会被站点收录。

## 写作约定

用 wikilink 互链，例如 `[[笔记名]]`。一篇笔记只讲一件事；项目、概念和综述靠双链连接，由 [[indexes/index|索引]] 收口。

每篇笔记在开头写 YAML frontmatter。常用字段包括标题、类型、标签、日期、状态、来源和 `publish` 标记：

```yaml
---
title: 笔记标题
type: 概念卡
tags:
  - 标签
date: 2026-11-17
updated: 2026-11-17
status: evergreen
source_bot: 研究 · 主题名
sources:
  - https://example.com
publish: true
---
```

`type` 取 `项目卡`、`主题综述`、`概念卡`、`趋势周报` 或 `论文笔记`。`status` 取 `seedling`（初稿）、`evergreen`（常青）或 `weekly`（按期更新）。公开的笔记加 `publish: true`。以后若启用 Quartz 的 explicit-publish 插件，只有带这个标记的笔记才会出现在站点里。

写入前必须按 `AGENTS.md` 里的脱敏规则检查。内部材料、账号相关内容和未公开的个人项目不要进 `content/`。
