---
title: "Example content"
description: "Examples for supported content"
author: "Kuravi Hewawasam"
date: 2018-12-22 00:00:00 -0500
tags: [web, jekyll]
mathjax: true
---

This page demonstrates the supported elements of the theme.
The theme is a heavily customized (ruined) version of [Kiko][kiko_github].

Text from [Bob ross lipsum generator][bobrosslipsum].
This is a regular paragraph.
We wash our brush with odorless thinner.
All you have to do is let your imagination go wild
A little happy sunlight shining through there.

[bobrosslipsum]: https://www.bobrosslipsum.com/
[kiko_github]: https://github.com/gfjaru/Kiko

<p class="lead">This is a lead section.
Makes a paragraph stand out.
Let the paint work.
I really recommend you use odorless thinner or your spouse is gonna run you right out into the yard and you'll be working by yourself.
It's so important to do something every day that will make you happy.
</p>

Let's put some happy little clouds in our world.
I spend a lot of time walking around in the woods and talking to trees, and squirrels, and little rabbits and stuff.
Anyone can paint.
I'm sort of a softy, I couldn't shoot Bambi except with a camera.





## Heading Levels
There are 6 heading levels defined in the SCSS.





## Quote

I sincerely wish for you every possible joy life could bring.
We spend so much of our life looking - but never seeing.
And I know you're saying
> Oh Bob, you've done it this time

And you may be right.





## Code
Code snippets can be include as follows:

``` javascript
function trigger_alert(){
  alert("Lorem Ipsum dolor sit amet");
}

trigger_alert();
```





## Emphasis
Emphasis style are available.
*This text will be italic.*
_This will also be italic._
**This text will be bold.**
__This will also be bold.__
*You **can** combine them too.*





## Unordered lists
I'll go over the colors one more time that we use:
* Titanium white
* Thalo green
* Prussian blue
* Van Dyke brown
* Alizarin crimson
* Sap green
* Cad yellow
* Permanent red





## Ordered lists
I'll go over the colors one more time that we use:
1. Titanium white
2. Thalo green
3. Prussian blue
5. Van Dyke brown
6. Alizarin crimson
7. Sap green
8. Cad yellow
9. Permanent red

kramdown
: A Markdown-superset converter

Maruku
: Another Markdown-superset converter





## Image
Be careful. You can always add more - but you can't take it away.
We have a fantastic little sky! Little trees and bushes grow however makes them happy. 

![Example graph](http://via.placeholder.com/200x200?text=Placeholder+image "Example image"){: .center }

How do you make a round circle with a square knife? That's your challenge for the day.
It all happens automatically.





## Figure
Figures with captions.

{% include figure.html image="/assets/img/cgplot_example_5.png" caption="A description of this figure" alt="Graph" class="center" %}

At home you have unlimited time.
That's what makes life fun.
That you can make these decisions.
That you can create the world that you want.
Maybe, just to play a little, we'll put a little tree here.
Just a little indication.





## Table
Use what happens naturally, don't fight it. See there, told you that would be easy.
Learn when to stop.
Life is too short to be alone, too precious.
Share it with a friend.

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

Let your imagination be your guide.
It looks so good, I might as well not stop.
Now then, let's play.
Tree trunks grow however makes them happy.





## YouTube
Embedding YouTube video.
Responsive embed picked up from [here](http://coolestguidesontheplanet.com/videodrome/youtube/)

{% include youtube.html id="ML4tw_UzqZE" %}





## Vimeo
Embedding Vimeo video.
Responsive embed picked up from [here](http://coolestguidesontheplanet.com/videodrome/vimeo/)

{% include vimeo.html id="191444383" %}





## SoundCloud
Embedding SoundCloud music

{% include soundcloud.html id=229438479 %}





## Equations
Embedding equations using MathJax

$$
\begin{align*}
x = \frac{-b\pm\sqrt{b^2-4ac}}{2a}
\end{align*}
$$





## GitHub gist
Embedding gists 

{% include gist.html id="89fc6bc6b4fddbb66855809e424d56de" %}






## Javascript canvas
Embedding javascript canvas [Example](https://codepen.io/Munkkeli/pen/PqWBdP)

{% include canvas.html id="canvas_example" script="canvas_example.js" width="100%" height="160px" background="#05BBD3" %}






## SVG
Embedding SVG [Example](https://codepen.io/guerreiro/pen/obhzc)

{% include svg.html width="100%" height="160px" background="#FC0" %}
