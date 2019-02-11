---
title: "Jekyll tag archive page"
description: "How to generate the tag archive page of this blog"
author: "Kuravi Hewawasam"
date: 2019-02-10 00:00:00 -0500
tags: [web, jekyll]
---

The tag archive page of this blog was created following [this guide][longqian.me_github-jekyll-tag] but with few alterations.
Once the tags are added to your blog using steps one thru five in the guide, [this tag archive page][tag-archive-page] was created instead of a series of pages for each tag as suggested in the guide.
This allows me to bypass the automatic tag generator written in python used in that article.
However, in this setup, posts with multiple tags will repeat under each tag.

First collect the `site.tags` generated with `collecttags.html` to a sorted list

{% raw %}
```liquid

{% capture temptags %}
{% for tag in site.tags %}
{{ tag[1].size | plus: 1000 }}#{{ tag[0] }}#{{ tag[1].size }}
{% endfor %}
{% endcapture %}
{% assign sortedtemptags = temptags | split:' ' | sort | reverse %}

```
{% endraw %}

Then cycle through the tags in `archive.html`.
In it the articles are listed below each tag using the `post` in `site.tags[tagname]`.

{% raw %}
```liquid

{% for temptag in sortedtemptags %}
{% assign tagitems = temptag | split: '#' %}
{% capture tagname %}{{ tagitems[1] }}{% endcapture %}
...
  {% for post in site.tags[tagname] %}
  ...
  {% endfor %}
{% endfor %}

```
{% endraw %}

All occurrences of tags are linked to this archive page with anchors for each tag. eg: [web](/archive.html#web)
For the actual implementation see the [repository][github.repository]






[longqian.me_github-jekyll-tag]: http://longqian.me/2017/02/09/github-jekyll-tag/
[tag-archive-page]: /archive.html
[github.repository]:  http://github.com/kuravih/kuravih.github.io