# Breadth-First Search
Primary use case, typically in trees or a [[Graph]]:
1. Traverse all vertices in the graph
2. Find shortest path, where **all edges have equal and positive weights**. The first time you meet your destination node, you have found the shortest path.

"as soon as a path between the source vertex and target vertex is found, it is guaranteed to be the shortest path between the two nodes (Leetcode)."

First determine the nodes and the edges before doing BFS in a specific question.

Given G = (V, E) and a starting vertex s, breadth-first search can be performed.

Uses [[Adjacency List]], Set, and a **Queue**. [[Depth-First Search]] uses a Stack.

It discovers all the vertices that are connected to s by traversing the edges. It gets the distance (smallest number of edges) from s to each reachable vertex. Also produces a "breadth-first tree" with root s that contains all reachable vertices.

Works on directed and undirected graphs.

Exhibit 1: Visualization of DFS vs BFS
![[bfs_dfs.gif]]

**Time complexity**
* Queue operations: $O(V)$
* Scan adjacency list: $O(E)$
* Full time: $O(V+E)$ - same as DFS

**Space complexity**
* *$O(V)$

**Note**:
* Don't need a Set{} if you don't have cycles, i.e., no sets for tree structures.
* "Normally, it's a bad idea to use BFS during the interview, unless the interviewer would push for it by adding new details into the problem description." (Leetcode)
	* DFS is usually easy to implement. There's no reason to choose the more complex approach.
	* Theory -  For DFS, depth of recurrence(extra space required) is equal to height of tree and for balanced tree it will be log(n) so Space complexity is O(log n).  For BFS, lowest layer of balanced tree will have n/2 nodes and hence queue will grow to n/2 size while processing lowest layer of tree. Space complexity is O(n).
	* Practically -  Thread stack size is much smaller than heap size(like -2MB vs 20GB). So DFS will throw StackOverFlow error for unbalanced tree way before BFS will throw OutOfMemoryError for a large tree.

---
## Tutorials: 
* [Graphs - BFS](https://leetcode.com/explore/learn/card/graph/620/breadth-first-search-in-graph/3883/)
* [Queue - BFS](https://leetcode.com/explore/learn/card/queue-stack/231/practical-application-queue/1376/)

## Templates
* [[BFS - Find if Path Exists]]
* [[BFS - Find All Paths to Target]]

---
Topics :: [[Graph]]
Reference :: Introduction to Algorithms
Type :: #atom
Creator :: Jacques
TAF ::
Discussion ::
Dis_Topic :: 
Resolved ::
Date :: 2022-07-25 14:47
