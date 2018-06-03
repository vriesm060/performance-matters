# Bootstrap Documentation Site Performance

<!-- Add intro -->

## Setup

<!-- Add setup -->

| First meaningful paint | First interactive  | Score  |
| ---------------------- | ------------------ | ------ |
| 5.420 seconds          | 5.420 seconds      | 64/100 |

**Original waterfall:**
![Original](screenshots/original.png)

**Original audit:**
![Original audit](screenshots/audit-original.png)

## Improvements

### 1. Loading Scripts and fonts.css async
---

By loading all the scripts asynchronous they load at the same time and don't have to wait on one another. This increases the loading speed by 1 second, but it shows the content 2 seconds earlier, which is more important.

By also loading the fonts.css file asynchronous, the content is shown even sooner. It now shows the content 5 seconds earlier than in the original way.

You can find the changes in the [async-loading](../async-loading/AUDIT.md) branch.

| First meaningful paint | First interactive  | Score  |
| ---------------------- | ------------------ | ------ |
| 2.280 seconds          | 6.300 seconds      | 73/100 |
| **-3.140 seconds**     | **+0.880 seconds** | **+9** |

**Waterfall after async loading:**
![After async loading](screenshots/after-async-loading.png)

**Audit after async loading:**
![Audit after async loading](screenshots/audit-after-async-loading.png)

### 2. Minify CSS and JS
---

In order to reduce more loading time I minified the CSS and JS files. I used [CSS Compressor](https://csscompressor.com/) to minify the CSS files and I used [JS Compress](https://jscompress.com/) to minify the JS files.

By doing this I was able to reduce the loading time by 2 seconds and make the content appear 1 second earlier.

You can find the changes in the [minify](../minify/AUDIT.md) branch.

| First meaningful paint | First interactive  | Score  |
| ---------------------- | ------------------ | ------ |
| 4.940 seconds          | 4.940 seconds      | 69/100 |
| **-0.480 seconds**     | **-0.480 seconds** | **+5** |

**Waterfall after minify:**
![Waterfall after minify](screenshots/after-minify.png)

**Audit after minify:**
![Audit after minify](screenshots/audit-after-minify.png)

### 3. Compressing image files
---

By compressing the image files I was able to make the biggest change in loading speed. The overall speed got reduced by 7 seconds. To compress the image files I used [TinyPNG](https://tinypng.com/).

You can find the changes in the [compress-images](../compress-images/AUDIT.md) branch.

| First meaningful paint | First interactive  | Score  |
| ---------------------- | ------------------ | ------ |
| 5.410 seconds          | 5.410 seconds      | 64/100 |
| **-0.010 seconds**     | **-0.010 seconds** | **0**  |

**Waterfall after compressing images:**
![Waterfall after compressing images](screenshots/after-compress-images.png)

**Audit after compressing images:**
![Audit after compressing images](screenshots/audit-after-compress-images.png)

### Merging everything together
---

| First meaningful paint | First interactive  | Score  |
| ---------------------- | ------------------ | ------ |
| 2.060 seconds          | 6.460 seconds      | 79/100 |
| **-3.360 seconds**     | **+1.040 seconds** | **+15**|

**Waterfall after all changes:**
![Waterfall after all changes](screenshots/after-all-changes.png)

**Audit after all changes:**
![Audit after all changes](screenshots/audit-after-all-changes.png)
