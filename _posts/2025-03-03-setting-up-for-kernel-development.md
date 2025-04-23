---
title: Setting up a test environment for Linux Kernel
date: 2025-03-03 21:30:00 +/-0300
categories: [Open Source Software Development, Linux Kernel Environment Setup]
tags: [linux, kernel, kernel-linux, setup, qemu, mac0470]
---
I've always been eager to explore the complex world of the Linux kernel and the broader open source movement. However, during my undergraduate studies, I ended up focusing more on other areas such as machine learning, competitive programming, and others. That’s why I decided to enroll in the course [MAC0470 – Desenvolvimento Software Livre](https://uspdigital.usp.br/jupiterweb/obterDisciplina?sgldis=MAC0470), to finally have the opportunity to dive into this fascinating and intricate world.

### Firsts Steps

The first step, and by far the most important one, was installing a Linux system on my computer. I had seen some friends set up dual-boot systems before, but I had never done it myself. Despite the initial nerves, the installation went surprisingly smoothly. I’m especially grateful to two friends who helped me through the process: [Octavio Carneiro] (https://o-carneiro.github.io/) (who will also be my project partner for this course) and [Vinicius Lira] (https://github.com/lira-frts).

After that, it was time to dive deeper into the world of free software. To guide us through this journey, we’re following several tutorials from [FLUSP](https://flusp.ime.usp.br/), an active and important group at IME-USP that focuses on free and open source software. To really get started, the first step was setting up a safe environment where we can modify sensitive kernel files without risking damage to our machines

Following the tutorial [Setting Up a Test Environment Using QEMU and Libvirt](https://flusp.ime.usp.br/kernel/qemu-libvirt-setup/), I was able to understand the key points such as which tools are essential to install, how to configure the virtual machine, and how to prepare the disk image. At first, it was a bit challenging to take it all in, since everything was so new. However, the tutorial is very well written, and after reading it two or three times, things started to be more cleary. Finally, seeing the virtual machine boot up was both a huge relief and a rewarding moment.
