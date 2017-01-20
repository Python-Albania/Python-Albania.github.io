---
layout:     post
title:     Algorithms And Data Structure
author:     Geraldo Braho
tags: 		post template
subtitle:  	Some Short Description of Post
category:  project1
---
<!-- Start Writing Below in Markdown -->

# Table of Contents

* TOC
{:toc}

# Linear Search
# Binary Search
# Bubble Sort
# Insertion Sort
# Quick Sort
# Stack
# Queue
# Linked List
# Binary Tree


These are algorithms that students are expected to understand  for A- Level Computing. It is very useful to be able to implement them in a programing language to understand more fully how they work.



## Linear Search

The Linear search is used to find an item in a list. The items do not have to be in order. To search for an item start at the beginning of the list and continue searching until either the end of the list is reached or the item is found.
The algorithm is as follows(given a list called 'List' and looking for an item called 'item')

```python

position <- 0
found <- False
while position < len(List) and not found:
  if List[position] = item:
    found <- True

  position <- position +1


```

## Links

[In-Line](https://www.google.com)

[I'm a reference-style link 1][1]

[I'm a reference-style link 1][2]

[1]:https://www.mozilla.org
[2]:http://www.reddit.com

## Images

Hold your pointer clicked over the image to expand the view.

![Description](http://projectpages.github.io/project-pages/img/Logo_Fairy_Tail_right.png)

## Code

Inline `code`.

{% highlight python %}
import numpy as np
def hello_world():
    print('Hello World!'')
{% endhighlight %}

## MathJax

Use MathJax for Math.
$$ A = \pi r^2 $$

## Tables

Here | is | a | row!
|---------|:----------|:----------:|---------:|
is   |Left|  Center  |Right|
a    | cut | it | A
column  | short | B | C

## Quotes

> War does not decide who is *right*, only who is **left**.

## Rule

---

## HTML

Can write the whole post or sections in HTML for very specific needs. [For the advanced user or the code savvy.]

# Advanced Functionality

Head over to the [documentation page](http://projectpages.github.io/ppguide/) for tutorials on some basic html formatting and some extensions you can use for cool stuff like interactive 3D visualizations.

## Color and Alignment

<p align="center">This text is centered.</p>

<p style="color:red">This is a red text with <span style="color:blue">blue</span> and <span style="color:green">green</span> inline text.</p>

# Some Advanced Features

## Data Projector

<embed src="/project-pages/2016/05/02/New-Projector/" height="500px" width="100%">

## STL

<div align="center"><script src="https://embed.github.com/view/3d/projectpages/project-pages/gh-pages/stl/test.stl"></script></div>
