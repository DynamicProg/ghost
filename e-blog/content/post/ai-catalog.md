---
title: "ChatGPT-Next-Web部署流程"
description: "ai-catalog"
keywords: "ai,catalog"

date: 2024-04-17T03:04:49+08:00
lastmod: 2024-04-17T03:04:49+08:00

categories:
  - ai
tags:
  - ai
  - catalog

comment:
  enable: false
url: "post/ai-catalog.html"
toc: true
weight: 2
---

网页版ChatGPT应用环境配置和部署流程
// TODO 待补充下列各节点细节

<!--more-->

GitHub上[ChatGPT-Next-Web](https://github.com/ChatGPTNextWeb/ChatGPT-Next-Web)是热门开源项目，通过ChatGPT-Next-Web可以一键部署一个自己的ChatGPT应用。

## 服务器

建议购买[腾讯云](post/ai-catalog.html)或[阿里云](https://cn.aliyun.com/)，这里以[腾讯云](post/ai-catalog.html)举例

### 购买流程
* 登录[腾讯云](post/ai-catalog.html)
* 实名认证
* 购买[轻量应用服务器](https://cloud.tencent.com/product/lighthouse)
* 选择安装系统Ubuntu 20.04
* 登录启动
* [域名注册TODO](https://dnspod.cloud.tencent.com/)

## 基础配置
* Ubuntu国内镜像源配置
* SSH配置访问
* GNOME配置桌面
* VNC配置远程桌面
* 服务器防火墙配置

## 软件配置
* Docker和Docker-compose安装配置
* Nginx Proxy Manager安装
* VSCode
* Google Chrome

## 部署和安装
* 获取[OPENAI_API_KEY](https://openai.com/)
* 了解[ChatGPT-Next-Web](https://github.com/ChatGPTNextWeb/ChatGPT-Next-Web)
* Docker安装chatgpt-web，配置docker-compose.yml
* 防火墙和端口配置
* 启动
```
docker-compost up -d
```

现在就可以使用浏览器，输入http://ip:port访问了部署的网页版应用了
[示例](http://81.70.81.156:8090/)
