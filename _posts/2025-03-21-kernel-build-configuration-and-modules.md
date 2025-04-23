---
title: Linux kernel build configuration and modules
date: 2025-03-21 13:45:00 +/-0300
categories: [Open Source Software Development, Linux Kernel Environment Setup]
tags: [linux, kernel, kernel-linux, setup, ARM, boot, mac0470]
---

As I dive deeper into the world of contributing to the Linux kernel, FLUSP's Tutorial 3 — [Introduction to Linux Kernel Build Configuration and Modules](https://flusp.ime.usp.br/kernel/modules-intro/) — focuses on creating a simple kernel module, configuring the Kconfig and the kernel build using menuconfig, and finally testing everything on the virtual machine.

This tutorial was extremely important for solidifying concepts that hadn’t been entirely clear to me in the previous ones. It also emphasized a crucial point: every time we make changes to the files we’ll be working on, we’ll need to go through this process again, using menuconfig to properly configure the build. This step is essential to ensure the virtual machine still boots correctly and to check whether we've accidentally broken something.
