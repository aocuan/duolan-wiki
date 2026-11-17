---
title: duolan-wiki
tags:
  - index
date: 2026-11-17
publish: true
---

这是 duolan 的公开个人知识库。本地用 Obsidian 写，这个 GitHub 仓库是唯一的内容来源。以后可以用 Quartz 做成网站，目前先不发布站点。

## 目录

- [[notes/index|笔记]]：自己写的笔记
- [[sources/index|来源]]：摘录、引用和外部资料
- [[indexes/index|索引]]：主题索引和 MOC

日记和不宜公开的内容放在仓库根目录的 `private/`，不要放进 `content/`。

## 写作约定

用 wikilink 互链，例如 `[[笔记名]]`。

每篇笔记在开头写 YAML frontmatter，至少包含标题、标签和日期，并加上 `publish` 标记：

```yaml
---
title: 笔记标题
tags:
  - 标签
date: 2026-11-17
publish: true
---
```

`publish: true` 表示这篇可以公开。以后若启用 Quartz 的 explicit-publish 插件，只有带这个标记的笔记才会出现在站点里。`private/` 已加入 `.gitignore`，其中的内容既不会提交，也不会发布。
