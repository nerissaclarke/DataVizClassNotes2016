#Class 5: Line charts, working with nested data

##Housekeeping
Show + tell?
Any questions from Monday?
Any questiosn about projects?

### Useful stuff

Useful API references and tutorials:

* [d3.nest](https://github.com/mbostock/d3/wiki/Arrays#nest) - a utility for nesting an array of data. Experiment with [Mister Nester](http://bl.ocks.org/shancarter/raw/4748131/).
* [d3.svg.line](https://github.com/mbostock/d3/wiki/SVG-Shapes#line) - a utility we haven't explored yet for generating an [SVG path string](http://www.w3schools.com/svg/svg_path.asp).
* [Operating on Selections](https://github.com/mbostock/d3/wiki/Selections#operating-on-selections)
* [Nested Selections](https://bost.ocks.org/mike/nest/)

Reading: Check out [this article on visualization design](http://style.org/stdp3/) featuring excellent slides, including work by [Kevin Quealy](https://twitter.com/KevinQ).

Also check out this [version of the data visualization course](https://shancarter.github.io/ucb-dataviz-fall-2013/) by Shan Carter and Kevin Quealy, which emphasizes using R for data exploration.


##Goals for today
  * Familiarize ourselves with line charts and the `path` and `line` SVG elements
  * Learn to recognize hierarchical data when we see it
  * Create and manipulate nested data
  * Work on the 'fiddly bits' of charts -- the last 10 percent

##Line charts
Mostly we've worked with `circle` elements, but the `path` element, which power line charts, is slightly different. First, about line charts:

* Strengths of line charts
  * A charting workhorse
  * Ideal for comparing relationships over time
  * Generally better than bar charts if you're comparing more than two series 

* Common mistakes
  * Legends when they are not necessary (dynamic labels can be a headache too though)
  * Dual Axes
  * 3D charts (except when it's not a mistake)

* Examples of NYT line charts, (not all made using D3):
  * [The Jobless Rate for People Like You](http://www.nytimes.com/interactive/2009/11/06/business/economy/unemployment-lines.html) 
  * [Recovering, But at Different Paces](http://www.nytimes.com/interactive/2012/11/27/us/recovering-but-at-different-paces.html?ref=us)
  * [Case Shiller Home Prices Interactive](http://www.nytimes.com/interactive/2014/01/23/business/case-shiller-slider.html)
  * [Why Peyton Manning’s Record Will Be Hard to Beat](http://www.nytimes.com/interactive/2014/10/19/upshot/peyton-manning-breaks-touchdown-passing-record.html)
  * [How Likely is it that Birth Control Could Let You Down?](http://www.nytimes.com/interactive/2014/09/14/sunday-review/unplanned-pregnancies.html)
  * [American Middle Class is No Longer the World’s Richest](http://www.nytimes.com/2014/04/23/upshot/the-american-middle-class-is-no-longer-the-worlds-richest.html?abt=0002&abg=0)

##About SVG paths and lines

Let's take a look at [the documentation](http://www.w3.org/TR/SVG/paths.html) for paths and [lines](http://www.w3.org/TR/SVG/lines.html)

##Lab, part I
The Upshot launched with a large story using a study by the Luxembourg Income Study (LIS) that included cross-country comparisons for a variety of income levels in a handful of countries. The Times focused on comparing middle-class incomes, publishing a front-page story titled [The American Middle Class Is No Longer the World’s Richest](http://www.nytimes.com/2014/04/23/upshot/the-american-middle-class-is-no-longer-the-worlds-richest.html?abt=0002&abg=0). We’ll work with [the data used in that story](http://www.lisdatacenter.org/resources/other-databases/) today. 

Open up the data in a spreadsheet of your choice and spend a few minutes getting to know what the fields represent. It's messy!

Our first goal will be to **make a line chart of the middle class income for the U.S.** using the PPP positional measure (tab 3). Specifically, take a look at `Cut-off points (cop): Equivalized (PPP), 2005 PPP dollars`, the data set in the "middle" of that sheet. Think about how you would need to format or restructure this data. 

For this, and all today's exercises, we'll work with [incomes.csv](incomes.csv), a slightly cleaned up version of that spreadsheet.

We'll make four charts of increasing complexity today.

Here's our first goal:
<img src="step-1.png">

1. Recall our checklist from week 3 and the d3 margin conventions we always like to borrow.

  1. Navigate to your working directory, create an `index.html` file with D3 loaded and start a local server
  1. Load your data
  1. Add an SVG on the page.
  1. Format your data, adding fields as necessary
  1. Do your data join
  1. Position your elements 
  1. Add an axis
  1. Add styles
  1. Other customizations, "fiddly bits"

2. Next, make the same chart, but instead we want to include all the other countries as a reference.Let's use d3.nest()!

3. Our goal is something like this. Think about what elements you would need to make that.

<img src="step-2.png">

4. The chart we just made isn't helpful if we care about knowing which countries are which. Your nested data does not need to change, but you will need to restructure your code to make a chart for each country. Let's say we want to compare middle-class incomes of the U.S. to the following countries:

  ```
  var compareCountries = ["United Kingdom", "Norway", "Germany", "Canada", "Netherlands", "France", "Sweden", "Ireland", "Spain"]
  ```

  Here's our goal – note the sort here isn't particularly meaningful -- and how would we maybe change that, by the way?:
  <img src="step-3.png">


5. Finally, a look forward to next class: a comparison of the full distribution at each income level, highlighting the US in each. 

  <img src="step-4.png">

  If you have time, try to get it closer to this. It gets complicated quickly!

  <img src="step-5.png">

  It's just one line to make this more simplified version, if you prefer:

  <img src="step-7.png">


##Discussion for next week/if there's time today
Based on some of our talks about what to do with complex forms on the web -- particularly on small devices -- here are some examples that use layering, which *can* work well on tiny devices. (Check out both on mobile and desktop.)

  - [A 3-D View of a Chart That Predicts The Economic Future: The Yield Curve](http://www.nytimes.com/interactive/2015/03/19/upshot/3d-yield-curve-economic-growth.html)
  - [The Facebook Offering: How It Compares](http://www.nytimes.com/interactive/2012/05/17/business/dealbook/how-the-facebook-offering-compares.html)
  - [Fewer Helmets, More Deaths](http://www.nytimes.com/interactive/2014/03/31/science/motorcycle-helmet-laws.html)
  - [How the Recession Reshaped the Economy, in 255 Charts](http://www.nytimes.com/interactive/2014/06/05/upshot/how-the-recession-reshaped-the-economy-in-255-charts.html)
  - [The Tenure Pipeline at Harvard Business School](http://www.nytimes.com/2013/09/08/education/harvard-case-study-gender-equity.html?ref=education)


& publish your blocks! By Monday, I would like everyone to have a block for Anscombes Quartet and one using the barley data.