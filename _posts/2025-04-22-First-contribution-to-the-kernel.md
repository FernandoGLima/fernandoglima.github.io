---
title: First contribution to the kernel
date: 2025-04-16 20:30:00 +/-0300
categories: [Open Source Software Development, Kernel contributions]
tags: [linux, kernel, kernel-linux, setup, ARM, boot, mac0470, open-source, iio]
---

Alongside [Octavio Carneiro](https://o-carneiro.github.io/) and Lucas Eiji, I have just sent my first contribution to the Linux Kernel, on the IIO Tree. The two modifications we made weren’t major, in fact, they were extremely simple and involved adding just a few lines of code. However, they might have a very very small impact, as they aim to avoid interleaving register reads/writes with buffered data capture.

### Both Contribution

Both contribution consists of adding the function iio_device_claim_direct() to be called in some cases, to prevent concurrent access of the device in differente modes. The sudden mode change can screw up the buffer data capture by injecting config bytes in the readings.
This added function acts as some sort of “mutex” that locks the mode of the device and prevents this.

Here’s an in-code example of the first change:

```c
static int ad4000_write_raw_get_fmt(struct iio_dev *indio_dev,
				    struct iio_chan_spec const *chan, long mask)
{
	switch (mask) {
	case IIO_CHAN_INFO_SCALE:	
		if (!iio_device_claim_direct(indio_dev)) /*Part modified*/ 
			return -EBUSY;
		
		iio_device_release_direct(indio_dev);
		return IIO_VAL_INT_PLUS_NANO;
	default:
		return IIO_VAL_INT_PLUS_MICRO;
	}
}
```

Here’s the other change change:
```c
static int ads131e08_debugfs_reg_access(struct iio_dev *indio_dev,
                                        bool readval, u8 reg, u8 writeval)
{
    struct ads131e08_state *st = iio_priv(indio_dev);

    if (!iio_device_claim_direct(indio_dev))
        return -EBUSY;

    if (readval) {
        int ret = ads131e08_read_reg(st, reg);
        *readval = ret;
        return ret;
    }

    iio_device_release_direct(indio_dev);
    return ads131e08_write_reg(st, reg, writeval);
}
```

The whole patchest was basically this change in 2 more places: 
 - In ad4000.c write_raw_get_fmt()
 - In ads131e08.c ads131e08_trigger_handler(), but we're not so sure about this change and still gonna talk with the TA.

### PatchSet

This was the most challenging part. Before making the changes, I forgot to run a git pull, which made the git rebase process more difficult later on as I tried to get everything in order. Another tricky part was writing the commit message and following all the formalities of submitting a patchset since even the smallest mistake can lead to the patch being rejected. Now, all that’s left is to wait for feedback from the TA(teacher assistant) and, eventually, from the maintainers.

### Future Contributions

Unfortunately, in the last week, I had to prioritize other courses that gonna be either in exam week or had pending assignments, so I wasn’t able to work on additional issues. However, since the ones we tackled were resolved quickly and easily, we definitely plan to take on more in the future. At the moment, we’re working on a third issue, which involves refactoring code with a high level of similarity and duplicated sections (pressure/dps310.c::dps310_read_pressure AND pressure/dps310.c::dps310_read_temp).
