---
layout: post
current: post
cover:  assets/images/welcome.jpg
navigation: True
title: How to write blog posts with Markdown
date: 2020-07-24 19:00:00
tags: [how-to-contribute]
class: post-template
subclass: 'post'
author: jdossgollin
permalink: markdown-tips
---

All documents should be formatted in Markdown.
Markdown is easy to use and write!
See some examples [on GitHub](https://github.com/{{ site.username }}/{{ site.repo }}/tree/source/_posts) for examples of other posts.
If you're looking for a Markdown editor, try [VS Code]() with the [Markdown Preview Enhanced](https://marketplace.visualstudio.com/items?itemName=shd101wyy.markdown-preview-enhanced){:target="_blank"} extension or [Typora](https://typora.io/){:target="_blank"} for a streamlined experience.

For things like *italics*, **bold** text, `code`, and links see a good [Markdown Cheat Sheet](https://www.markdownguide.org/cheat-sheet/){:target="_blank"}.
Here are a few special features to mention:

### Page Information

At the top of every blog post is a block of information.
For example, the information for this post looks like:

```
---
layout: post
current: post
cover:  assets/images/welcome.jpg
navigation: True
title: How to write blog posts with Markdown
date: 2017-07-27 10:00:00
tags: [getting-started]
class: post-template
subclass: 'post'
author: ghost
permalink: markdown-tips
---
```

Most of them you should copy and paste exactly.
However:

* `date`: set the date you would like to have associated with your post
* `tags`: you can add more tags to your image

### Images

If you're using images, it's **vital** that you post an image that you have permission to share -- we don't want to get in legal trouble!
There are two ways to do this:

1. add an image that you have taken (or that you have permission to share) to the repository (put it in `assets/images` and give it a specific, useful name -- perhaps one that relates to the name of your post). then, link to it as `assets/images/file_name.sufix` when you're including it (see syntax below)
1. embed an image from a site like Wikipedia or Flickr that provides open-access images:

To add an image, you just use regular markdown syntax:

```
![alt text](image url)
```

If you add `#full` to the end of the image URL, you can get cool full-width images:

```
![walking](https://upload.wikimedia.org/wikipedia/commons/4/4e/Drought_in_the_Valley.JPG#full)
```

![walking](https://upload.wikimedia.org/wikipedia/commons/4/4e/Drought_in_the_Valley.JPG#full)

Sites like Flickr also provide code to embed an image.
Copying and pasting in the `html` code from their site gives nice results like:

<a data-flickr-embed="true" href="https://www.flickr.com/photos/bertknot/8180659592/in/gallery-188632717@N05-72157714493410492/" title="maaslant kering (5)"><img src="https://live.staticflickr.com/8200/8180659592_ec99b73c75.jpg" width="500" height="309" alt="maaslant kering (5)"></a><script async src="//embedr.flickr.com/assets/client-code.js" charset="utf-8"></script>

### Math

We have mathjax so you can use math syntax.
You can have equations on their own:

```
$$E=Mc^2$$
```

$$E=Mc^2$$

and inline math.
But note that

```
inlime math like $$E=mc^2$$ needs two dollar signs
```

inline math like $$E=mc^2$$ needs two dollar signs
