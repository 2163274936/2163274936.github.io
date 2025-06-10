---
title: Centos7.9通过Wordpress搭建电商平台（一）
author: 维利翁
date: 2025-06-10T00:00:00+08:00
lastmod: 2025-06-10T00:00:00+08:00
categories:
  - Blog
tags:
  - Blog
  - 电商
  - WordPress
  - VMWorkstation
  - Centos
summary: Centos7.9 Building an E-commerce Platform with Wordpress (Part One)
featuredImage: /l.png
showSummary: true
draft: false
comments: false
description:
---
大二下的期末实训课我选择了校内实训，老师要求搭建一个美妆的电商平台。思索片刻，我排除了自主开发前后端原始网站的方案。因为大一时我曾用 HTML+PHP 和 Python 开发过校内内网简易网站，深知从零搭建会面临诸多问题：后端逻辑容易出错、前端样式美观度不足且存在兼容性报错、数据库设计逻辑复杂等。基于以往经验，我果断决定采用成熟的平台模板来搭建电商平台。

Wordpress就是一个不错的选择。此前我曾用它搭建过personal blog，虽然后来觉得设计复杂便不再使用，但至少有过一次安装经验，而且我了解到不少实际运营的跨境电商小型网站都基于WordPress 部署，其丰富的高完成度插件和模板能够满足电商平台的功能需求。

  
在环境选择上，我采用了国内高校常用的 CentOS 7 系统，具体版本为 CentOS 7.9（其他 CentOS 版本亦可）。下面正式分享我搭建美妆电商平台的建议。