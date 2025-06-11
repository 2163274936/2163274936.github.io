---
title: Windows手动创建虚拟网卡
author: 维利翁
date: 2025-06-07T00:00:00+08:00
lastmod: 2025-06-07T00:00:00+08:00
categories:
  - Blog
tags:
  - 虚拟网卡
  - Windows
  - virtualNetworkCard
summary: Windows manually creates a virtual network card
featuredImage: /f.jpg
showSummary: true
draft: false
comments: false
lightgallery: true
---

### 在ENSP软件的使用中，我们会遇到使用mobax等连接工具连接虚拟设备的场景，这时就需要创建一张虚拟网卡。   

### Windows键+R 打开运行 输入“hdwwix”添加硬件选项


---

![](posts/hugo-github-virtua%20Network-card/1.png)
### 下一步

---

![](posts/hugo-github-virtua%20Network-card/2.png)
### 选择手动安装

---

![](posts/hugo-github-virtua%20Network-card/3.png)
### 选择网络适配器

---

![](posts/hugo-github-virtua%20Network-card/4.png)
### 选择微软的 KM-Test LoopBack
![](posts/hugo-github-virtua%20Network-card/5.png)

---
### 点击下一步进行安装
![](posts/hugo-github-virtua%20Network-card/6.png)
### 安装完重启一下电脑才有

---

### 运行框输入 ncpa.cpl 打开"网络连接"

![](posts/hugo-github-virtua%20Network-card/7.png)


---

### 高亮处就是我们新建的LoopBack网卡

![](posts/hugo-github-virtua%20Network-card/8.png)