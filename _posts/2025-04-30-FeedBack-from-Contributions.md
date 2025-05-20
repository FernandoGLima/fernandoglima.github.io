---
title: Feedback on the Patches
date: 2025-04-30 20:30:00 +/-0300
categories: [Open Source Software Development, Kernel contributions]
tags: [linux, kernel, kernel-linux, setup, ARM, boot, mac0470, open-source, iio]
---

In the last post, we showed the small modifications made to a part of the code in the Linux kernel regarding buffer protection, aimed at preventing concurrent access to the device in different modes and avoiding corruption of the buffer data capture. We have now received feedback on both patchs.

If it interests anyone to see, our patch can be found at the [lore platform](https://lore.kernel.org/linux-iio/?q=fernandolimabusiness%40gmail.com). 


## First response

After submitting our contribution to the Kernel mailing list, we received a response from Marcelo Schmitt, an IIO maintainer, who addressed several points. First, unfortunately, we forgot to run get_maintainer.pl to obtain all the expected recipients for this patch. However, he mentioned that the code appears to be syntactically correct. (There was some difficulty on our part running the maintainers tool, but we reviewed the documentation and adhered strictly to the required syntax formats.) 

After that, he then pointed out that the function iio_device_claim_direct() is only used in highly critical parts of the code, and unfortunately, this was not one of them. Furthermore, he indicated that it did not pose a risk to the reading and storage of data in the buffer, nor did it align with best programming practices.

Unfortunately, our contribution was not accepted, and as a team, we agreed that it might not make sense to further argue for its implementation. (However, we found it somewhat odd, as this change was actually suggested by Marcelo himself in the class's pad.)

## Second Feedback

Unfortunately, we received another negative piece of feedback and our contribution was not accepted. This time, after submitting our patch to the Kernel mailing list, we received a response from Jonathan Cameron, who is also an IIO maintainer and is responsible for this part of the code. 

From the start, our submission was flawed, as we accidentally sent it twice to the mailing list due to a typo in Jonathan's email address. He kindly pointed out the error and reminded us to include a message when resubmitting.

Afterward, Jonathan commented that in one of the changes, in his words, "This is a debug accessor. If it is even vaguely possible to access the registers whilst in buffered mode, this might be very useful for debugging." Basically, one part of the code was deemed unnecessary, as it was usefull for debugging purposes. 

In another part, he explained that the implementation did not make sense because it was not a state transition and did not affect the buffer so it should not be implemented. Additionally, he pointed out that some portions of the code did not conform to the "correct kernel code style."

## Third Feedback

Fortunately, there is still one more patch that we submitted, and we remain optimistic about receiving better feedback. As of now, we have not yet received any response regarding this submission.

