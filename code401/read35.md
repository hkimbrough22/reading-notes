# Code 401 - Reading Notes

<!-- All references used were from Code 401 reading
assignment 35 -->

[comment]: <> (https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/graphs.html)

## Graphs
A graph is a non-linear data structure that can be looked at as a collection of `vertices` (or `nodes`) potentially connected by line segments named `edges`.

### Common Terminology

- Vertex - A vertex, also called a “node”, is a data object that can have zero or more adjacent vertices.
- Edge - An edge is a connection between two nodes.
- Neighbor - The neighbors of a node are its adjacent nodes, i.e., are connected via an edge.
- Degree - The degree of a vertex is the number of edges connected to that vertex.

### Directed versus Undirected Graphs
#### Undirected
An Undirected Graph is a graph where each edge is undirected or bi-directional.

In this example, no "directions" (arrows) are given to any of the points.

![Undirected Graph Example](../UndirectedGraph.png)

#### Directed
A Directed Graph also called a Digraph is a graph where every edge is directed.

Unlike an undirected graph, a Digraph has direction. Each node is directed at another node with a specific requirement of what node should be referenced next.

![Directed Graph Example](../DirectedGraph.png)


[BACK TO HOME](../README.md)