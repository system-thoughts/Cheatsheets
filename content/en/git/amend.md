---
title: "rewriting history"
linkTitle: "amend"
date: 2023-01-19
tags: ["git"]
categories: ["git"]
description: >
  This page will cover the needs and solutions to rewrite and alter Git history.
---

{{< card-code header="**rewrite commit's author info**"  lang="bash" >}}
git commit --amend --author="NewAuthor <NewEmail@address.com>"
{{< /card-code >}}