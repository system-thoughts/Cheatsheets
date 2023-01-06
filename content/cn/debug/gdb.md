---
title: "gdb"
linkTitle: "gdb"
date: 2023-01-05
tags: ["gdb"]
categories: ["debug"]
description: >
  GDB是GNU项目开发的调试器，用户使用gdb观测当前运行程序的状态，或者观测程序崩溃时的状态。
---


{{< cardpane >}}
  {{< card-code header="gdb启动程序"  title="跟踪程序执行过程，理解代码" lang="bash" >}}
    $ gdb <program>
  {{< /card-code >}}
  {{< card-code header="gdb调试coredump文件"  title="coredump问题定位" lang="bash" >}}
    $ gdb <program> <coredump_file>
  {{< /card-code >}}
  {{< card-code header="gdb调试正在运行的程序"  title="调试守护进程/死循环程序" lang="bash" >}}
    $ gdb <program> <pid> # 方法一： <pid>表示进程pid
    $ gdb -p <pid> # 方法二： 使用-p选项，忽略<program>
    (gdb) attach <pid> # 方法三： 先启动gdb，利用gdb attach命令便可attach到调测进程
  {{< /card-code >}}
{{< /cardpane >}}
