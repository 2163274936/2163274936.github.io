---
title: Windows基于Hugo + GitHub Pages + Cloudflare搭建个人博客
author: 维利翁
date: 2025-05-11T00:00:00+08:00
lastmod: 2025-05-11T00:00:00+08:00
categories:
  - Blog
tags:
  - Hugo
  - GithubPages
  - Blog
summary: windows系统0成本通过Github仓库托管Hugo静态网站生成器最后通过cloudflare自定义域名搭建个人blog
featuredImage: /rbl.png
showSummary: true
draft: false
comments: false
---

# Hugo + GitHub Pages 是什么？

这是将 **Hugo 静态网站生成器** 和 **GitHub Pages 静态网页托管平台** 相结合，用来搭建一个**快速、安全、免费的博客或网站**的组合方案。最后通过Cloudflare配置CNAME 指向 GitHub Pages。确保你能够通过自定义域名访问你的 GitHub Pages 托管的博客。

## 我们需要准备什么？

- 安装 Hugo网站生成器

- 安装Git Bash 命令行工具

- 通过阿里云万网购买域名（可选）

- 创建Github 账号并且搭建public仓库获得github免费三级域名,设置仓库自定义域名(可选)

- 使用`git push` 命令用于将本地 Git 仓库的提交（commit）推送到远程Github仓库

- 创建Cloudflare 账号，添加自定义域名通过Free套餐配置 DNS（CNAME 指向 GitHub Pages）

- 配置GitHub Actions（CI/CD 自动工作流） 自动部署博客

- 使用使用黑曜石（Obsidian）等md笔记工具来写博客文章，配置git插件自动推送
  
  ## 什么是 Hugo？
  
  ### Hugo 是一种**静态网站生成器**

- 使用 Go 语言开发，**速度极快（毫秒级构建）**。

- 不需要数据库，仅通过 Markdown 文件构建网页。

- 通过命令一键将 Markdown 文章转换为 HTML 静态页面。

- 支持主题系统、标签分类、文章分页、目录自动生成、RSS、SEO、短代码等博客功能。
  
  ## 什么是 GitHub Pages？

### GitHub Pages 是 GitHub 提供的**静态网页托管服务**

- 每个 GitHub 用户或组织都可以免费部署一个网站。

- 只要将 HTML、CSS、JS 等静态文件推送到特定分支（如 `gh-pages`），GitHub 会**自动托管并部署**你的网站。

- 支持自定义域名（绑定你自己的 .com/.cn 域名）。

- 默认启用 HTTPS 安全加密，适合搜索引擎抓取。

## 什么是 Cloudflare？

### Cloudflare 是全球最大的 CDN 和 DNS 服务提供商之一

**Cloudflare 最关键、最实用的功能之一就是支持** ✅ **自定义域名绑定**

- 提供DNS服务，Cloudflare 免费提供超快的域名解析服务（极稳定）。

- 提供HTTPS证书 ，自动为你的自定义域名配置 HTTPS（支持自动续期）。

- 提供智能缓存，为你的域名加速内容访问（CDN 全球缓存）。

- 域名跳转，可将 `yourdomain.com` → `www.yourdomain.com`。

- 等等功能 

## 三者结合是如何工作的？

1. **选择静态博客生成器 Hugo**：用于构建博客内容。

2. **选择 GitHub Pages 托管博客**：托管静态文件，免费提供 GitHub Pages 部署。

3. **使用 Git 进行版本控制**：管理博客源代码和文章更新。

4. **配置 GitHub Actions 自动化部署**：每次推送内容时自动构建并部署。

5. **使用 Cloudflare CNAME 指向 GitHub Pages，跳转自定义域名。

6. **使用 Obsidian 撰写博客文章**：本地编辑 Markdown 文件，提升写作效率。

# 正式教程：

**加粗文本** 用于强调重点内容，*斜体文本* 用于表达不同的语气。

1. 有序列表项1
2. 无序列表项2
- 无序列表项1
- 无序列表项2

[链接文本](https://example.com) 可以添加超链接指向其他网页或资源。

图片示例：
![图片描述](images/your-image.jpg)

### 二级小标题

继续丰富文章的内容，按照逻辑和结构进行合理的分段和阐述。

<script defer src="[https://cdn.commento.io/js/commento.js](https://cdn.commento.io/js/commento.js)"></script> <div id="commento"></div>