---
title: 我的第一篇笔记
date: 2023-06-15T14:30:00+08:00
draft: true
categories:
  - 学习笔记
tags:
  - Hugo
  - Markdown
description: 介绍如何使用 Hugo 创建笔记网站
---
 
# 我的第一篇笔记

欢迎来到我的技术笔记网站！这个网站使用 [Hugo](https://gohugo.io/) 构建，配合 Markdown 语法记录我的学习过程。

## 为什么选择 Hugo？

选择 Hugo 作为笔记工具的主要原因：

1. **速度快** - 静态网站生成器，毫秒级构建时间
2. **灵活性高** - 支持多种主题和自定义
3. **便于管理** - 纯文本文件，可使用 Git 进行版本控制
4. **Markdown 友好** - 原生支持 Markdown 语法

## 基本使用

创建新笔记的命令：
hugo new posts/your-note-title.md
启动本地服务器预览：
hugo server -D
## 常用 Markdown 语法

### 代码块
def hello_world():
    print("Hello, Hugo!")
    
# 这是一个 Python 示例
### 数学公式

支持 LaTeX 格式的数学公式：

$$E = mc^2$$

### 表格

| 特性   | 支持情况 |
| ---- | ---- |
| 代码高亮 | ✅    |
| 数学公式 | ✅    |
| 流程图  | ✅    |
| 任务列表 | ✅    |

## 下一步计划

- [ ] 添加更多分类和标签
- [ ] 自定义主题样式
- [ ] 配置自动部署到 GitHub Pages
- [ ] 添加评论系统

通过这篇笔记，你可以了解我使用 Hugo 创建笔记网站的基本过程。后续我会记录更多关于开发、学习和生活的内容。    

<% tp.date.now() %>
<% tp.file.creation_date() %>
<% tp.file.last_modified_date() %>
<% tp.web.daily_quote() %>
<% tp.web.random_picture() %>