# BFS Find if Path Exists

```python
def has_path(n: int, edges: List[List[int]], source: int, destination: int) -> bool:  
  
    # Create adj list  
    adj_list = [[] for i in range(0, n)]  # Set length of array  
    # Populate adj list    
    for a, b, in edges:  
        adj_list[a].append(b)  
        adj_list[b].append(a) # Add this if undirected. 
  
    # Instantiate Seen, and Queue  
    queue = [source]  
    seen = {source}  
  
    # Traverse graph  
    while queue:  
        # Get current node by Dequeue from queue  
        vertex = queue.pop(0)  
  
        # Check if target reached  
        if vertex == destination:  
            return True  
  
        # Add all unseen neighbors to the queue  
        for neighbor in adj_list[vertex]:    
            if neighbor not in seen:  
                seen.add(neighbor)  
                queue.append(neighbor)  
  
    # No valid path exists  
    return False  
  
  
# Params  
n = 3  
edges = [[0, 1], [1, 2], [2, 0]]  
source = 0  
destination = 2  
  
# Solution  
print(has_path(n, edges, source, destination))
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
Date :: 2022-07-25 16:18
