# Tester Interview Exercise: Outlining Blocks of Data

## The Scenario
A project receives data about smoke concentrations in the air.
The data is in a grid format -- there is a value for each square in the grid.
The project's aim is to be able to draw on a map the boundary lines between certain concentrations of smoke.


To do this, the service needs to be able to turn a block of squares into lines which draw round the edges of the block.

Here is a very simplified example.  The four blocks in this grid:

![Grid with four blocks](imgs/grid-with-blocks.svg)

should be turned into these lines in blue:

![Grid with line around blocks](imgs/grid-with-line.svg)

The service needs to:
* output geojson (a type of json format)
* be able to complete processing in less than 30 seconds
* handle at least ten concurrent pieces of processing

## Test input format
The devs have done some basic testing while writing the code. 
They've made a test harness that takes in a string of text 
where a dot . represents an empty grid square and an X represents a full grid square.

For example, the grid above would be represented like this:

```
......
..XX..
..X...
..X... 
......
......
```

## Please come prepared to discuss
1. examples of grid inputs you'd want to put through the system to see how it handled particular cases
2. what other checks you would want to carry out to verify the system is operating correctly (e.g. per the requirements above)