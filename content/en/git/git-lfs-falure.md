---
title: "git lfs clone big file failure"
linkTitle: "git-lfs"
date: 2023-09-14
tags: ["git-lfs"]
categories: ["git"]
description: >
  This page will cover the needs and solutions to rewrite and alter Git history.
---

## git-lfs download big file failure
```bash
Error downloading object: kernel.tar.gz (a49325e): Smudge error: Error downloading kernel.tar.gz (a49325e421068d58a3be21fa7bda9d81f9a5c2747ab51d9df55df38233b02ca9): batch response: Post "xxx": Gateway Time-out

Errors logged to '/home/code/kernel/.git/lfs/logs/20230913T061423.436234732.log'.
Use `git lfs logs last` to view the log.
error: external filter 'git-lfs filter-process' failed
fatal: kernel.tar.gz: smudge filter lfs failed
```

## Solution
1. skip big file download
```bash
# git lfs install --skip-smudge

Git LFS initialized.
```

2. remove error-download repo, clone the same repo once again:
```bash
# rm kernel/ -rf && git clone ssh://git@xx/kernel.git
Cloning into 'kernel'...
remote: Enumerating objects: 157582, done.
remote: Counting objects: 100% (45285/45285), done.
remote: Compressing objects: 100% (32284/32284), done.
remote: Total 157582 (delta 22548), reused 13001 (delta 13001), pack-reused 112297
Receiving objects: 100% (157582/157582), 1.37 GiB | 34.85 MiB/s, done.
Resolving deltas: 100% (48892/48892), done.
```

3. turn off the repo's git SSL config
```bash
cd kernel/ && git config  http.sslverify false
```

4. retry to pull big file
```bash
# git lfs pull
```

5. reinstance LFS, git-lfs download big file finis
```bash
# git lfs install --force

Updated Git hooks.
Git LFS initialized.
```
