#Class 2: Charting and intent; one dataset two ways

Here's what we'll do today:

"SOFT" (non-technical)
  - Think about projects 

"HARD" (more technical)
  - Get more experience with d3 selections, data joins and axes
  - Complete a fully functional scatterplot with last week's data
  - Load data asynchronously with d3.tsv
  - Javascript array manipulation
  - Hosting with bl.ocks.org

Documentation pages that may be useful today:

[SVG](https://developer.mozilla.org/en-US/docs/Web/SVG):
  - [g](https://developer.mozilla.org/en-US/docs/Web/SVG/Element/g)
  - [text](https://developer.mozilla.org/en-US/docs/Web/SVG/Element/text)
  - [circle](https://developer.mozilla.org/en-US/docs/Web/SVG/Element/circle)

[D3](https://github.com/mbostock/d3/wiki):
  - [d3.tsv](https://github.com/mbostock/d3/wiki/CSV#tsv)
  - [d3.svg.axis()](https://github.com/mbostock/d3/wiki/SVG-Axes)
  - [d3.select()](https://github.com/mbostock/d3/wiki/Selections#d3_select)
  - [d3.selectAll()](https://github.com/mbostock/d3/wiki/Selections#d3_selectAll)
  - [d3.extent](https://github.com/mbostock/d3/wiki/Arrays#d3_extent)
  - [selection.data()](https://github.com/mbostock/d3/wiki/Selections#data)
  - [ordinal.rangeRoundBands()](https://github.com/mbostock/d3/wiki/Ordinal-Scales#ordinal_rangeRoundBands)

Plain JS
  - [Array.map](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map)

##Housekeeping
 * Before we start, any questions about technical aspects of last time? We'll try be less rote today.  
 * Chat about the [medium post](https://medium.com/@hint_fm/design-and-redesign-4ab77206cf9) – particularly the Tufte  
 * *Projects/assignment*: Think about what you might want to do for your (optional) Project. 

##Revisiting last week's progress
We worked with `d3.select()` and `d3.selectAll()`; we made our first data join; we altered attributes of DOM elements, we created elements with `append()`.

Today, we're going to plot our data from last week and get familiar with all the standard methods and components of almost any D3 chart. If things go well, ours could even be an improvement on what we could get in five minutes with Excel.

We made it pretty far [last time](index2.html), but let's start (somewhat) from the beginning again, as these are fundamental steps we'll be doing for (almost) every d3 chart:

1. Clear out or start a new `index.html` that loads D3, either locally or from its source. It should look like this:

```
  <!DOCTYPE html>
  <meta charset="utf-8">

  <style type="text/css">
    /*css to go here*/
  </style>

  <body></body>

  <script src="https://cdnjs.cloudflare.com/ajax/libs/d3/3.5.5/d3.min.js" charset="utf-8"></script>

  <script>
    //JS to go here
  </script>

```

2. Navigate to your current folder (say, `metis/class2` and fire up a local server).


##Picking up where we left off

1. Clear out or start a new `index.html`. 

2. Make a Javascript object out of your tabular data and make sure you know how to manipulate it. (This is an annoying but useful exercise in getting useful in a text editor.) I'll use the data from the group number II, but you should chart whatever you drew.

2. Add an SVG element of width 720 and height 400.

3. Using a data join, add a circle for every element of our array. Give it a radius 5 and a class, `anscombe-circle'. Inspect it in the browser. To start, I like to put a pink border around the SVG to make sure I knew it drew:

  ```
  svg {
    border: 1px solid #f0f;
  }
  ```

4. Position the circles based on their `x` and `y` attributes. How does SVG interpret these positions?

5. We need a [scale](https://github.com/mbostock/d3/wiki/Quantitative-Scales#linear-scales). Let's add one. 

6. Let's label the coordinate positions of each using text. Is another data join really necessary?

7. Redo the original join, using groups first, then appending circles and text. Note SVG [transformation](http://www.w3.org/TR/SVG/coords.html) documentation, which is not that fun. 

8. Maybe [axes](https://github.com/mbostock/d3/wiki/SVG-Axes) are in order? The built-in components are a little clunky, and [Gregor Aisch](https://twitter.com/driven_by_data) prefers not to use them at all, but you have to know the rules before you break them, so let's use them for now.  

9. We might need to move our axes around. We'll go through the math. Also, it looks horrible unstyled. Let's inspect it and fix, using CSS. Scott Murray [can help](http://chimera.labs.oreilly.com/books/1230000000345/ch08.html#_cleaning_it_up).

10. The margins are a problem, and they will always be. Here's [a great trick](https://bl.ocks.org/mbostock/3019563) we'll use on every chart we make from here on out.

11. Let's style the chart to match our drawing. Things like [tickSize](https://github.com/mbostock/d3/wiki/SVG-Axes#tickSize) might help.

12. Let's make this a block before time runs out, using git and Github. Add a thumbnail and check out your own bl.ocks page! [Not bad](http://bl.ocks.org/kpq/585b89ff4657dcb35dc1)!

##If there's time/getting more advanced

1. Add `p` tags under the chart for the mean of x and y, and the variance of each. Calculate them dynamically.

2. Load your data dynamically instead of using a variable. (Why would we want to do that?) Here's [a tsv](quartet.tsv) to get you started. You might need to filter your data before plotting your quartet. (And you might have to coerce the data!)

3. So far, after 100 lines of code, our chart isn't really better than what we get with the free tools. (Paste your data into [Chartbuilder](http://quartz.github.io/Chartbuilder/) and feel free to weep.) What makes D3 different is its ability to create **dynamic** visualizations and things that tools aren't designed to create. A scatterplot is simple to make a widget for; [other forms](http://www.nytimes.com/newsgraphics/2013/09/28/eli-manning-milestone/), less so.

 To push this further, abstract our chart out by making a function that updates the chart given a group id, including updating the text fields for averages. Fire the function (and update the chart) every three seconds.

4. If you're really interested in doing stats in Javascript, calculate the Pearson Coefficient and best-fit line and update both in your function. 


## For Wednesday
 * Publish your visualization of Anscombe's Quartet
 * Review [this code](anscombe.html), and come to Wednesday with any questions you might have



