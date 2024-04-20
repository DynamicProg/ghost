---
title: "ChatGPT-Next-Web部署流程"
description: "ai-catalog"
keywords: "ai,catalog"

date: 2024-04-17T03:04:49+08:00
lastmod: 2024-04-17T03:04:49+08:00

categories:
  - AI
tags:
  - AI
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
![腾讯云首页](/imgs/ai-server-buy-1.png)
* 实名认证
* 购买[轻量应用服务器](https://cloud.tencent.com/product/lighthouse)
![腾讯云轻量应用服务器](/imgs/ai-server-buy-1.png)
* 选择安装系统Ubuntu 20.04
![腾讯云轻量应用服务器](/imgs/ai-server-buy-2.png)
* 登录启动
![腾讯云轻量应用服务器](/imgs/ai-server-buy-3.png)
* [域名注册](https://dnspod.cloud.tencent.com/)
![域名注册入口](/imgs/ai-server-domain.png)
![域名选择](/imgs/ai-server-domain-buy.png)
![域名购买+信息模版](/imgs/ai-server-domain-buy-2.png)
![域名控制台](/imgs/ai-server-domain-portal.png)
* [云解析DNS](https://cloud.tencent.com/product/dns)
DNS入口
![DNS入口](/imgs/ai-server-dns.png)
DNS配置
![DNS配置](/imgs/ai-server-dns-config.png)
DNS控制台:
![DNS控制台](/imgs/ai-server-dns-portal.png)
* [ICP 备案](https://cloud.tencent.com/product/ba)
备案太麻烦了，先不申请了。。。

## 基础配置
* Ubuntu国内镜像源配置
* SSH配置访问
![访问](/imgs/ai-server-ssh.png)
![Termius](/imgs/ai-server-ssh-login.png)
* GNOME配置桌面
* VNC配置远程桌面
* 服务器防火墙配置
![防火墙](/imgs/ai-server-firewall.png)

## 软件配置
* Docker和Docker-compose安装配置
* Nginx Proxy Manager安装
![NPM访问](/imgs/ai-server-default.png)
* VSCode
* Google Chrome

## 部署和安装
* 获取[OPENAI_API_KEY](https://openai.com/)
* 了解[ChatGPT-Next-Web](https://github.com/ChatGPTNextWeb/ChatGPT-Next-Web)
* Docker安装chatgpt-web，配置docker-compose.yml
* 防火墙和端口配置
* 启动
```l
docker-compose up -d
```

现在就可以使用浏览器，输入 http://ip:port 访问部署的网页版应用了

[示例](http://81.70.81.156:8090/)
