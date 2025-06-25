---
title: "First Contribution to GNOME"
date: 2025-06-25 10:00:00 +/-0300
categories: [Open Source Software Development, GNOME contributions]
description: "In this post, we talk about the GNOME Files system Nautilus and the issue 3880"
tags: [linux, gnome, setup, contribution, open-source, mac0470]
---

In the previous post, we prepared our development environment to begin contributing to the GNOME project. Now that this is complete, we can start diving deeper into the project and familiarizing ourselves with its structure. GNOME offers a variety of applications that are thoroughly documented by the maintainers, and for beginners like us, it’s helpful to search for issues labeled newcomers to find accessible entry points.

We chose to contribute to the Nautilus (also known as Files) project. Nautilus is the default file manager for the GNOME desktop environment. It provides a simple and intuitive interface for managing files and folders, supports features like file previews, search, and integration with cloud services, making it an essential tool for everyday desktop use.

### The Issue

Looking for an issue tagged as newcomers on the nautilus, we came across the [issue 3880](https://gitlab.gnome.org/GNOME/nautilus/-/issues/3880). This issue concerns a missing icon problem related to the file transfer completion indicator. It was identified that the icon emblem-ok-symbolic, which Nautilus uses when a file transfer finishes, was removed from the adwaita-icon-theme the icon project of GNOME (specifically at [commit a00466f1](https://gitlab.gnome.org/GNOME/adwaita-icon-theme/-/commit/a00466f12bd5419d6f22c1097a16fd670431c9d4)).

Despite this removal, Nautilus still references this icon in its source code, notably in the [file nautilus-progress-info-widget.c](https://gitlab.gnome.org/GNOME/nautilus/-/blob/8b83ae880c94196ed658a7d7964acbaa67c9324d/src/nautilus-progress-info-widget.c#L55) at line 55, which causes a visual regression where the icon is missing after a file operation completes.

```c
static void
info_finished (NautilusProgressInfoWidget *self)
{
    gtk_widget_set_sensitive (self->priv->button, FALSE);
    if (!nautilus_progress_info_get_is_cancelled (self->priv->info))
    {
        gtk_button_set_icon_name (GTK_BUTTON (self->priv->button), "emblem-ok-symbolic");
        /* Translators: This describes an operation, such as copying or compressing files, as being completed. */
        gtk_widget_set_tooltip_text (GTK_WIDGET (self->priv->button), _("Operation Completed"));
    }
}
```
![Missing Icon]({{ '/assets/img/2025-06-25-First-contribution-to-gnome/Missing_Icon.png' | relative_url }})
_Missing icon_

### Planning how to solve the issue

The problem was cleary, basicaly the emblem-ok-symbolic was deleted from the icon theme, but Nautilus did not update its references accordingly. Interestingly, Jan Tojnar, the maintainer that report this issue, notices that the removed icon is very similar to another symbolic icon called checkmark-small-symbolic available in the icon library and a easy change would be enough.

However, Nautilus also has its own internal icon named file-operation-finished-symbolic.svg with slightly different proportions. This creates uncertainty about which icon should be used going forward—whether to restore the old emblem icon, use Nautilus’s internal icon, or switch to the standard checkmark icon for consistency and better maintainability.

Following this doubt, first i was leaning to use Nautilus’s own icon, file-operation-finished-symbolic, to avoid relying on external icon themes that might change or remove icons. However, i suggest to use to the standard checkmark-small-symbolic, because would be a better approach since it maintains consistent proportions, is a widely accepted icon, and is unlikely to be removed in future icon theme updates.

But Peter Eisenmann, the other maintainer, came up with an even brighter and simpler idea: "You could replace the Nautilus icon with the checkmark-small-symbolic icon and then use it under its new name." This solution was far more elegant in its simplicity.

![Discussion About The Issue]({{ '/assets/img/2025-06-25-First-contribution-to-gnome/discussion_issue.png' | relative_url }})
_Discussion About The Issue_

### Tackling the issue

After Peter’s simple yet effective idea, I just got straight to work. This part was quite straightforward. Basically, the change involved replacing the contents of the file file-operation-finished-symbolic.svg with the data from the removed file emblem-ok-symbolic.svg. Then, I updated the code so that wherever the function emblem-ok-symbolic was called, it would instead refer to file-operation-finished-symbolic.

Once the changes were made, I compiled and ran the project to verify that everything was working correctly. After confirming the modification was successful, I tested it locally to ensure stability. Finally, I wrote the commit message and submitted the merge request for review.

![Icon fixed]({{ '/assets/img/2025-06-25-First-contribution-to-gnome/Icon_fixed.jpg' | relative_url }})
_Icon Fixed_

Now, all that’s left is to wait for the commit feedback.

> This post is to report our first contributions and interactions with Open Source Development, first started as an assignment on the [Open Source development class](https://uspdigital.usp.br/jupiterweb/obterDisciplina?sgldis=MAC0470&codcur=3122&codhab=5000), at the Institute of Mathematics and Statistics of the University of São Paulo, advised by professor [Paulo Meirelles](https://www.ime.usp.br/~paulormm/).
{: .prompt-info }
