---
title: "Environment setup and Learning How to contribute to GIT"
date: 2025-05-06 17:00:00 +/-0300
categories: [Open Source Software Development, GIT contributions]
description: "This is the first post related to contributing to GIT, where we will talk about the struct of GIT and our roadmap to setup the development environment"
tags: [linux, git, setup, contributions, open source, mac0470]
---

Git is an essential tool for anyone involved in software development, especially in open-source projects. It enables developers to efficiently track changes, collaborate on code, and manage different versions of a project. This tool has fundamentally revolutionized the way we produce software, and it will be an honor to contribute, even in a small way, to this incredible and essential tool. Once again, I am teaming up with [Octavio Carneiro](https://o-carneiro.github.io/) and [Lucas Enji](https://eijiuchiyama.github.io/softwarelivre/) to work together and contribute to free software. We chose Git not only because of its rich history, but also due to the incredible presentation by our course monitor, which sparked our interest even more.

In this post, we will discuss how Git's code is structured, how to set up your environment for contributing, and how to tackle ours first issues.

## Struct of the project

The structure of the [Git project](https://github.com/git/git) is available on GitHub in a repository called "git" by the user "git" — so, it's github/git/git, many gits. And it is available under the GNU General Public License version 2.

When we first accessed the repository for the Git files, we were taken aback by the sheer volume of files. It was a bit overwhelming, and at first glance, the repository seemed somewhat disorganized in compare of GNOME. We were particularly surprised by the state of the issue tracker, which appeared to be neglected. There were very few open issues, most of which had been lingering for several years. This lack of activity and organization, especially when compared to the well-maintained structure of the GNOME repository, left us feeling concerned. We worried that this disorganization could potentially hinder our ability to contribute effectively.

However, after thoroughly reviewing the slides from the monitor's presentation, we discovered a website that will be extremely useful on our journey to contribute to this project: [Git Hacking](https://git.github.io/Hacking-Git/). This site contains a wealth of important information, including the complete Git documentation. Additionally, it provides detailed instructions for new contributors, outlining how to modify the code, submit a patch set, and contribute in a clean and efficient manner. We spent hours on the site, reading through the documentation to gain a deep understanding of the correct approach to contributing.

For most of it, we just jumped on reading issues documented as newcomers and looked for one that we could work on.

## Setup

This was by far one of the easiest parts of the entire course. After spending hours setting up the environment so we could configure the VM and make modifications to the Linux kernel, this process was practically instantaneous in comparison. There were no difficulties at all, as it simply involved running the git clone command, followed by a make in the repository. And just like that, we were ready to dive in and start contributing.

> This post is to report our first contributions and interactions with Open Source Development, first started as an assignment on the [Open Source development class](https://uspdigital.usp.br/jupiterweb/obterDisciplina?sgldis=MAC0470&codcur=3122&codhab=5000), at the Institute of Mathematics and Statistics of the University of São Paulo, advised by professor [Paulo Meirelles](https://www.ime.usp.br/~paulormm/).
{: .prompt-info }
