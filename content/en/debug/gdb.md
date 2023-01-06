---
title: "gdb"
linkTitle: "gdb"
date: 2023-01-05
tags: ["gdb"]
categories: ["debug"]
description: >
  GDB, the GNU Project debugger, allows you to see what is going on inside another program while it executes -- or what another program was doing at the moment it crashed.
---


{{< cardpane >}}
  {{< card-code header="gdb launch program"  title="trace the program execution process to understand code" lang="bash" >}}
    $ gdb <program>
  {{< /card-code >}}
  {{< card-code header="gdb debug coredump file" title="coredump problem location" lang="bash" >}}
    $ gdb <program> <coredump_file>
  {{< /card-code >}}
  {{< card-code header="gdb debug running program" title="debug daemon/infinite loop program" lang="bash" >}}
    $ gdb <program> <pid> # method 1: <pid> represents process pid
    $ gdb -p <pid> # method 2: <pid> use -p option to ignore <program>
    (gdb) attach <pid> # method 3: launch gdb first, then use gdb attach command
  {{< /card-code >}}
{{< /cardpane >}}