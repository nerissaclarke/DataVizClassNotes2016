#Class 8: Updating elements: Data joins; interactivity; (possibly) responsive charts
So far we've only drawn things once and produced only static charts. Today, we'll update things we've drawn. 

##Housekeeping
Anything? Show and Tell? Questions about the readings?

## Useful links for the day
These all take work to understand, but you can see Mike's explanations get better and better.
 * [Three little circles](http://bost.ocks.org/mike/circles/)
 * [How selections work](http://bost.ocks.org/mike/selection/)
 * [selection.data()](https://github.com/mbostock/d3/wiki/Selections#data)
 * [Thinking with joins](http://bost.ocks.org/mike/join/)
 * [General Update Pattern](http://bl.ocks.org/mbostock/3808218)
 * [General Update Pattern II](http://bl.ocks.org/mbostock/3808221)
 * [General Update Pattern III](http://bl.ocks.org/mbostock/3808234)

4. Make a checklist for your 

	2. Make new data join
	3. Get rid of old elements
	4. Enter new elements
	5. append elements as needed
	6. update new selection

Today we're not going to add or get rid of elements – we'll merely be updating what's on the page.

##Lab, part 1: Updating axes, responsive views, UI control.
1. We'll start with a simple one. Let's open up [starterOne.html](starterOne.html)

2. Here are the features we'd like, all of which require updating existing elements:
	* have four buttons as a UI; on clicking, the chart should update
	* update the color of the circles based on the button that's been selected
	* create a chart title and a measure for an average value that renders and updates above the chart
	* make the chart responsive from 300px to 1050px ([On Resize](http://www.w3schools.com/jsref/event_onresize.asp))
	* update the axis based on a slider
	* Gratuituously cycle and animate through the quartet groups on a loop.


##Lab, part 2: Handle different # of values 
1. We'll start with [starterTwo.html](starterTwo.html)

2. Here are the features we'd like, all of which require updating existing elements:
	* have a button for each country
	* update the values based on the selected value (but this time, handle # sized datasets)

##Lab, part 2 
* Work on your own visualizations. Get your work publish to a bl.ocks.org page.
* Project work. Let's review the notes you made.


##Homework for Wednesday
Take a look at [this map](https://bl.ocks.org/mbostock/4060606). Don't worry about understanding all the code. We'll be going over this on Wendesday.






