# AGENTS.md

这是 duolan 的公开个人知识库。笔记是普通 Markdown，本地用 Obsidian 编写。仓库是唯一的内容来源。

## 目录约定

- `content/index.md`：首页，说明这个库是什么、怎么写
- `content/notes/`：自己写的笔记
- `content/sources/`：摘录、引用和外部资料
- `content/indexes/`：主题索引和 MOC
- `private/`：日记和不宜公开的内容
- 仓库其余部分是 Quartz 5 的站点模板，方便以后自己托管；现在不发布网站，不要为了写笔记去改这些源码

## 公开范围

- 只有提交到 git、位于 `content/` 下的笔记是公开的
- `private/` 必须永远不要提交，也不要复制或移动进 `content/`
- 不要把密钥、账号、未公开的个人日记或其他敏感信息写进 `content/`

## 如何阅读和检索

- 先读本文件、`llms.txt` 和 `content/index.md`
- 按文件名、标题、`tags` 和 wikilink 查找，不要假设仓库里有向量数据库或现成的 RAG 服务
- 从 `content/indexes/` 开始看主题入口，再顺着双链进入具体笔记

## 如何写笔记

- 写在 `content/` 的对应目录下，使用 Markdown
- 必须有 YAML frontmatter，至少包含 `title`、`tags`、`date`
- 可以公开的笔记加上 `publish: true`
- 用 wikilink 互链，例如 `[[笔记名]]`
- 新增或大幅改动一篇笔记时，视情况更新 `content/indexes/` 里的相关索引
- 不要提交 `private/`，也不要改动与这次笔记无关的 Quartz 源码
- 提交说明用中文，写清改了什么即可
