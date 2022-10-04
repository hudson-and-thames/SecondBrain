# Post-Order Traversal

Post-order traversal is to traverse the left subtree first. Then traverse the right subtree. Finally, visit the root.

It is worth noting that when you delete nodes in a tree, deletion process will be in post-order. That is to say, when you delete a node, you will delete its left child and its right child before you delete the node itself.

Also, post-order is widely use in mathematical expression. It is easier to write a program to parse a post-order expression.

Time: O(N)
Space: O(N)

## Recursive
```python
# Recursive version
    def postorderTraversal(self, root: TreeNode) -> List[int]:
        
        def dfs(node):
            if not node:
                return None
            
            dfs(node.left)
            dfs(node.right)
            post_order.append(node.val)
        
        post_order = []
        dfs(root)
        
        return post_order
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
Date :: 2022-09-15 20:01
