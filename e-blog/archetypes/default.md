---
title: "{{ replace .Name "-" " " | title }}"
description: "{{ .Name }}"
keywords: "{{replace .Name "-" ","}}"

date: {{ .Date }}
lastmod: {{ .Date }}

categories:
  -
tags:
  -
  -
comment:
  enbale: false
url: "{{ lower .Name }}.html"
toc: true
---

{{ .Name }}

<!--more-->
