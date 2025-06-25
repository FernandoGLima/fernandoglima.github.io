---
title: "First contact to GNOME"
date: 2025-06-20 17:00:00 +/-0300
categories: [Open Source Software Development, GNOME contributions]
description: "This is the first post related to contributing to GNOME, where we will talk about the files project and how to setup the development environment"
tags: [linux, gnome, setup, contribution, open-source, mac0470]
---

The GNOME Project is a free and open-source desktop environment primarily for Linux-based systems. Designed to be simple, user-friendly, and accessible, GNOME offers a clean and modern interface with a focus on productivity and ease of use. 

Undoubtedly, GNOME is one of the most important components of the Linux ecosystem. This was one of the key reasons I chose to contribute to the project.

Additionally, my decision was strongly influenced by several friends—Otavio Silva, Felipe Anibal, and Rodrigo—who had previously contributed and shared very positive experiences. I was also encouraged by the GNOME contribution page, which is extremely well-organized and educational, making it especially welcoming for new contributors.

In this post, we will introduce the GNOME project and how to setup an environment in order to contribute to this project.

### The Files project

The [GNOME welcome page](https://welcome.gnome.org/pt-BR/) is exceptionally well-organized and user-friendly, particularly for newcomers. The website clearly separates the different projects within the GNOME ecosystem, allowing contributors to easily identify where and how they can get involved.

One of its most notable strengths is the availability of basic yet highly effective tutorials. These guides provide a smooth introduction to the contribution process, covering everything from setting up the development environment to submitting the first merge request.
This structured and accessible approach significantly lowers the entry barrier for new contributors, making the GNOME community feel welcoming and inclusive from the very beginning.

When I first started exploring the GNOME projects, I found it somewhat overwhelming due to the large number of open issues across the various repositories. As a newcomer, it was initially difficult to decide where to begin.

However, this initial feeling quickly gave way to a sense of clarity, as I realized how well-documented and well-organized everything is. Each project is clearly structured, with issues consistently labeled using helpful tags such as "newcomer," "bug," or "enhancement." These tags make it much easier to filter tasks according to one’s experience level and interests.

Thanks to this thoughtful organization, what at first seemed complex soon became approachable and manageable and it made me even more motivated to contribute.

![Gnome Files]({{ '/assets/img/2025-06-20-Setting-Enviroment-For-Gnome/Gnome_Files.png' | relative_url }})
_GNOME Files Repository_


### Environment Setup

Setting up the development environment for GNOME is relatively straightforward, especially for users who are already familiar with Linux. The official tutorials provide clear, step-by-step instructions, making the process accessible even to those with limited experience in contributing to open source projects.

One additional requirement is creating an account on GNOME’s GitLab instance and setting up SSH or HTTPS keys in order to securely push code and interact with repositories. This process is also well-documented and easy to follow.

An important tool in the GNOME development workflow is GNOME Builder, an integrated development environment (IDE) specifically designed for GNOME projects. Builder offers built-in support for Flatpak, GNOME SDKs, and project templates, which significantly simplifies building, testing, and running GNOME applications.

At first glance, GNOME Builder can feel a bit confusing due to its unique layout and integration features. However, after a short period of use, it becomes much easier to navigate. Once familiar with its environment, it proves to be an extremely helpful tool that streamlines the development process and enhances productivity.


![Gnome Builder]({{ '/assets/img/2025-06-20-Setting-Enviroment-For-Gnome/Gnome_Builder.png' | relative_url }})
_GNOME Builder_

It is now time to thoroughly review and analyze various open issues with tag 'newcomers' in order to identify suitable tasks to contribute to.

> This post is to report our first contributions and interactions with Open Source Development, first started as an assignment on the [Open Source development class](https://uspdigital.usp.br/jupiterweb/obterDisciplina?sgldis=MAC0470&codcur=3122&codhab=5000), at the Institute of Mathematics and Statistics of the University of São Paulo, advised by professor [Paulo Meirelles](https://www.ime.usp.br/~paulormm/).
{: .prompt-info }
