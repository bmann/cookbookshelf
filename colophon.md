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

## Recipe & Cookbook Formats

(in progress documentation of the YAML front matter I'm using for the recipe collection)

<s>Deleted aged example of a start at recipe / source formatting</s>

(which is likely better served by looking at the recipe source files)

* [Example Recipe from a Cookbook](https://raw.githubusercontent.com/bmann/cookbookshelf/gh-pages/_recipes/2016-01-24-pork-chops-chickpeas.md)
* [Example of Recipe sourced from a Website](https://raw.githubusercontent.com/bmann/cookbookshelf/gh-pages/_recipes/2012-12-18-biscuits.md)
* [Example Cookbook that the Recipe is from](https://raw.githubusercontent.com/bmann/cookbookshelf/gh-pages/_cookbooks/2016-01-24-indian-cooking.md)

## Cheat Sheet

A few items that are specific to the Long Haul theme, or other things to remember.

See the [example post formatting]({{ '/post/styles' | prepend: site.baseurl }}) for all the styled elements.

Because this is running in a sub-directory, this is needed in relative URLs:

{% highlight liquid %}
prepend: site.baseurl
{% endhighlight %}

## To Do

* <s>A way to separate quantities from ingredient names, both for scaling and in order to pull out major ingredients</s>
    * Short answer: you use an indexed area that looks like this:
 
{% highlight liquid %}
 ingredients:
  - { qty: 2, measure: cups,  name: "flour", extended: "sifted" }
  - { qty: 1, measure: Tbsp, name: "baking soda" }
{% endhighlight %}

 
* An ingredients page that automatically groups recipes based on the ingredients
* Search, which is a bit tricky with Jekyll + GitHub Pages, but can likely use something like [jekyll + lunr.js](https://github.com/slashdotdash/jekyll-lunr-js-search)
* Dive into the quagmire that [Microformats.org has documented about recipe formats](http://microformats.org/wiki/recipe-formats). This is for import / export into recipe apps (e.g. [Paprika uses a YAML Format](http://paprikaapp.com/help/mac/#yamlformat)), grocery lists, etc.