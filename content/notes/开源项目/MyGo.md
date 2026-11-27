---
title: MyGo
type: 项目卡
tags:
  - 开源项目
  - 桌面框架
date: 2026-11-26
updated: 2026-11-26
status: evergreen
sources:
  - https://github.com/egoist/mygo
  - https://github.com/wailsapp/wails
  - https://github.com/tauri-apps/tauri
publish: true
repo: https://github.com/egoist/mygo
license: MIT
stars: 6997
verdict: 思路新、卖点实在，但仍很年轻；原型和小工具可以试，要长期维护的产品先选 Wails 或 Tauri
---

# MyGo

[MyGo](https://github.com/egoist/mygo) 是用 Go 写桌面应用的框架，作者是 egoist。许可证 MIT，星标 6,997，截至 2026-11-26（太平洋时间）。仓库 2026 年 9 月下旬才建，增长很快。

## 它怎么做

- 每个窗口二选一：要么用系统自带的 webview（macOS 的 WKWebView、Windows 的 WebView2、Linux 的 WebKitGTK）显示网页前端，要么用纯 Go 写的原生界面，由框架自己在 GPU 上绘制，没有 HTML 和 JS。两种窗口可以在同一个应用里混用。
- 前端调用 Go 代码时，框架根据 Go 代码生成带类型的 TypeScript 客户端。
- 不依赖 cgo，可以在一台机器上编出三个平台的包；产物是几 MB 的单个二进制。菜单、托盘、通知、打包签名和自动更新都内置。

## 判断

早期调研（2026-10）时它刚建两周，一天发好几个版本，接口还在大改，提交几乎都来自作者一人。卖点是实在的，「Go 直接画原生界面」这一块也是同类里少见的。但正式项目要等它出 1.0、贡献者变多、有几个像样的应用上线以后再考虑。用的话要锁死版本，准备好升级时改代码。

## 和相邻框架的差别

- [Wails](https://github.com/wailsapp/wails)（MIT，约 3.7 万星）：同样是 Go 加系统 webview，已经成熟，适合要长期维护的 Go 桌面应用。
- [Tauri](https://github.com/tauri-apps/tauri)（MIT / Apache-2.0 双许可，约 11.3 万星）：Rust 后端，生态最大，也覆盖移动端。
- Electron：自带完整浏览器，体积和内存最大，生态最全。

作者自己的 [[Lorca]] 只在 Windows 和 Linux 客户端用了 MyGo，主体是 Rust，不能当成 MyGo 扛住正式产品的证据。

入口：[[indexes/开源项目]]。
