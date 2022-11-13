---
title: "Example content"
description: "Examples for supported content"
author: "Kuravi Hewawasam"
date: 2022-11-05 00:00:00 -0500
tags: [web, jekyll]
mathjax: true
---

This page demonstrates the supported elements of the theme.
The theme is a heavily customized (ruined) version of [Kiko][kiko_link].

Text from [lorem2][lorem2_link].

Lorem ipsum dolor sit amet, consectetuer adipiscing elit.
Donec odio.
Quisque volutpat mattis eros.
Nullam malesuada erat ut turpis.
Suspendisse urna nibh, viverra non, semper suscipit, posuere a, pede.

[kiko_link]: https://github.com/gfjaru/Kiko
[lorem2_link]: https://lorem2.com/

<p class="lead">This is a lead section.
Makes a paragraph stand out.
Donec nec justo eget felis facilisis fermentum.
Aliquam porttitor mauris sit amet orci.
Aenean dignissim pellentesque felis.
</p>

Morbi in sem quis dui placerat ornare.
Pellentesque odio nisi, euismod in, pharetra a, ultricies in, diam.
Sed arcu.
Cras consequat.




<!-------------------------------------------------------------------------------------------------------------------->
## Heading Levels
There are 6 heading levels defined in the SCSS.




<!-------------------------------------------------------------------------------------------------------------------->
## Quote
Praesent dapibus, neque id cursus faucibus, tortor neque egestas auguae, eu vulputate magna eros eu erat.
Aliquam erat volutpat.
Nam dui mi, tincidunt quis, accumsan porttitor, facilisis luctus, metus.
> Phasellus ultrices nulla quis nibh.

Quisque a lectus.
Donec consectetuer ligula vulputate sem tristique cursus.
Nam nulla quam, gravida non, commodo a, sodales sit amet, nisi.



<!-------------------------------------------------------------------------------------------------------------------->
## Code
Code snippets can be include as follows:

``` javascript
function trigger_alert(){
  alert("Lorem Ipsum dolor sit amet");
}

trigger_alert();
```




<!-------------------------------------------------------------------------------------------------------------------->
## Emphasis
Emphasis style are available.
*This text will be italic.*
_This will also be italic._
**This text will be bold.**
__This will also be bold.__
*You **can** combine them too.*




<!-------------------------------------------------------------------------------------------------------------------->
## Unordered lists
Ut convallis, sem sit amet interdum consectetuer, odio augue aliquam leo, nec dapibus tortor nibh sed augue:
* Lorem ipsum dolor sit amet, consectetuer adipiscing elit.
* Aliquam tincidunt mauris eu risus.
* Vestibulum auctor dapibus neque.
* Nunc dignissim risus id metus.
* Cras ornare tristique elit.
* Vivamus vestibulum ntulla nec ante.
* Praesent placerat risus quis eros.



<!-------------------------------------------------------------------------------------------------------------------->
## Ordered lists
Ut convallis, sem sit amet interdum consectetuer, odio augue aliquam leo, nec dapibus tortor nibh sed augue:
1. Lorem ipsum dolor sit amet, consectetuer adipiscing elit.
2. Aliquam tincidunt mauris eu risus.
3. Vestibulum auctor dapibus neque.
4. Nunc dignissim risus id metus.
5. Cras ornare tristique elit.
6. Vivamus vestibulum ntulla nec ante.
7. Praesent placerat risus quis eros.

kramdown
: A Markdown-superset converter

Maruku
: Another Markdown-superset converter




<!-------------------------------------------------------------------------------------------------------------------->
## Image
Lorem ipsum dolor sit amet, consectetuer adipiscing elit.
Donec odio.
Quisque volutpat mattis eros.
Nullam malesuada erat ut turpis.
Suspendisse urna nibh, viverra non, semper suscipit, posuere a, pede.

![Example image](http://via.placeholder.com/200x200?text=Placeholder+image "Example image"){: .center }

Donec nec justo eget felis facilisis fermentum.
Aliquam porttitor mauris sit amet orci.
Aenean dignissim pellentesque felis.




<!-------------------------------------------------------------------------------------------------------------------->
## Table
Morbi in sem quis dui placerat ornare.
Pellentesque odio nisi, euismod in, pharetra a, ultricies in, diam.
Sed arcu.
Cras consequat.


|-----------------+------------+-----------------+----------------|
| Default aligned |Left aligned| Center aligned  | Right aligned  |
|-----------------|:-----------|:---------------:|---------------:|
| First body part |Second cell | Third cell      | fourth cell    |
| Second line     |foo         | **strong**      | baz            |
| Third line      |quux        | baz             | bar            |
|-----------------+------------+-----------------+----------------|
| Second body     |            |                 |                |
| 2 line          |            |                 |                |
|=================+============+=================+================|
| Footer row      |            |                 |                |
|-----------------+------------+-----------------+----------------|

LPraesent dapibus, neque id cursus faucibus, tortor neque egestas auguae, eu vulputate magna eros eu erat.
Aliquam erat volutpat.
Nam dui mi, tincidunt quis, accumsan porttitor, facilisis luctus, metus.




<!-------------------------------------------------------------------------------------------------------------------->
## YouTube
Embedding YouTube video.
Responsive embed picked up from [here](http://coolestguidesontheplanet.com/videodrome/youtube/)

{% include youtube.html id="ML4tw_UzqZE" %}




<!-------------------------------------------------------------------------------------------------------------------->
## Vimeo
Embedding Vimeo video.
Responsive embed picked up from [here](http://coolestguidesontheplanet.com/videodrome/vimeo/)

{% include vimeo.html id="191444383" %}




<!-------------------------------------------------------------------------------------------------------------------->
## SoundCloud
Embedding SoundCloud music

{% include soundcloud.html id=229438479 %}




<!-------------------------------------------------------------------------------------------------------------------->
## Equations
Embedding equations using MathJax

$$
\begin{align*}
x = \frac{-b\pm\sqrt{b^2-4ac}}{2a}
\end{align*}
$$




<!-------------------------------------------------------------------------------------------------------------------->
## GitHub gist
Embedding gists 

{% include gist.html id="89fc6bc6b4fddbb66855809e424d56de" %}




<!-------------------------------------------------------------------------------------------------------------------->
## Javascript canvas
Embedding javascript canvas [Example](https://codepen.io/Munkkeli/pen/PqWBdP)

{% include canvas.html id="canvas_example" script="canvas_example.js" width="100%" height="160px" background="#05BBD3" %}




<!-------------------------------------------------------------------------------------------------------------------->
## SVG
Embedding SVG [Example](https://codepen.io/guerreiro/pen/obhzc)

{% include svg.html width="100%" height="160px" background="#FC0" %}
