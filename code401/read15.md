# Code 401 - Reading Notes

<!-- All references used were from Code 401 reading
assignment 15 -->
[comment]: <> (https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-15/resources/Trees.html)
## Trees
1. Binary Trees
2. Binary Search Trees
3. K-ary Trees

### Common Terminology
- Node - A Tree node is a component which may contain it’s own values, and references to other nodes
- Root - The root is the node at the beginning of the tree
- K - A number that specifies the maximum number of children any node may have in a k-ary tree. In a binary tree, k = 2.
- Left - A reference to one child node, in a binary tree
- Right - A reference to the other child node, in a binary tree
- Edge - The edge in a tree is the link between a parent and child node
- Leaf - A leaf is a node that does not have any children
- Height - The height of a tree is the number of edges from the root to the furthest leaf

![Binary Tree](../BinaryTree1.png)

### Depth-First Traversals
![Depth-First Traversals](../tree-example.png)
- Pre-order: A, B, D, E, C, F
- In-order: D, B, E, A, F, C
- Post-order: D, E, B, F, C, A

Uses Stacks to operate.

### Breadth-First Traversals
- Output: A, B, C, D, E, F

Uses Queue.

[BACK TO HOME](../README.md)