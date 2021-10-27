# Code 401 - Reading Notes

<!-- All references used were from Code 401 reading
assignment 28 -->
[comment]: <> (https://developer.android.com/guide/topics/ui/layout/recyclerview#java)
## RecyclerView

RecyclerView makes it easy to efficiently display large sets of data. You supply the data and define how each item looks, and the RecyclerView library dynamically creates the elements when they're needed.

As the name implies, RecyclerView recycles those individual elements. When an item scrolls off the screen, RecyclerView doesn't destroy its view. Instead, RecyclerView reuses the view for new items that have scrolled onscreen. This reuse vastly improves performance, improving your app's responsiveness and reducing power consumption.


[BACK TO HOME](../README.md)