---
author: jdossgollin
cover:  assets/images/2020-07-24-markdown-tips/cover.jpeg
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

## Page Information

At the top of every blog post is a block of information.
For example, the information for this post looks like:

```yml
---
cover:  assets/images/YYYY-MM-DD-your-title-with-no-spaces/cover.jpg
title: Title for your post
date: YYYY-MM-DD HH:mm:ss
tags: [tag-1, tag-2, tag-3]
author: username # remember when you created an author username? It goes here!
permalink: your-title-with-no-spaces
navigation: True # don't change this
layout: post # don't change this
current: post # don't change this
class: post-template # don't change this
subclass: 'post' # don't change this
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

## Images

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
![stock photo](assets/images/2020-07-24-markdown-tips/cover.jpeg)
```

![stock photo](assets/images/2020-07-24-markdown-tips/cover.jpeg)

## Math

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

## Citations

If you're citing an academic document, you can do so using the [jekyll-scholar](https://github.com/inukshuk/jekyll-scholar){:target="_blank"} plugin.
To do so, you first need to put the bibtex entry for the work you would like to cite in `_bibliography/library.bib`.
For example, add

{% raw %}
```bibtex
@article{doss-gollin_fatalism:2020,
  title = {Adaptation over Fatalism: Leveraging High-Impact Climate Disasters to Boost Societal Resilience},
  author = {{Doss-Gollin}, James and Farnham, David J. and Ho, Michelle and Lall, Upmanu},
  year = {2020},
  volume = {146},
  doi = {10.1061/(ASCE)WR.1943-5452.0001190},
  journal = {Journal of Water Resources Planning and Management},
  number = {4},
  open = {true}
}
```
{% endraw %}

Then I can cite it using
{% raw %}
```jekyll
{% cite doss-gollin_fatalism:2020 %}
```
{% endraw %}
which renders as {% cite doss-gollin_fatalism:2020 %}.
To add a bibliography, just add

{% raw %}
```jekyll
{% bibliography --cited %}
```
{% endraw %}

at the end of your document and it will render as

{% bibliography --cited %}

## Footnotes

You may want to reference some material that isn't an academic paper or clarify a subtle point.
You can do so using footnotes.
To add a footnote to markdown, just type type `[^some_key]` after your text. `some_key` can be a unique identifier for each footnote, since you can have an unlimited number of footnotes.[^1]
Then somewhere below type

```
[^some_key]: This is an example of a footnote
```

and at the bottom of the page it will render as

[^1]: This is an example of a footnote
