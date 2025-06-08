---
title: 路由协议基础
author: 维利翁
date: 2025-06-09T00:00:00+08:00
lastmod: 2025-06-09T00:00:00+08:00
categories:
  - Blog
tags:
  - Blog
description: Fundamentals of Routing Protocols
featuredImage: 
showSummary: false
draft: false
comments: false
lightgallery: true
---

# 路由分类

按照路由来源，分为三类： 
（1）直连路由。由链路层协议发现，无需配置。接口存在IP地址时，路由进程自动生成。只能发现本接口所属网段路由。
（2）静态路由。无开销，配置简单。但在发生网络故障的时候，静态路由不会自动修正。必须管理员介入 。
（3）动态路由。动态路由协议发现和维护的路由成为动态路由。无需手动配置具体路由表项，由路由协议自动发现和计算。支持路由备份。如原有链路故障导致路由表项失效，协议可自动计算和使用另外路径，无需人工维护。但动态路由会一部分链路开销。
