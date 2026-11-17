# duolan-wiki

duolan-wiki 是一套公开的个人知识库。本地用 Obsidian 写，这个仓库是唯一的内容来源。

## 技术栈

- **Obsidian**：本地写作和双链。用 [obsidian-git](https://github.com/Vinzent03/obsidian-git) 自动提交并推到 GitHub。
- **Quartz 5**：以后可以把 `content/` 做成网站。模板和 `quartz.config.yaml` 已经留好，**站点发布暂缓**，目前不会部署到 GitHub Pages。
- **给 AI 用**：根目录有 `AGENTS.md` 和 [llms.txt](https://llmstxt.org/)，并建议安装 [obsidian-skills](https://github.com/obsidianmd/obsidian-skills)，让 Claude Code、Codex、Cursor 等正确读写这个库。

## 目录

```
content/index.md         首页
content/notes/           按主题分类的笔记
  概念/ 开源项目/ agent工程/ skills/
  rag/ 企业知识/ 论文/ 趋势/
content/sources/         摘录、引用和外部资料
content/indexes/         主题索引和 MOC
templates/               笔记模板（不进入站点）
private/                 日记、未脱敏草稿和不宜公开的内容（已加入 .gitignore）
```

## 开始使用

1. 克隆仓库：

   ```bash
   git clone https://github.com/aocuan/duolan-wiki.git
   cd duolan-wiki
   ```

2. 用 Obsidian 打开**仓库根目录**作为库（vault）。笔记写在 `content/` 里；这样根目录的 `private/` 也会出现在库中。Quartz 源码会出现在文件列表里，可在 Obsidian 的「文件与链接」里排除 `quartz/`、`node_modules/`、`docs/` 等文件夹。

3. 安装社区插件 [obsidian-git](https://github.com/Vinzent03/obsidian-git)，用来自动提交并推送到 GitHub。

4. 给 AI 编程工具安装官方 skills：

   ```bash
   npx skills add obsidianmd/obsidian-skills
   ```

日记请写在 `private/`。这个目录已在 `.gitignore` 中，克隆后如果不存在，自己建一个即可。

每篇公开笔记请带上 YAML frontmatter（`title`、`type`、`tags`、`date`、`publish: true`），并用 wikilink 互链。写入前必须按 `AGENTS.md` 里的脱敏规则检查。详细约定见 `content/index.md` 和 `AGENTS.md`。模板在 `templates/`。

## 以后若要发布网站

现在不部署站点。如果以后要自己托管，先把 `quartz.config.yaml` 里的 `baseUrl`（目前是占位 `example.com`）改成真实地址，不要带 `https://`，然后按 [Quartz 托管说明](https://quartz.jzhao.xyz/hosting) 配置。本地预览可以先执行 `npm i`，再运行 `npx quartz build --serve`。

本仓库基于 [Quartz 5](https://github.com/jackyzha0/quartz)（MIT）。保留 `upstream` 远程后，可以用 `npx quartz upgrade` 拉取上游更新。
