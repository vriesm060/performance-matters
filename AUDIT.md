# Bootstrap Documentation Site Performance

[Go back to master](../master/AUDIT.md)

## Setup

All the audits where done on a Fast 3G internet connection, which was good enough to check the performance on. These were the original stats:

| First meaningful paint | First interactive | Score  |
| ---------------------- | ----------------- | ------ |
| 5.420 seconds          | 5.420 seconds	   | 64/100 |

**Original waterfall:**
![Original waterfall](screenshots/original.png)

**Original audit:**
![Original audit](screenshots/audit-original.png)

## Improvements

### Compressing image files
---

By compressing the image files I was able to make some small changes in loading speed. The overall speed got reduced by 0.010 seconds. To compress the image files I used [TinyPNG](https://tinypng.com/).

These are the new stats:

| First meaningful paint | First interactive  | Score  |
| ---------------------- | ------------------ | ------ |
| 5.410 seconds          | 5.410 seconds	    | 64/100 |
| **-0.010 seconds**     | **-0.010 seconds** | **0**  |

**Waterfall after compressing images:**
![Waterfall after compressing images](screenshots/after-compress-images.png)

**Audit after compressing images:**
![Audit after compressing images](screenshots/audit-after-compress-images.png)
