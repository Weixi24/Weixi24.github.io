# 个人网站 — 项目文档

> 一个静态个人网站，用于记录个人经历、学习记录、博客文章。
> 技术栈：Hugo（静态网站生成器）+ GitHub Pages（免费托管）

---

## 1. 项目概述

### 1.1 目标
- 个人博客：写技术笔记、学习心得、生活感悟
- 学习记录：展示学习路径和成长轨迹
- 个人经历：简历性质的自我介绍
- 可扩展：后续可加评论、搜索、分析等功能

### 1.2 技术选型
| 组件 | 选择 | 理由 |
|------|------|------|
| 静态站点生成器 | Hugo (Go) | 速度快、生态成熟、主题丰富 |
| 托管 | GitHub Pages | 免费、自动 HTTPS、支持自定义域名 |
| 内容格式 | Markdown | 简单、版本可控、工具链成熟 |
| 版本管理 | Git | 天然记录修改历史 |
| 评论系统 | Giscus (GitHub Discussions) | 免费、与 GitHub 集成 |
| 搜索 | 前端 JS 搜索 | 静态站方案，无需后端 |

### 1.3 目录结构
```
personal-site/
├── archetypes/          # 新建文章的模板
├── content/             # 所有文章内容
│   ├── posts/           # 博客文章
│   ├── about.md         # 关于我
│   └── timeline.md      # 时间线（学习/成长记录）
├── data/                # 静态数据（如导航菜单配置）
├── layouts/             # 自定义模板（可选）
├── public/              # 生成的静态文件（gitignore）
├── static/              # 静态资源（图片、CSS）
├── themes/              # Hugo 主题
├── hugo.toml            # Hugo 配置文件
└── README.md            # 项目说明
```

---

## 2. 实施计划

### 阶段一：环境准备
- [x] 安装 Hugo Extended (v0.163.1)
- [x] 安装 Git (v2.54.0)
- [ ] 配置 GitHub 账号和 SSH
- [ ] 创建 GitHub 仓库

### 阶段二：主题配置
- [x] 选择 PaperMod 主题
- [x] 配置主题参数（标题、描述、导航菜单）
- [ ] 自定义配色和字体（待决定）

### 阶段三：基础内容
- [x] 创建首页（最新文章列表 + 简介）
- [x] 创建"关于我"页面
- [x] 创建博客文章模板
- [x] 创建第一篇文章（测试用）

### 阶段四：部署上线
- [ ] 配置 GitHub Pages
- [ ] 设置自动构建和部署（GitHub Actions）
- [ ] 测试访问

### 阶段五：扩展功能
- [ ] 评论系统（Giscus）
- [ ] 搜索功能
- [ ] 时间线页面
- [ ] RSS 订阅

---

## 3. 开发日志

### [2026-06-13] 项目启动
- 确定技术方案：Hugo + GitHub Pages
- 创建项目文档（README.md）

### [2026-06-13] 环境搭建
- 安装 Hugo Extended v0.163.1（winget）
- 初始化 Hugo 项目：`hugo new site .`
- 安装 PaperMod 主题（git submodule）
- 配置 hugo.toml（中文 locale、导航菜单、暗色模式）
- 创建基础内容：about.md、posts/hello-world.md
- 本地预览成功：http://localhost:60903/（13 个页面生成）

### [2026-06-13] 主题选择
- 候选：Hugo Blog Awesome / PaperMod
- 选择：PaperMod（社区最大、功能最全）
- 开始环境准备

---

## 4. 维护指南

### 新增文章
```bash
hugo new posts/文章文件名.md
# 编辑 content/posts/文章文件名.md
# 预览：hugo server
# 提交：git add . && git commit -m "..." && git push
```

### 本地预览
```bash
hugo server -D  # -D 显示草稿
```

### 部署到 GitHub Pages
```bash
hugo                    # 生成静态文件
git add . && git commit -m "..." && git push
```

---

## 5. 主题候选列表

| 主题名 | 特点 | 风格 |
|--------|------|------|
| PaperMod | 极简、快速、响应式 | 文字导向 |
| Even | 优雅、简洁 | 博客风格 |
| LoveIt | 功能丰富、深色模式 | 多功能 |
| Stack | 卡片式、现代 | 个人主页 |
| Blowfish | 现代、暗色 | 技术博客 |

> 待定：选择后在此记录具体配置

---

## 6. 待决定事项

- [ ] 网站名称 / 标题
- [ ] 个人简介内容
- [ ] 头像 / Logo
- [ ] 社交链接（GitHub、知乎等）
- [ ] 域名（是否需要自定义域名）
