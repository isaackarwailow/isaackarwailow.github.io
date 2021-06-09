---
layout: post
author: Isaac Low
title: Algorithmic questions
---

In preparing for my coding interviews, I thought I should challenge myself with answering some questions on this blog.
[Data Science Interviews](https://awesomeopensource.com/project/alexeygrigorev/data-science-interviews) should have
3 categories of coding interview

1. Python
2. SQL
3. Algorithms

Perhaps they dont even ask about algorithms and data structures. But better safe than sorry.
A good resource on algorithms can be found [here](https://awesomeopensource.com/project/kdn251/interviews#algorithms).

*Question: What is a binary search?*

Personally, I think they would ask more on binary search trees, but we'll stick with this one as it is only a primer.

**Answer: binary search is an algorithm that takes O(log n) time to search an index item. It is usually used to speed up the
search on a linked list**

For those that are new, I suggest reading about Big O notation. Basically there is

* O(n) --> linear time
* O(log n) --> log time
* O(n!) --> factorial time
* O(n* log n) --> quicksort
* O(n**2) --> selection sort

Then it is a matter of understanding how random access and sequential access applies to arrays and linked lists. Here is a code
that I borrowed from a resource to understand binary search programmatically. Note to self: More code, less typing.

```python
def binary_search(list, item):
    low = 0
    high = len(list) - 1

    while low <= high:
        mid = (low + high)
        guess = list[mid]
        if guess == item:
            return mid
        if guess > item:
            high = mid - 1
        else:
            low = mid + 1
    return None

my_list = [1, 3, 5, 7, 9]

print(binary_search(my_list, 3))
print(binary_search(my_list, -1))
```