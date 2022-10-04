# Pre-Order Traversal (DFS)
A method to traverse a [[Binary Tree]]

Top down, left to right (because its a stack, you have to load it right to left).

Time: O(N)
Space: O(N)


## Recursive


## Iterative
```python
# Definition for a binary tree node.
# class TreeNode:
#     def __init__(self, val=0, left=None, right=None):
#         self.val = val
#         self.left = left
#         self.right = right

class Solution:
    def preorderTraversal(self, root: TreeNode) -> List[int]:
        answer = []
        stack = []
        
        # Load the first element
        if root:
            stack.append(root)
            
        while len(stack) > 0:
            cur = stack.pop()
            answer.append(cur.val)
            if cur.right:
                stack.append(cur.right)
            if cur.left:
                stack.append(cur.left)
        return answer
```

---
Topics ::  [[Binary Tree]]
Reference :: Leetcode
Type :: #atom
Creator :: Jacques
TAF ::
Discussion ::
Dis_Topic :: 
Resolved ::
Date :: 2022-09-15 19:29
