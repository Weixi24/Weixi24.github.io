# 我的个人网站

> 用 Hugo + PaperMod 搭建的静态个人网站，部署在 GitHub Pages。

## 快速开始

```bash
# 本地预览
hugo server -D

# 新建文章
hugo new posts/文章名.md

# 提交部署
git add . && git commit -m "更新内容" && git push
```

## 技术栈

- Hugo Extended v0.163.1
- PaperMod 主题
- GitHub Pages 托管
- Markdown 写文章

## 本地开发

需要安装 Hugo Extended：
```bash
winget install Hugo.Hugo.Extended
```

本地预览：
```bash
hugo server -D
```
访问 http://localhost:1313/

## 更新文章

每个文章是一个 Markdown 文件：`content/posts/文件.md`

```yaml
---
title: "文章标题"
date: 2026-06-13
description: "文章描述"
---

正文内容（Markdown 格式）
```

## 维护日志

见 [README.md](README.md)
