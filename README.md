# PandasThumb
This repository holds the source code for the Panda's Thumb website.

## Writing a Blog Post

Blog Posts are found in the `\_posts/` directory.  Instructions on how to write them can be found at https://jekyllrb.com/docs/posts/.  Post are written using kramdown (markdown) syntax as described at http://kramdown.gettalong.org/syntax.html.

### Example Blog Post
Create a file called `_posts/2016-11-01-hello-world.md` with the following content:

```
---
title: 'Hello World'
date: '2016-11-01 12:01:00 -07:00'
author: Reed A. Cartwright
---

Hello World
```

### Below the fold
To separate your post into an initial section that appears on the main page and "the rest" insert `<!--more-->` at the point where you want the break to occur.

```
---
title: 'Hello World'
date: '2016-11-01 12:01:00 -07:00'
author: Reed A. Cartwright
---

Hello World

<!--more-->

Just kidding.
```

### Future Posting

If you want your post to run in the future, then put its date into the future. The server runs a cron job every hour that checks to see if anything needs to be published.

### Uploading Images

Upload all images and other content into the `/uploads/[YEAR]/` directory, in markdown you can insert images into your post like so:

```markdown
![Skadoosh](/uploads/2016/slide-kung-fu-panda-3.jpg)
```

![Skadoosh](/uploads/2016/slide-kung-fu-panda-3.jpg)

However, we are still working on the best way to use naked images on the new PT layout, so you should prefer figures for now.

### Figures

Ideally, you should prefer to use figures instead of images; however, figures are not directly supported in Markdown syntax.  However, you can use the following `html` syntax to insert one.

```html
<figure>
<img src="/uploads/2016/slide-kung-fu-panda-3.jpg" alt="Skadoosh"/>
<figcaption>
Skadoosh
</figcaption>
</figure>
```

If you want to use markdown syntax inside the `figure` tag, the Kramdown documentation describes how to do it.  Note that GitHub does not support the `figure` tag, so what you see when you preview your post online will not be the same as the final rendering.

### Sidebar Figures

If you want to specify a `figure`/`img` that floats to the right or left you can use `class="on-the-left-side"` or `class="on-the-right-side"` attributes in the image tag. This will make the figures consume 33% of the content width with fully sized and scale nicely on mobiles.

