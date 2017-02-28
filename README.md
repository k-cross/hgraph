# HGraph

HGraph is a library for graphs and hyper-graphs which not only includes the underlying data structures, but also common algorithms and layout engines for visualizing the graphs in different ways.
There are many different types of graphs and there are no assumptions about what you can do with the graph types (ie edges that loop the same node or multiple edges to the same nodes) unless of course, the graph type doesn't support the layout trying to be generated.

Please keep in mind that I aim to be mathematically accurate in the implementation of these graphs, but I am not a mathematician so feel free to correct mathematical inaccuracies or request changes in naming. I also aim for high performance for pragmatic use, not just theoretical. Lastly, this is meant to be exactly as simple as it can be and no simpler.

## Planned

### Graph Types

* Graph
    * A generic graph with no weights or directed edges.
    * Equal weighted graphs will also be included as an algorithm assignment.
* Weighted Graph
    * A generic graph with weights but no directed edges.
* Directed Acyclic Graph (DAG)
    * A generic graph with directed edges and no weights.
    * Equal weighted DAGs will also be included as an algorithm assignment.
* Weighted Directed Acyclic Graph (WDAG)
    * A generic graph with directed edges and weights.
* Hyper-Graph
    * A generic graph with hyper-edges.
* Hyper-Graph Variations (With Appropriate Names)
    * Other variations on hyper-graphs with weights and directions and possibly other things I don't know about yet.
* Multi-Dimensional Graphs
    * I originally thought these were what hypergraphs are, but I was wrong.
    * My idea of this is the same thing as a WDAG except there can be different weight units attached to nodes making two unique edges. For example, a cost edge and a distance edge.
* Mesh
    * A generic graph where all nodes are connected to each other.
    * Equal weighted meshes will also be included as an algorithm assignment on a generic mesh.
* Weighted Mesh
    * Slightly different implementation than mesh as there is a _common weight_ which means every edge equals at least this much.
    * There are explicitly assigned weights to edges as well.
* Locality Mesh
    * A type of weighted mesh that connects to all nodes within a certain radial distance (distance is defined by edge weights).
* Other Types
    * Not planned but other types that can be pragmatically constructed can be included in the future.

### Graph Operations

All operations listed here will only be applied to the graphs where it makes sense (ie search will not be applied to a mesh because it'd be stupid).

* Search
    * BFS/DFS/A* and potentially other types
* Path Finding
* Minimum Spanning Trees
* Conversion
    * Converts some graph types into others that make sense (ie convert a 

### Layout Engines

There are many types of layout engines and I plan to implement a few where interactive layouts may be available in a distant future.

* Standard Layouts

#### Multi-Dimensional Layouts
    
These are also planned for multi-dimensional graphs. 
Essentially there will be engines to layout distances according to 3-space even if higher dimensionality is required.
The goal is to visulize data and nodes with new insights and accuracy in order to give more meaningful results.
