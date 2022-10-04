# In-Order Traversal
In-order traversal is to traverse the left subtree first. Then visit the root. Finally, traverse the right subtree.

Time: O(N)
Space: O(N)

```python
    def inorderTraversal(self, root: TreeNode) -> List[int]:
        answer = []
        
        # Create an empty stack
        stack = []

        # Start from the root node (set current node to the root node)
        curr = root

        # If the current node is None and the stack is also empty,
        # we are done
        while stack or curr:

            # If the current node exists, push it into the stack 
            # defer it) and move to its left child
            if curr:
                stack.append(curr)
                curr = curr.left
            else:
                # Otherwise, if the current node is None, pop an 
                # element from the stack,
                # print it, and finally set the current node to its 
                # right child
                
                curr = stack.pop()
                answer.append(curr.val)
                
                
                curr = curr.right
        
        return answer
```

---
Topics :: [[Binary Tree]]
Reference :: Leetcode
Type :: #atom
Creator :: Jacques
TAF ::
Discussion ::
Dis_Topic :: 
Resolved ::
Date :: 2022-09-15 19:53
