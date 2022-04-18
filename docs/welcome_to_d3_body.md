## Welcome To D3

[D3](https://d3js.org/)
is a set of tools for drawing dynamic visualizations in a browser.
The results can be beautiful and very effective, but the recipes are
messy and difficult to teach.  

D3 stands for 'Data-driven documents'.

Much of the code is Javascript on the web page itself.  It's rather
idiomatic and has a style that seems unusual to me.


Since serious javascript is outside the domain of this course, we are going
to look at the structure of D3 applications without trying to fully understand
all the details.

This means our visit to D3 must stay pretty superficial.



#### First some examples

There are many at [The ObservableHQ Gallery](https://observablehq.com/@d3/gallery).

See also [the D3 Home Page](https://d3js.org/)


* [Treemap](https://observablehq.com/@d3/treemap)
* [Zoomable treemap](https://observablehq.com/@d3/zoomable-treemap)
* [Sortable bar chart](https://observablehq.com/@d3/bar-chart-transitions)
* [Force-directed graph](https://observablehq.com/@d3/force-directed-graph)
* [Tidy tree](https://observablehq.com/@d3/tree)
* [Icicle graph (zoomable!)](https://observablehq.com/@d3/zoomable-icicle)
* [Sankey diagram](https://observablehq.com/@d3/sankey) (see also the [HuBMAP data queue](https://software.docs.hubmapconsortium.org/data-sankey/index.html))


Keep in mind, each of these is a sort of recipe.  You can copy it and
customize it, but it's not as plug-and-play as, say, seaborn.



#### Still to cover

* Get the Note off the demo page!
* logic must be in the browser to minimize response time loop
* sequence of events: data restructure, layout, transcription to SVG
* animation