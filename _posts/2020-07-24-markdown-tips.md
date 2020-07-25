---
author: jdossgollin
cover:  assets/images/welcome.jpg
date: 2020-07-24 19:00:00
permalink: markdown-how-to
title: How to write blog posts with Markdown
tags: [how-to-contribute]
class: post-template
current: post
layout: post
navigation: True
subclass: 'post'
---

All documents should be formatted in Markdown.
Markdown is easy to use and write!
See some examples [on GitHub](https://github.com/{{ site.username }}/{{ site.repo }}/tree/source/_posts) for examples of other posts.
If you're looking for a Markdown editor, try [VS Code](https://code.visualstudio.com/){:target="_blank"} with the [Markdown Preview Enhanced](https://marketplace.visualstudio.com/items?itemName=shd101wyy.markdown-preview-enhanced){:target="_blank"} extension or [Typora](https://typora.io/){:target="_blank"} for a streamlined experience.

For things like *italics*, **bold** text, `code`, and links see a good [Markdown Cheat Sheet](https://www.markdownguide.org/cheat-sheet/){:target="_blank"}.
There are a few special features worth mentioning.
And if you feel overwhelmed, don't worry -- we're here to help 😎!

### Page Information

At the top of every blog post is a block of information.
For example, the information for this post looks like:

```yml
---
author: jdossgollin
cover:  assets/images/welcome.jpg
date: 2020-07-24 19:00:00
permalink: markdown-how-to
title: How to write blog posts with Markdown
tags: [how-to-contribute]
class: post-template
current: post
layout: post
navigation: True
subclass: 'post'
---
```

Most of them you should copy and paste exactly.
However:

* `author`: If you're writing a post for the first time, create a username and add it with your information to `/_data/authors.yml`. Then set this field to the username you created
* `cover`: an image to use with your post on the homepage
* `date`: Set the date you would like to have associated with your post
* `permalink`: this will be the link to your post so choose something short and unique (no spaces!)
* `tags`: You can add any number of tags to your image. If you're creating a new tag, you should also add a description to `/_data/tags.yml`.
* `title`: The title of your post

### Images

If you're using images, it's **vital** that you post an image that you have permission to share -- we don't want to get in legal trouble!
There are two ways to do this:

1. add an image that you have taken (or that you have permission to share) to the repository (put it in `assets/images` and give it a specific, useful name -- perhaps one that relates to the name of your post). then, link to it as `assets/images/file_name.sufix` when you're including it (see syntax below)
1. embed an image from a site like Wikipedia or Flickr that provides open-access images.

To add an image, you just use regular markdown syntax:

```markdown
![alt text](image-url)
```

If you add `#full` to the end of the image URL, you can get cool full-width images:

```markdown
![full width image of drought](https://upload.wikimedia.org/wikipedia/commons/4/4e/Drought_in_the_Valley.JPG#full)
```

![full width image of drought](https://upload.wikimedia.org/wikipedia/commons/4/4e/Drought_in_the_Valley.JPG#full)

Sites like Flickr also provide code to embed an image.
Copying and pasting in the `html` code from their site gives nice results like:

<a data-flickr-embed="true" href="https://www.flickr.com/photos/bertknot/8180659592/in/gallery-188632717@N05-72157714493410492/" title="maaslant kering (5)"><img src="https://live.staticflickr.com/8200/8180659592_ec99b73c75.jpg" width="500" height="309" alt="maaslant kering (5)"></a><script async src="//embedr.flickr.com/assets/client-code.js" charset="utf-8"></script>

Here's how to link to a local image

```markdown
![stock photo](assets/images/welcome.jpg)
```

![stock photo](assets/images/welcome.jpg)

### Math

You can embed math using [KaTeX](https://katex.org/){:target="_blank"}.
For example,

{% raw %}
```jekyll
{% katex display %}
c = \pm\sqrt{a^2 + b^2}
{% endkatex %}
```
{% endraw %}

will render as

{% katex display %}
c = \pm\sqrt{a^2 + b^2}
{% endkatex %}

See [https://github.com/linjer/jekyll-katex](https://github.com/linjer/jekyll-katex){:target="_blank"_} for more sophisticated syntax including inline math and shortcuts if you're writing a lot of equations.
