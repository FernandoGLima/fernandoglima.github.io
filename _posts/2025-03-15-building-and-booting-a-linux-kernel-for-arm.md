---
title: Building and booting a custom Linux kernel for ARM
date: 2025-03-15 09:30:00 +/-0300
categories: [Open Source Software Development, Linux Kernel Environment Setup]
tags: [linux, kernel, kernel-linux, setup, ARM, boot, mac0470]
---

Following our sequence of setup posts for the Linux Kernel contribution environment, now we are following a second tutorial, [Building and booting a custom Linux kernel for ARM using KW](https://flusp.ime.usp.br/kernel/build-linux-for-arm-kw/), on how to compile the Linux Kernel and boot it in the VM that was set up in the previous post.

This tutorial was much more straightforward, shorter, and simpler than the previous one. The first part focused on understanding the structure of the Linux kernel trees. Since the kernel is incredibly complex ,and we’re just undergraduate students having our first real contact with it, we're not cloning all of the Linux trees. Our goal is to contribute specifically to the IIO (Industrial I/O) tree, so that’s the only one we’re cloning onto our machine.

After cloning the IIO tree, the tutorial mainly focused on configuring the Linux kernel for compilation, compiling it, and building it. This part went quite smoothly, without any major issues or errors.

The only issue I had with this tutorial was that, by mistake, I went through the kernel build process without using kw, and had to configure that part separately afterward. Fortunately, it wasn’t a big deal. I'm really enjoying using kw, it’s a tool that significantly streamlines the process.
