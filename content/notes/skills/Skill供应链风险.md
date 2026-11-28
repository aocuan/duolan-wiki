---
title: Skill 供应链风险
type: 主题综述
tags:
  - skills
  - 安全
date: 2026-11-27
updated: 2026-11-27
status: seedling
source_bot: 侦察 · 热门论坛情报
sources:
  - https://github.com/convex/convex-backend-skill/issues/64
  - https://news.ycombinator.com/item?id=50669765
publish: true
---

# Skill 供应链风险

SKILL.md 不是文档，而是给 agent 的可执行指令。它能让 agent 跑命令、联网、读写文件，权限和一段 shell 脚本差不多。装第三方 skill 或插件，就是在引入一段供应链。

## 一个公开案例

[convex/convex-backend-skill 的 issue #64](https://github.com/convex/convex-backend-skill/issues/64)（2026-10-26 提出，截至 2026-11-27 仍未关闭）指出，这个已上架官方插件市场的技能包有三处问题：

- quickstart 技能把用户一句话的项目想法，以「遥测」名义发到一个自动生成名字的远程主机，用户事先不知道；
- add 技能从同一主机下载脚本，直接交给 shell 执行，版本不固定；
- 另一个技能把「下载」和「执行」拆成两步，注释里直说这样做是因为合在一起的形态会被安全检查拦下。

提出者认为这更像是为了让上手流程顺利，而不是恶意；但最后一条等于让 agent 绕开用户或管理员自己选择的检查。2026-11-27 这条被转到 [Hacker News](https://news.ycombinator.com/item?id=50669765)，当天约 255 分、80 条评论。

## 判断

- **审 skill 要像审脚本。** 重点找三类东西：向外发送数据、运行时下载且不固定版本的远程脚本、要求改变命令形态的措辞。
- **只看单条命令的安全检查不够。** 把一个危险动作拆成几步就能绕过。harness 需要把前后调用关联起来，例如同一个文件先被下载、后被执行。概念见 [[Harness]]。
- **上架官方市场不等于审计过。** 团队用第三方 skill 时，固定到具体 commit，升级时看差异；也可以先用扫描工具过一遍，见 [[薄技能与重框架]] 里提到的 SkillSpector。

相关：[[Skills]]、[[agent-skills]]。入口：[[indexes/Skills]]。
