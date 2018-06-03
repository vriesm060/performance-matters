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

### Loading Scripts and fonts.css async
---

By loading all the scripts asynchronous they load at the same time and don't have to wait on one another. This increases the loading speed by about 1 second, but it shows the content 2 seconds earlier, which is more important.

By also loading the fonts.css file asynchronous, the content is shown even sooner. It now shows the content 3 seconds earlier than in the original way.

These are the new stats:

| First meaningful paint | First interactive  | Score  |
| ---------------------- | ------------------ | ------ |
| 2.280 seconds          | 6.300 seconds	    | 73/100 |
| **-3.140 seconds**     | **+0.880 seconds** | **+9** |

**Waterfall after async loading:**
![Waterfall after async loading](screenshots/after-async-loading.png)

**Audit after async loading:**
![Audit after async loading](screenshots/audit-after-async-loading.png)
