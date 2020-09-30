# Graphs 

* A graph is a non-linear data structure that 
can be looked at as a collection of vertices 
(or nodes) potentially connected by line 
segments named edges.


### Directed vs Undirected
* Undirected Graphs


An Undirected Graph is a graph where each 
edge is undirected or bi-directional. This 
means that the undirected graph does not move 
in any direction.

* Directed Graphs (Digraph)


A Directed Graph also called a Digraph is a 
graph where every edge is directed.

Unlike an undirected graph, a Digraph has 
direction. Each node is directed at another 
node with a specific requirement of what node 
should be referenced next.

Compare the visual below with the undirected 
graph above. Can you see the difference? The 
Digraph has arrows pointing to specific nodes.


#### Complete vs Connected vs Disconnected
There are many different types of graphs. 
This depends on how connected the graphs are 
to other node/vertices.

The three different types are completed, 
connected, and disconnected.

### Complete Graphs
A complete graph is when all nodes are connected to all other nodes.

#### Connected


A connected graph is graph that has all of vertices/nodes have at least one edge.

In the visual above, this looks a lot more than what you are used to seeing. If you look closely at the different vertices of the graph, you will see that each node is connected to at least one other node or vertices. A Tree is a form of a connected graph. We will talk more about that in a bit.

### Disconnected
A disconnected graph is a graph where some 
vertices may not have edges.

In the above visual, the disconnected graph 
shows that some nodes may not always be 
connected to other nodes or vertices of the 
graph. It is complelty possible to have 
standalone nodes or edges (also known as 
islands) in a graph data structure.

* Acyclic vs Cyclic
In addition to undirected and directed 
graphs, we also have acyclic and cyclic 
graphs.

##### Acyclic Graph

An acyclic graph is a directed graph without cycles.

A cycle is when a node can be traversed through and potentially end up back at itself.

Here is an example of 3 acyclic graphs:


