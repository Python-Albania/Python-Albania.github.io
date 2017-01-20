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
# Exercise 1
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

{% highlight python %}

position <- 0
found <- False
while position < len(List) and not found:
  if List[position] = item:
    found <- True

  position <- position +1


{% endhighlight %}





<iframe width="560" height="315" src="https://www.youtube.com/embed/Gf1G1tLkOas" frameborder="0" allowfullscreen></iframe>




## Exercise 1

1. Implement the linear search as described in the video and using the algorithm , test that if it works with the item in and not in the list.
2. Add a counter to report how many searches have been done for each item searched for.
3. Add the Functionality to add an item to the list if not found.
