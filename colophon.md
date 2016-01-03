---
layout: default
title: Colophon
---

<h1 class="pageTitle">Colophon</h1>

<p class="intro">I want to keep track of recipes that I use, as well as where I source them. I tend to bookmark links under the <a href="http://tumblr.bmannconsulting.com/tagged/recipe">recipe tag on my Tumblr</a>, but that doesn't give me a copy of them, nor does it let me search them by ingredient.</p>

It is my understanding that the list of ingredients are not copyrightable, so I include them from the source. The cooking directions must be followed from the source blog or cookbook.



## Header

<figure>
    <img src="{{ '/assets/img/eat_this_everyday.jpg' | prepend: site.baseurl }}" alt="I could eat this everyday">
    <figcaption>Detail from "Cooking in Switzerland" (<a href="https://www.flickr.com/photos/boris/4317109573">Photo by me on Flickr</a>)</figcaption>
</figure>

## Features

* [Jekyll 3](http://jekyllrb.com)
* [Long Haul Theme](https://github.com/brianmaierjr/long-haul)
* Hosted on [GitHub Pages](https://pages.github.com/) (source repo [bmann/cookbookshelf](https://github.com/bmann/cookbookshelf))

## Recipe Format

(in progress documentation of the YAML front matter I'm using for the recipe collection)

* title:  "Example Recipe"
* image: example.jpg _// image local to /assets/img_
* source-url: http://example.com
* source-name: "Name of Remote Source Example Recipe"
* source-author: John Doe
* source-book: Name of Cookbook or Magazine
* source-book-page: Page Number
* ingredients: qty ingredient1

## Cheat Sheet

A few items that are specific to the Long Haul theme, or other things to remember.

See the [example post formatting]({{ '/post/styles' | prepend: site.baseurl }}) for all the styled elements.

Because this is running in a sub-directory, this is needed in relative URLs:

{% highlight liquid %}
prepend: site.baseurl
{% endhighlight %}

## To Do

* A way to separate quantities from ingredient names, both for scaling and in order to pull out major ingredients
* An ingredients page that automatically groups recipes based on the ingredients
* Search, which is a bit tricky with Jekyll + GitHub Pages, but can likely use something like [jekyll + lunr.js](https://github.com/slashdotdash/jekyll-lunr-js-search)
* Dive into the quagmire that [Microformats.org has documented about recipe formats](http://microformats.org/wiki/recipe-formats). This is for import / export into recipe apps (e.g. [Paprika uses a YAML Format](http://paprikaapp.com/help/mac/#yamlformat)), grocery lists, etc.