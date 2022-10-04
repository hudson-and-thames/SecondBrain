# Graph
A graph G = (V, E)

Where:
* V = Vertices (nodes)
* E = Edges (relationships/lines/connections)

Memory requirement: 

Core things to do are: 
1. Represent a graph
2. Search a graph.
	1. Depth-First Search
	2. [[Breadth-First Search]]

Exhibit 1 shows two representations for a graph:
* Adjacency lists: $O(V+E)$
* Adjacency matrices: $O(V^2)$

**Exhibit 1: Representations**
![[graph_representations.png]]

An edge: (v, u) shows that v -> u.

A graph is an object that can contain the attribute `Adj` which refers to the adjacency list. So if we want to look at a vertex we go: `G.Adj[u]`.



---
Topics :: [[Data Structure]]
Reference :: Introduction to Algorithms
Type :: #atom
Creator :: Jacques
TAF ::
Discussion ::
Dis_Topic :: 
Resolved ::
Date :: 2022-07-25 14:31
