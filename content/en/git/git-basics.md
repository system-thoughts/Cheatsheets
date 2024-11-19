---
title: "git basics"
linkTitle: "git-basics"
date: 2023-01-19
tags: ["git"]
categories: ["git"]
description: >
  This page will cover the git basic useage.
---

{{< card-code header="**rewrite commit's author info**"  lang="bash" >}}
git commit --amend --author="NewAuthor <NewEmail@address.com>"
{{< /card-code >}}


{{< card-code header="**clone repo use specific name instead of original name**"  lang="bash" >}}
git clone <repo_url> <specific_repo_name>
{{< /card-code >}}
