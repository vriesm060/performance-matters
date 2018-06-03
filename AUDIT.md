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

### Minify CSS and JS
---

In order to reduce more loading time I minified the CSS and JS files. I used [CSS Compressor](https://csscompressor.com/) to minify the CSS files and I used [JS Compress](https://jscompress.com/) to minify the JS files.

By doing this I was able to reduce the loading time by half a second and make the content appear half a second earlier as well.

These are the new stats:

| First meaningful paint | First interactive  | Score  |
| ---------------------- | ------------------ | ------ |
| 4.940 seconds          | 4.940 seconds	    | 69/100 |
| **-0.480 seconds**     | **-0.480 seconds** | **+5** |

**Waterfall after minify:**
![Waterfall after minify](screenshots/after-minify.png)

**Audit after minify:**
![Audit after minify](screenshots/audit-after-minify.png)
