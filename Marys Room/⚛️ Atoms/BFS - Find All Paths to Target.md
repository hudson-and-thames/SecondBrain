# BFS Find All Paths to Target

```python
# Find all paths from 0 to n-1.  
# It is directed acyclic (DAG) which means we don't need a seen set() in this algo  
def allPathsSourceTarget(graph: List[List[int]]) -> List[List[int]]:  
    paths = []  
    # Check graph not empty and edge case  
    if not graph or len(graph) == 0:  
        return paths  
  
    # Instantiate first path in queue  
    queue = [[0]]  
  
    # Traverse and find all paths  
    while queue:  
        # Get current path and last node  
        curr_path = queue.pop(0)  
        last_node = curr_path[-1]  
  
        # Add new paths to queue  
        for node in graph[last_node]:  
            # Create a path with the additional node  
            next_path = curr_path.copy()  
            next_path.append(node)  
  
            # If at last node then record full paths  
            if node == len(graph) - 1:  
                paths.append(next_path)  
            else:  
                queue.append(next_path)  
  
    return paths  
  
  
# Params  
graph = [[1, 2], [3], [3], []]  
expected_output = [[0, 1, 3], [0, 2, 3]]  
print(allPathsSourceTarget(graph))
```

---
Topics :: [[Breadth-First Search]]
Reference :: Leetcode
Type :: #atom
Creator :: Jacques
TAF ::
Discussion ::
Dis_Topic :: 
Resolved ::
Date :: 2022-07-25 16:48
