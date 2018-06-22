## D3 History

### [D3js Introduction](https://d3js.org)
Read the introduction on this page - short and hits the big items


### [D3js v5.0 Changes](https://github.com/d3/d3/blob/master/CHANGES.md#changes-in-d3-50)
Primary major change is moving to Promises

[What are promises and why should you care?](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Using_promises)


### [D3js v4.0 Changes](https://github.com/d3/d3/blob/master/CHANGES.md#changes-in-d3-40)
Contains massive API changes


## D3 Package Overview

There are a couple things I found confusing in reading the documentation that should be kept in mind:
 - Function parameter names are very vague (e.g. `row` or `init`) and you should read the description to make sure you understand
 - The namespaces can be confusing and not easy to identify or trace back, but the general rules seem to be:
   - `d3.<name>` is a method within that package
   - `<class>.<name>` is usually a method on an object of type `<class>`, e.g. `tree.size` is a method on a `d3.tree` object found in `d3-hierarchy` package


[d3-array](https://github.com/d3/d3-array/blob/master/README.md)
 - Extends JS native arrays with statistical, search, transforming, and plotting methods

[d3-axis](https://github.com/d3/d3-axis/blob/master/README.md)
 - Draws human-readible axes based on a `d3-scale`

[d3-brush](https://github.com/d3/d3-brush/)
 - Interactive method to select/adjust data visualization, e.g. zoom region, timeline scrubber

[d3-chord](https://github.com/d3/d3-chord/)
 - Graph to visualize matrix of flows across a circular chart

[d3-collection](https://github.com/d3/d3-collection/)
 - Set of array-based data structures including map, set, and nest (tree array)

[d3-color](https://github.com/d3/d3-color/)
 - Methods to define/adjust colors, e.g. RGB, named colors, opacity, etc.

[d3-scale-chromatic](https://github.com/d3/d3-scale-chromatic)
 - Provides color schemes to align with a `d3-scale` both discrete or continous
 
[d3-contour](https://github.com/d3/d3-contour)
 - Provides numerous forms of contour and density plots

[d3-dispatch](https://github.com/d3/d3-dispatch/)
 - Provides callback registration and listening to separate concerns in code
 - Good example: https://bl.ocks.org/mbostock/5872848

[d3-drag](https://github.com/d3/d3-drag/)
 - Provides a flexible abstraction to enable drag-and-drop behavior on graphs

[d3-dsv](https://github.com/d3/d3-dsv/)
 - Parsing and formatting of data into delimiter-separate values, e.g. comma or tab
 - Great documentation!
 - d3.csv/d3.tsv are actually part of `d3-fetch`!

[d3-ease](https://github.com/d3/d3-ease/)
 - Animation effects for transitions to provide appealing time distortions, e.g. slow starts
 - Page contains great visualization of different easings!

[d3-fetch](https://github.com/d3/d3-fetch)
 - Numerous shortcut functions to fetch (read) various file formats and process them
 - With three parameters: `dsv(delimiter, file_path, row_conversion_function)`
 - With two parameters: `dsv(delimiter, file_path, init_function, row_conversion_function)`
 - `csv(*)` is equivalent to `dsv(",", *)`

[d3-force](https://github.com/d3/d3-force/)
 - Physics simulator for forces on particles for interacting objects, e.g. tic-tac toe
 - Also can be useful for network graphs, beeswarm plots, or other common graphs

[d3-format](https://github.com/d3/d3-format/blob/master/README.md)
 - Used for complex number-to-string formatting ala Python 3's .format

[d3-geo](https://github.com/d3/d3-geo/blob/master/README.md)
 - Functions to draw, project, and do various math related to geographic maps
 - This is VERY complex and basic maps should use a small fraction of methods!

[d3-hierarchy]()
 - 

[d3-interpolate]()
 - 
 
[d3-path]()
 - 

[d3-polygon]()
 - 

[d3-quadtree]()
 - 

[d3-random]()
 - 

[d3-scale]()
 - 

[d3-selection]()
 - 

[d3-shape]()
 - 

[d3-time-format]()
 - 

[d3-time]()
 - 

[d3-timer]()
 - 

[d3-transition]()
 - 

[d3-voronoi]()
 - 

[d3-zoom]()
 - 



