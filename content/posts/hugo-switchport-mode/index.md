---
title: 交换机常见端口模式Access、Hybrid、Trunk 区别
author: 维利翁
date: 2025-05-21T13:00:00+08:00
lastmod: 2025-05-21T13:00:00+08:00
categories:
  - Blog
tags:
  - Hugo
  - GithubPages
  - Blog
description: 在网络交换机配置中，Access、Hybrid 和 Trunk 是 VLAN（虚拟局域网）端口的三种不同模式，主要用于处理 VLAN 标签和数据帧的转发。
featuredImage: /d.png
showSummary: true
draft: false
comments: false
lightgallery: true
---
# 以下仅属于言简意赅的概念介绍：

### 什么是VLAN？
-  **VLAN（虚拟局域网）**：在物理网络上通过逻辑划分创建的虚拟独立网络，隔离流量，提高安全性和管理效率。
### 什么是以太网？
-  以太网是一种局域网技术，基于 IEEE 802.3 标准.用于设备间传输数据。
### 什么是数据帧？
-  **数据帧**：以太网传输的基本数据单位，包含源/目的 MAC 地址、数据负载和校验信息。
### 什么是tag标签？
-  **Tag 标签**：VLAN 标签是一个加在数据帧上的“身份证”，标明它属于哪个 VLAN，方便交换机识别和分发。
# 正篇：

### Access端口 通常连接到终端设备（计算机、打印机等）只属于一个VLAN。

## 工作机制

## 1.接收数据帧：

### Access端口接收的以太网帧通常是无vlan标签的（untagged）

-  交换机会为收到的无标签帧自动打上Access口配置的pvid（默认vlan id）将其归属到对应的vlan
- 若收到带有标签的帧（tagged）Access端口通常会丢弃，因为极大多数情况下它只处理无标签帧。
## 2.发送数据帧：

-  Access端口发送的数据帧会去除VLAN标签，以普通以太网数据帧（untagged）形式发送给终端设备。因为大多数终端设备不能处理有tagged的数据帧。
### Trunk 端口是在交换机中用于处理多个VLAN流量的一种端口模式。它可以同时承载多个VLAN。通常用于连接交换机之间、交换机与路由器，或支持 VLAN 的设备（如服务器）。通过 **VLAN 标签（802.1Q）**区分不同 VLAN 的流量。

## 工作机制

## 1.接收数据帧：

有标签帧（Untagged Frames）：
- 接收到的帧带有 802.1Q 标签（4 字节，包含 VLAN ID，如 VLAN 10）。
- 交换机根据 VLAN ID 将帧转发到对应 VLAN。
- 
无标签帧（Untagged Frames）：
- 如果收到无标签帧，Trunk 端口会将其归到 **Native VLAN **（中文翻译一般为本征VLAN，通常是 VLAN 1，可手动配置）。
- 例如：无标签帧收到后，分配到 VLAN 1。
## 2.发送数据帧：

