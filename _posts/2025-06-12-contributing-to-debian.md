---
title: "First Contribution to Debian"
date: 2025-06-12 17:00:00 +/-0300
categories: [Open Source Software Development, Debian contributions]
description: "First time interacting with a Debian Enviroment and contribuing through Packaging"
tags: [linux, debian, contribution, open-source, mac0470]
---

This project marked the final assignment of our Open Source Software Development course. As part of the experience, we had the chance to meet and learn from Charles and Lucas Kanashiro, two active contributors and maintainers from Debian Brasil. For this project, we were introduced to the Debian community and encouraged to make a small, meaningful contribution, which is currently awaiting merge.

## Understanding the Debian Project

Debian is a fully open source operating system project that began in 1997. It’s guided by a strong commitment to open collaboration and community-driven development. The project's philosophy centers on giving back to the broader free software ecosystem, making it accessible for contributors worldwide to participate and improve the distribution.

As a Linux distribution, Debian functions by assembling and managing the essential elements of an operating system. This includes not just bundling together core components, but also configuring and distributing them in a way that users can reliably install and run on their machines. 

Debian comprises key components of an OS, including the Linux kernel (whi anages memory, processes, and hardware communication), system libraries like libc, userland tools, a package manager to handle software installation and updates, applications, and a graphical interface. Its modular and reliable structure has made it a foundation for many other distributions, such as Ubuntu, Linux Mint, and others. As a result, contributing to Debian has a wider ripple effect, benefiting users across multiple ecosystems built upon it.

### Packaging

For our contribution, we focused on Debian packaging — the process of preparing software so it can be installed and used by others. Though it might seem simple, packaging involves careful configuration and dependency management to ensure everything works reliably.

We edited two important files: debian/control, which contains metadata about the package including its dependencies, and debian/changelog, which records the history of changes, especially those related to packaging updates. This hands-on experience helped us understand how Debian organizes and distributes software, and how even small contributions support the broader ecosystem.

### The contribution

This was intended as our initial contribution to the Debian project, helping us get familiar with its development workflow. Our task involved a small but important update to the debian/control file, bringing it in line with the current version.

![debian change]({{ '/assets/img/2025-06-12-contributing-to-debian/control.png' | relative_url }})
_Debian Control Standards-Version change_

Afterward, we generated the changelog file and committed our changes to the project.

![Debian changelog]({{ '/assets/img/2025-06-12-contributing-to-debian/changelog.png' | relative_url }})
_Debian changelog_

But we kind did something wrong. Instead of targeting the branch debian/experimental, we target master. But, Lucas Kanashiro come to rescue us and change the target. After that, our commits were merged and we made our first contribution!

![debian MR]({{ '/assets/img/2025-06-12-contributing-to-debian/request.png' | relative_url }})
_Debian merge request_

> This post is to report our first contributions and interactions with Open Source Development, first started as an assignment on the [Open Source development class](https://uspdigital.usp.br/jupiterweb/obterDisciplina?sgldis=MAC0470&codcur=3122&codhab=5000), at the Institute of Mathematics and Statistics of the University of São Paulo, advised by professor [Paulo Meirelles](https://www.ime.usp.br/~paulormm/).
{: .prompt-info }

