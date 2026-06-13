# 开发日志

## [2026-06-13] 项目启动
- 确定技术方案：Hugo + GitHub Pages
- 创建项目文档

## [2026-06-13] 环境搭建
- 安装 Hugo Extended v0.163.1（winget）
- 初始化 Hugo 项目：`hugo new site .`
- 安装 PaperMod 主题（git submodule）
- 配置 hugo.toml（中文 locale、导航菜单、暗色模式）
- 创建基础内容：about.md、posts/hello-world.md、timeline.md
- 本地预览成功：13 个页面生成

## [2026-06-13] 部署上线
- 创建 GitHub 仓库：Weixi24/Weixi24.github.io
- 配置 GitHub Actions 自动部署（.github/workflows/deploy.yml）
- 推送代码到 main 分支
- GitHub Pages 启用，网站上线：https://weixi24.github.io

## [2026-06-13] 扩展功能
- 时间线页面：content/timeline.md，导航栏已添加入口
- Giscus 评论系统：
  - 配置 comments.html partial（Giscus script）
  - 修改 single.html 默认开启评论
  - about.md 和 timeline.md 关闭评论
  - 配置 hugo.toml 中 giscus 参数
  - 安装 giscus GitHub App
- 搜索功能：PaperMod 内置，无需额外配置
- RSS 订阅：PaperMod 内置，无需额外配置

## [2026-06-13] 已知问题
- README.md 首页显示为项目文档而非博客列表（已修复：使用 hugo.toml 配置 homeInfoParams）
