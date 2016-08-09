#Class 11: Network Graphs

##Housekeeping
  * Anything?
  * Show N' Tell? Any cool maps?

#Network Graphs 101 

What is a Network Graph?

> In mathematics and computer science, graph theory is the study of graphs, which are mathematical structures used to model pairwise relations between objects. A graph in this context is made up of vertices, nodes, or points which are connected by edges, arcs, or lines.

Sounds complicated, but it's not that bad. Essentially, you have two sets of items: nodes and links. The nodes are (usually) the circles in the network graph. The links are the lines. And having two datasets, one for the nodes and one for the links, is how you'll generate a network graph. Here's a look at a very basic network graph:

![simple graph!](https://upload.wikimedia.org/wikipedia/commons/thumb/5/5b/6n-graf.svg/2000px-6n-graf.svg.png)

#####Types of Graphs

There are many different type of layouts for graphs. They type of graph is determined by it's layout. All graph layouts are generally aim for the same goal: readabiliy. Here's a look at few:
 * [Force Directed](https://bl.ocks.org/mbostock/4062045)
  * [Blocks](https://bl.ocks.org/mbostock/afecf1ce04644ad9036ca146d2084895)
  * [Lattice](https://bl.ocks.org/mbostock/1b64ec067fcfc51e7471d944f51f1611)
 * [Arc](https://www.jasondavies.com/primos/)
 * [Hive](https://bost.ocks.org/mike/hive/)
 * [Tree](https://bl.ocks.org/mbostock/4339083)
 * [Lattice](https://bl.ocks.org/mbostock/1b64ec067fcfc51e7471d944f51f1611)

##Lab, part I
Let's first make that image above of a really basic network graph. Let's go through that Force Directed Graph example to get a sense of what that'll look like:
 1. Add you SVG
 2. Define your force simluation
 3. Put your data in the correct format
 4. Input the data into the simulation
 5. Set the positions for all the elements you want using the ticked() function
 6. Start the simulation 

##Lab, part II
Let's try making our own network graph, using our old friend, the barley data. This example will show how to make a graph when the dataset is in a different format. 
 1. Load the data in
 2. Sketch out the sort of graph layout we want
 3. Identify the distinct nodes and links
 4. Build distinct arrays for nodes and links

##Lab, part III
Two options:
 * Continue to build on the barley example. See if you can get the yield to determine the radius size. (Hint you may want to make a lookup for the value (**easier approach**) or change how we created the orginal set of nodes.)
 * Try to do the general update pattern on a force directed graph, using a filter to trim or grow the graph. 

##Or, projects.

## For Wednesday!
* Make sure you have [homebrew](http://brew.sh/) installed on your mac. If/Once you do, install node ```brew install node```
* Make a [heroku account](https://www.heroku.com/) if you don't have one already 



