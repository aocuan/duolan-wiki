---
title: OntoSmith
type: 项目卡
tags:
  - 开源项目
  - 企业知识
date: 2026-11-17
updated: 2026-11-17
status: evergreen
source_bot: 研究 · 企业本体
sources:
  - https://github.com/Dongbumlee/ontosmith
  - https://dongbumlee.github.io/ontosmith/
repo: https://github.com/Dongbumlee/ontosmith
license: MIT
stars: 287
verdict: 从文档抽三元组并逐条过闸的工具，不是操作本体平台。适合对照「类型先定、证据可回指」，不要当成业务写回系统。
publish: true
---

# OntoSmith

[Dongbumlee/ontosmith](https://github.com/Dongbumlee/ontosmith)（MIT，约 287 星，截至 2026-11-17，太平洋时间；说明页 [dongbumlee.github.io/ontosmith](https://dongbumlee.github.io/ontosmith/)）用来从文档里抽出实体和关系，并要求每条事实经过判定后才写入图数据库，同时挂上证据原文。提议和判定是分开的，判定一步可以用决策模型来做，见 [[决策模型检索]]。

这里的「本体」是扁平的抽取契约：实体类型、关系类型，加上定义和边界例子。它没有类层次，也不做公理推理，因此不是 [[操作本体]]，也不是 [[基础本体]]。和常见的图检索相比，它强调先定类型、人先批、事实逐条审。

星标不高，适合当方法和流水线的参考，不适合当成企业写回平台。入口：[[indexes/开源项目]]。
