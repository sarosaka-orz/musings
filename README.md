# 楓見隨想錄

> 大型機、語言模型、以及其他事情

一個關於 IBM Z、LLM、以及把它們放在一起時發生的事情的個人部落格。風格受京都美學啟發——簡約、溫暖、留白。

## 技術棧

- [Astro](https://astro.build) — 靜態網站框架
- Markdown — 文章撰寫
- GitHub Pages — 部署託管

## 本地開發

```bash
npm install
npm run dev
```

開發伺服器會在 `localhost:4321` 啟動。

## 建構

```bash
npm run build
```

產出會在 `dist/` 目錄。

## 目錄結構

```
src/
├── content/posts/    # Markdown 文章
├── components/       # Astro 元件
├── layouts/          # 頁面佈局
├── pages/            # 路由頁面
└── styles/           # 全域樣式
```

## 新增文章

在 `src/content/posts/` 建立 `.md` 檔案，frontmatter 格式：

```markdown
---
title: 文章標題
date: 2026-06-01
tags: [tag1, tag2]
excerpt: 摘要文字
---

正文內容...
```