---
title: "修改历史记录"
linkTitle: "amend"
date: 2023-01-19
tags: ["git"]
categories: ["git"]
description: >
  介绍修改Git历史记录的需求及其相应的解决方案。
---

{{< card-code header="**修改提交的作者信息**"  lang="bash" >}}
git commit --amend --author="NewAuthor <NewEmail@address.com>"
{{< /card-code >}}