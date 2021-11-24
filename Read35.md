# Graphs
### What is a Graph ?
A graph is a non-linear data structure that can be looked at as a collection of vertices (or nodes) potentially connected by line segments named edges.

### What are the common terms for graphs ?
- Vertex - A vertex, also called a “node”, is a data object that can have zero or more adjacent vertices.
- Edge - An edge is a connection between two nodes.
- Neighbor - The neighbors of a node are its adjacent nodes, i.e., are connected via an edge.
- Degree - The degree of a vertex is the number of edges connected to that vertex.

### Directed vs Undirected (Links to an external site.)
Undirected Graph: An Undirected Graph is a graph where each edge is undirected or bi-directional.
The undirected graph we are looking at has 6 vertices and 7 undirected edges.


### Complete Graphs
A complete graph is when all nodes are connected to all other nodes.

### Connected
A connected graph is graph that has all of vertices/nodes have at least one edge.

### Disconnected
A disconnected graph is a graph where some vertices may not have edges.

### Acyclic Graph
An acyclic graph is a directed graph without cycles.

A cycle is when a node can be traversed through and potentially end up back at itself.

### Cyclic Graphs
A Cyclic graph is a graph that has cycles.

A cycle is defined as a path of a positive length that starts and ends at the same vertex.

## Breadth First
In a breadth first traversal, you are starting at a specific vertex/node. This node must be specified when calling the BreadthFirst() method. The breadth-first traversal of a graph is like that of a tree, with the exception that graphs can have cycles. When a graph has cycles and we are trying to traverse, this leaves the possibility to be in an infinite loop….this is bad. To prevent such behavior, we need to have some sort of flag that specifies if we have already visited that vertices. Upon each visit, we just set the “visited” flag from false to true.

## Depth First
In a depth first traversal, we approach it a bit different than the way we do when working with a depth first traversal of a tree. Similar to how the breadth-first uses a queue, we are going to use a Stack for our depth-first traversal.

The algorithm for a depth first traversal is as follows:

Push the root node into the stack
Start a while loop while the stack is not empty
Peek at the top node in the stack
If the top node has unvisited children, mark the top node as visited, and then Push any unvisited children back into the stack.
If the top node does not have any unvisited children, Pop that node off the stack
repeat until the stack is empty.

## examples of graphs in use:

1. GPS and Mapping
2. Driving Directions
3. Social Networks
4. Airline Traffic
5. Netflix uses graphs for suggestions of products
