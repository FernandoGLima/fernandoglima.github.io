---
title: "First Contribution to GIT"
date: 2025-05-14 17:00:00 +/-0300
categories: [Open Source Software Development, GIT contributions]
description: In this post, we will take a closer look at the GIT MicroProjects"
tags: [linux, git, setup, contributions, open source, mac0470]
---

In the last post, we discussed the incredible history of Git and how it is an essential tool, as well as the impressive ease with which we could compile and make modifications to it. However, one of the critiques we mentioned in the previous post came back to haunt us when we attempted to make our first contribution.

## First Try

As we mentioned earlier, the issue tracker, or the main list, appeared somewhat neglected at first glance. It had very few current open issues, with limited community interaction. After reviewing several issues, we decided to tackle an older one from 2022, which was related to Git's cherry-pick feature. At first, it seemed like a manageable problem for us as a team to address. However, after consulting with the teacher assistant, we realized that it was actually a much larger contribution than we initially anticipated and most likely beyond our current capabilities so we let it go.

## MicroProjects

Realizing that we were somewhat lost and stuck, the course monitor provided us with a recommendation that would change the course of our contribution: the micro-projects. At first, we had understood that this page was intended solely for those participating in the Google Summer of Code (GSoC). However, we were mistaken. This page is also aimed at newcomers who wish to contribute to Git and gain an understanding of how this ecosystem works.

Each year, the Git team curates this page with very small projects, designed as a tutorial and a first step for contributing to this massive project. The projects serve as an introduction to how make their first contribution, teaching contributors how to follow the code guidelines, the correct format for submitting a patch and other important steps in this world of contribution. While the page lists several projects, each person is allowed to work on only one to provide opportunities for other new contributors. Some of the available projects include "Modernize Test Path Checking in Git’s Test Suite," "Fix Sign Comparison Warnings in Git’s Codebase," and "Add More Builtin Patterns for Userdiff," among others.

We chose to contribute to the "Fix Sign Comparison Warnings in Git’s Codebase" project, which simply involves adding certain types of casts, operations that convert a variable from one data type to another, in order to prevent unnecessary warnings. This not only helps in eliminating those warnings but also reduces the likelihood of potential bugs or errors.

Here are the small changes that we made:


After our contributions to the Linux kernel were not accepted, we eagerly awaited the acceptance of these smaller contributions. However, we have not been completely defeated in our efforts with the Linux kernel. Since this modification is so minor, I felt compelled to try again to contribute to the Kernel, but this time focusing on refactoring duplicated code, with the goal of improving the overall quality and maintainability of the code.

> This post is to report our first contributions and interactions with Open Source Development, first started as an assignment on the [Open Source development class](https://uspdigital.usp.br/jupiterweb/obterDisciplina?sgldis=MAC0470&codcur=3122&codhab=5000), at the Institute of Mathematics and Statistics of the University of São Paulo, advised by professor [Paulo Meirelles](https://www.ime.usp.br/~paulormm/).
{: .prompt-info }
