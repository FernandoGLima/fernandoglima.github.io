---
title: "First Contribution Accepted in GNOME"
date: 2025-06-28 10:00:00 +/-0300
categories: [Open Source Software Development, GNOME contributions]
description: "In this post, I talk about the learning process behind making commits and how I managed to get my first contribution accepted."
tags: [linux, gnome, contribution, open-source, mac0470]
---

In the previous post, I discussed how I worked on issue #3880 in Nautilus and described the process of identifying and fixing the problem. In this section, I will walk through what went wrong during the commit phase, what I learned from the experience, areas where I can improve, and how the contribution was ultimately accepted.

### The flawss in the commit

Writing a clear and well-structured commit message is an essential part of the development process. A good commit message helps maintainers and collaborators understand the purpose of the change quickly, making code review and future maintenance easier. It’s important to follow the project's commit message guidelines, which often include a short, descriptive summary followed by a more detailed explanation if necessary. 

Unfortunately, my first commit message did not fully follow the standard format. While the title and description were clear and well-written, I overlooked an important detail: including the appropriate prefix. These prefixes, often used to indicate the area of the codebase affected or the type of change (e.g., fix:, icon:, docs:), are crucial for maintainers to quickly understand the nature of the commit. This small mistake served as a valuable reminder of the importance of carefully following contribution guidelines to ensure clarity and consistency in collaborative projects.

![Missing prefix]({{ '/assets/img/2025-06-28-First-contribution-Accept/Missing_prefix.png' | relative_url }})
_Missing prefix_

In addition to commits, adhering to the project's code style and double-checking small details—such as indentation, variable naming, and removing unnecessary debug code—can make a significant difference. These practices show attention to detail, reduce the chances of rework, and increase the likelihood of having contributions accepted smoothly.

In this part, I made another small mistake: I accidentally added an extra empty line at the end of one of the files. Although it may seem harmless, this kind of change does not follow the clean code standards of the project and needs to be removed.

![Empty line add]({{ '/assets/img/2025-06-28-First-contribution-Accept/empty_line.png' | relative_url }})
_Empty line add_

### Fixing and Accepted

To resolve this problem, I followed Peter Eisenmann’s suggestion on GitLab and I removed the extra line and edited the commit title directly within the GitLab interface. However, applying the suggestion this way, automatically created a new commit. Ideally, I should have either squashed both commits on GitLab, or—more appropriately—squashed them locally and force-pushed the updated commit history to the branch.

Unfortunately, I didn't catch this in time, but Peter kindly handled it by squashing the commits himself on GitLab so that the contribution could be merged into GNOME 48.3.

![Squash the commits]({{ '/assets/img/2025-06-28-First-contribution-Accept/squash.png' | relative_url }})
_Squash the commits_

But most importantly, the contribution was accepted and successfully fixed the small visual bug in Nautilus. Despite the minor mistakes along the way, this experience was a valuable learning opportunity and a look forward in keep contributing to GNOME.

![Contribution accepted]({{ '/assets/img/2025-06-28-First-contribution-Accept/accepted.png' | relative_url }})
_Contribution Accepted_

> This post is to report our first contributions and interactions with Open Source Development, first started as an assignment on the [Open Source development class](https://uspdigital.usp.br/jupiterweb/obterDisciplina?sgldis=MAC0470&codcur=3122&codhab=5000), at the Institute of Mathematics and Statistics of the University of São Paulo, advised by professor [Paulo Meirelles](https://www.ime.usp.br/~paulormm/).
{: .prompt-info }
