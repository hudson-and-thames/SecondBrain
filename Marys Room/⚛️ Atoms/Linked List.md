# Linked List

A linked list is a linear data structure. Where each element is a separate object, and objects are linked together by the reference field.

All the nodes are linked in a sequence.

2 Types:
1. Single Linked List
2. Double Linked List

**Exhibit 1: Double linked list**
![[Double Linked List.png]]

Class attributes:
* value
* reference (links to next node)

Note:
* Can't access a node given an index, directly. You have to traverse the list until you get to the node. O(N)
* Head node represents the whole list.
* Main benefit of linked list is the insert and delete functionality.
* 2 Pointers and sentinel nodes are important concepts.

---
## Template
### Single Linked List
```python

class ListNode:
    def __init__(self, x):
        self.val = x
        self.next = None

class LinkedList:
    def __init__(self):
        self.size = 0
        self.head = ListNode(0)  # sentinel node as pseudo-head
        

    def get(self, index: int) -> int:
        """
        Get the value of the index-th node in the linked list. If the 
        index is invalid, return -1.
        """
        # If index is invalid
        if index < 0 or index >= self.size:
            return -1
        
        curr = self.head
        # Index steps needed 
        # to move from sentinel node to wanted index
        for _ in range(index + 1):
            curr = curr.next
        return curr.val
            

    def add_at_head(self, val: int) -> None:
        """
        Add a node of value val before the first element of the linked 
        list. After the insertion, the new node will be the first node 
        of the linked list.
        """
        self.add_at_index(0, val)
        

    def add_at_tail(self, val: int) -> None:
        """
        Append a node of value val to the last element of the linked 
        list.
        """
        self.add_at_index(self.size, val)
        

    def add_at_index(self, index: int, val: int) -> None:
        """
        Add a node of value val before the index-th node in the linked 
        list. If index equals to the length of linked list, the node 
        will be appended to the end of linked list. If index is 
        greater than the length, the node will not be inserted.
        """
        # If index is greater than the length, the node will not be 
        # inserted.
        if index > self.size:
            return
        
        # [so weird] If index is negative, 
        # the node will be inserted at the head of the list.
        if index < 0:
            index = 0
        
        self.size += 1
        # Find predecessor of the node to be added
        pred = self.head
        for _ in range(index):
            pred = pred.next
            
        # Node to be added
        to_add = ListNode(val)
        # Insertion itself
        to_add.next = pred.next
        pred.next = to_add
        

    def delete_at_index(self, index: int) -> None:
        """
        Delete the index-th node in the linked list, if the index 
        is valid.
        """
        # If the index is invalid, do nothing
        if index < 0 or index >= self.size:
            return
        
        self.size -= 1
        
        # Find predecessor of the node to be deleted
        pred = self.head
        for _ in range(index):
            pred = pred.next
            
        # Delete pred.next 
        pred.next = pred.next.next
        


# Your MyLinkedList object will be instantiated and called as such:
# obj = MyLinkedList()
# param_1 = obj.get(index)
# obj.addAtHead(val)
# obj.addAtTail(val)
# obj.addAtIndex(index,val)
# obj.deleteAtIndex(index)
```



---
## Tutorials
* [Introduction](https://leetcode.com/explore/learn/card/linked-list/209/singly-linked-list/1287/)
* [Insertion](https://leetcode.com/explore/learn/card/linked-list/209/singly-linked-list/1288/)
* [Deletion](https://leetcode.com/explore/learn/card/linked-list/209/singly-linked-list/1289/)
* [2 Pointer Technique](https://leetcode.com/explore/learn/card/linked-list/214/two-pointer-technique/)


---
Topics :: [[Data Structure]]
Reference :: Leetcode
Type :: #atom
Creator :: Jacques
TAF ::
Discussion ::
Dis_Topic :: 
Resolved ::
Date :: 2022-09-03 14:53
