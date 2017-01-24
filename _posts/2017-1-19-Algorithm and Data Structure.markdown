---
layout:     post
title:     Algorithms And Data Structure
author:     Geraldo Braho
tags: 		Python Algorithm  Data Structure
subtitle:  	A Brief review of sorting and searching in Python
category:  
share: true
comments: true-
---
<!-- Start Writing Below in Markdown -->

# Table of Contents

* TOC
{:toc}





# Linear Search



These are algorithms that students are expected to understand  for A- Level Computing. It is very useful to be able to implement them in a programing language to understand more fully how they work.



## What Is Linear Search

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


<br>


<iframe width="560" height="315" src="https://www.youtube.com/embed/Gf1G1tLkOas" frameborder="0" allowfullscreen></iframe>


<br>

## Exercise 1

1. Implement the linear search as described in the video and using the algorithm , test that if it works with the item in and not in the list.
2. Add a counter to report how many searches have been done for each item searched for.
3. Add the Functionality to add an item to the list if not found.


<br>


<br>

# Binary Search



The binary search is used to find an item in a ordered list.
Let's say we want to find a number in the list below:

{% highlight python %}

1 , 2,4,6,8,20,28,31,34,50

{% endhighlight %}


## What is Binary Search

To search for an item , we look in the middle of list and check if the number we want is in the middle, above the middle or below the middle.If it is in the middle, you have found the item. If it is higher than the middle value, then we adjust the bottom of the list so we can search in a smaller starting point of the list.If the number is lower than the middle value then we adjust the top of the list so that we can search in a smaller list which has it highest position one less then the middle position.


The pseudocode and algorithm is as below:

{% highlight python %}

Found <- False
while not Found and first <= top
    Midpoint <- (First + Last) DIV 2
    If List[Midpoint] = ItemSought Then
        ItemFound <- True
    Else
        If First >= Last Then
            SearchFailed <- True
        Else
            If List[Midpoint] > ItemSought Then
                Last <- Midpoint - 1
            Else
                First <- Midpoint + 1
            EndIf
        EndIf
    EndIf

{% endhighlight %}

<br>
<iframe width="560" height="315" src="https://www.youtube.com/embed/iIU91HCXnpo" frameborder="0" allowfullscreen></iframe>



<br>

## Exercise 2

1. Implement the binary search as shown in the video and test it if it works.
2. Add a counter to report how many searches have been done for each item searched for.


<br>
<br>
