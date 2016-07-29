#Class 7: Building confidence with hierarchical data; thinking about design.

##Housekeeping
Anything to discuss? Helpdesk? Making a bl.ock? Questions about the incomes chart? Show and tell?

##Goals for today
 * Get better at d3.nest(), including using a TRIPLE NEST
 * Work on the 'fiddly bits' of charts -- the last 10 percent. Axes are hard!
 * Become better designers
 * Learn about updating charts once we've drawn them.

##Lab, Part 1
Today we'll be working with baseball data, called [games.csv](games.csv). Download it and take a look. It's a chart of every team in baseball's winning percentage over the course of the 2015 season. Today we'll visualize this data set at few different ways, and get practice doing end-to-end chart development – formatting complex data, working with deeply nested selections, updating charts once we've drawn them, and thinking more about design than we ever have. You might also benefit from a lookup table called [lookup.tsv](lookup.tsv).

Our goal is to make a chart of each team's winning percentage over time; ideally to look as close as possible to one published in the Chicago Tribune more than 100 years ago.

<img src="Screenshot 2015-06-24 18.32.00.png">

But we want one for every division, sort of like this:

<img src="Screenshot 2016-04-11 18.33.13.png">

First, let's make a plan, thinking about what we'll want from D3. Scales, axes, dates, lines, and so on. And design! It looks simple, but putting them all together can be complicated.

##Part II: Make one chart, update for team and division.
We'll continue this on Monday if there's not time. Your goal is to make one larger chart, with the same design, but have the user select which division to show and have the chart update (including axes, scales and domains).

##Homework for Monday
Next class we'll be going through another fundamental, but difficult, part of D3, which is called the "General Update Pattern." 

For that, read through these two blog posts:
 * [Thinking with joins](https://bost.ocks.org/mike/join/)
 * [Three little circles](https://bost.ocks.org/mike/circles/)