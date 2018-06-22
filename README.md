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
   - `<class>.<name>` is usually a method on an object of type `<class>` (often the `<class>` documentation is on the same page)
   - e.g. `tree.size` is a method on a `d3.tree` object found in `d3-hierarchy` package
 

[d3-array](https://github.com/d3/d3-array/blob/master/README.md)
 - Extends JS native arrays with statistical, search, transforming, and plotting methods

[d3-axis](https://github.com/d3/d3-axis/blob/master/README.md) (**IMPORTANT**)
 - Draws human-readible axes based on a `d3-scale`

[d3-brush](https://github.com/d3/d3-brush/)
 - Interactive method to select/adjust data visualization, e.g. zoom region, timeline scrubber

[d3-chord](https://github.com/d3/d3-chord/)
 - Graph to visualize matrix of flows across a circular chart

[d3-collection](https://github.com/d3/d3-collection/)
 - Set of array-based data structures including map, set, and nest (tree array)

[d3-color](https://github.com/d3/d3-color/) (**IMPORTANT**)
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

[d3-dsv](https://github.com/d3/d3-dsv/) (**IMPORTANT**)
 - Parsing and formatting of data into delimiter-separate values, e.g. comma or tab
 - Great documentation!
 - d3.csv/d3.tsv are actually part of `d3-fetch`!

[d3-ease](https://github.com/d3/d3-ease/)
 - Animation effects for transitions to provide appealing time distortions, e.g. slow starts
 - Page contains great visualization of different easings!

[d3-fetch](https://github.com/d3/d3-fetch) (**IMPORTANT**)
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

[d3-hierarchy](https://github.com/d3/d3-hierarchy)
 - Provides tree, partitions, and other visualizations for heirarcichal data like file systems and nested geographies

[d3-interpolate](https://github.com/d3/d3-interpolate)
 - Provides interpolation between values of various types including numbers, colors, strings, and more
 - An `interpolator` interpolates between two values based on an input in [0,1]
 - e.g. `var i = interpolateNumber(7,14); i(0) >> 7; i(1) >> 14; i(0.1) >> 7.7;`
 
[d3-path](https://github.com/d3/d3-path)
 - Enables conversion of Canvas path commands into an SVG to use with D3js

[d3-polygon](https://github.com/d3/d3-polygon)
 - Provides a few operations on polygons (set of `(x,y)` pairs) like calculating centroids, convex hulls, etc.

[d3-quadtree](https://github.com/d3/d3-quadtree)
 - ????????
 - Apparently "two-dimensional recursive spatial subdivision", but unclear what this would actually be used for

[d3-random](https://github.com/d3/d3-random)
 - Random number generator functions for various distributions, e.g. normal, exponential, uniform, etc.

[d3-scale](https://github.com/d3/d3-scale) (**IMPORTANT**)
 - Provides a mapping from data (e.g. continous, ordinal, categorical, etc.) to a visual representation (e.g. position, color, etc.)
 - Following mathematics conventions, `domain` is the of input values and `range` is the set of output values

[d3-selection](https://github.com/d3/d3-selection) (**IMPORTANT**)
 - Drives DOM element selection, modification of elements including data joins, event binding/listening, and custom control flow over elements
 - This is a great reference for understanding data joins: https://github.com/d3/d3-selection#selection_data

[d3-shape](https://github.com/d3/d3-shape) (**IMPORTANT**)
 - Provides primitives for various shapes needed for visualization like lines, curves, areas, symbols, and more

[d3-time-format](https://github.com/d3/d3-time-format)
 - Parsing and formatting between strings and date values with numerous options for format, locale, etc.

[d3-time](https://github.com/d3/d3-time)
 - Numerous time-related math functions like intervals, counting days, ranges, etc.

[d3-timer](https://github.com/d3/d3-timer)
 - Provides a timer-driven queue to support and synchronize massive concurrent animations
 - `time` is the timestamp (numeric) that is considered the "start" time (default: `d3.now()`)
 - `delay` is added to `time` to determine when the timer begins (kickoff time is `time` *+* `delay`)

[d3-transition](https://github.com/d3/d3-transition)
 - Provides interpolated animation for changes in the DOM with adjustable timing, styles, and other configuration properties
 - Transitions are created using the `selection.transition([existing_transition])` method that takes an optional transition to synchronous movement across multiple selections

[d3-voronoi](https://github.com/d3/d3-voronoi)
 - Creates Voronoi diagrams (nearest neighbor polygons) with multiple accessible properties like edges, triangles, etc.

[d3-zoom](https://github.com/d3/d3-zoom)
 - Abstraction to allow pan and zoom selections in conjunction with `d3-scale`, `d3-axis`, `d3-drag`, and other modules
