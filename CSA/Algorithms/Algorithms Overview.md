## **[[Graph-Traversal]]**
**Depth-First:** Fully explores a branch before backtracking. Used for maze navigation and connected graphs.
**Breadth-First:** Fully explores a node before moving to the next. Used for finding the shortest path in unweighted graphs.
## **[[Tree-Traversal]] Methods:**
**Pre-Order:** Visit root, Traverse left sub-tree, Traverse right sub-tree
- Use:  Copying a tree (can be performed on any tree).
**In-Order:** Traverse left sub-tree, Visit the root, Traverse right sub-tree
- Use: Outputs contents of a binary tree in ascending order.
**Post-Order:** Traverse left sub-tree, Traverse right sub-tree, Visit root
- Use: Converts an expression tree to postfix notation and empties the tree.
## **[[Reverse Polish]] Notation (RPN) Importance:**
- Unambiguous, doesn't require brackets.
- Can be evaluated using stacks.
- In-order traversal gives infix.
- Post-order traversal gives a postfix.
---
## **[[Searching Algorithms]]:**
### **Linear Search:**
- $O(n)$
- Sequentially checks each item until the target is found.
- If the end is reached, the target is not in set.
### **Binary Search:**
- $O(\log (n))$
- Requires sorted data.
- Compare the middle element with the target value.
- Adjusts search area based on comparison.
**Binary Tree Search:** Similar to binary search, conducted on a binary tree.
---
## **[[Sorting Algorithms]]:**
### **Bubble Sort:**
- $O(n^2)$
- Iteratively compares and swaps adjacent elements.
### **Merge Sort:**
- $O(n\log(n))$
- Divides unsorted lists into sub-lists and recursively merges them.
## **[[Optimisation Algorithms]]**
### **Dijkstra's Shortest Path Algorithm:**
- Finds the shortest path between nodes in a weighted graph.
- Used in navigation systems and routers for packet routing.