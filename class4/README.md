#Class 4: Abstracting functions, discussing merits of chart forms; d3.nest()

Mmmmmmm Barley

##Housekeeping
Show + tell?
Any questions from Wednesday?
Projects & Pace

Resources on transforming and nesting data:

* [Arrays and nesting](https://github.com/mbostock/d3/wiki/Arrays#-nest)
* [An extremely useful tool by Shan Carter](http://bl.ocks.org/shancarter/raw/4748131/)
* [More examples of d3.nest](http://bl.ocks.org/phoebebright/raw/3176159/)

Resources on d3 selections:

* [General Update Pattern](https://bl.ocks.org/mbostock/3808218)
* [Thinking with Joins](https://bost.ocks.org/mike/join/)
* [Nested selections](https://bost.ocks.org/mike/nest/)


##Goals for today
* Using functions to draw charts
* Learning about data hierarchies and d3.nest()


##All the ways we can chart barley yields
No form is perfect -- each comes with its own tradeoffs. Here are some versions of your sketches from last week.

What are the merits of each?

Let's look at the code of each and see where there are major differences and talk about general strategies. I noticed three main types:

Morris did a [connected dot plot](http://bl.ocks.org/kpq/3097d976649b7f90c9eb).

University farm and Crookston did [bar charts](http://bl.ocks.org/kpq/c73936a85187c5727740)

Waseca did a variation of a [slopegraph](http://bl.ocks.org/kpq/867e3a5a2ca9661d7883). What are the pros and cons of this approach?

Here's a variation I made using [a scatterpplot and convex hulls](http://bl.ocks.org/pstuffa/2039304ed80b1c08be718fce486360ca)


##Generalizing
1. Let's choose one of these forms we want to go through and get it up and running.

2. Now let's generalize it using a function.

3. Now let's make six at once.

##Another way
Some of you already had to deal with this issue (particularly with the slopegraphs and even some of the grouped bar charts), but lots of visualizations come with inherent data hierarchy, which means, in some cases, we need to transform our data. d3.nest() is one way to do that. 


## Lab
1. Check out [Mister Nester](http://bl.ocks.org/shancarter/raw/4748131/) and try pasting the barley data into it.

2. Try making your group of six charts either using functions or using d3.nest(). (Note: for you nesters, some of you may need to nest twice.)


## Optional for Wednesday 
Explore the extended Barley Yield dataset from this [blog post](http://blog.revolutionanalytics.com/2014/07/theres-no-mistake-in-the-barley-data.html).
Extended barley data from [agridat package](http://www.rdocumentation.org/packages/agridat/functions/minnesota.barley.yield)
