# Binary Search Tree

A **Binary Search Tree (BST)** is a type of binary tree where the value of each node is greater than or equal to 
the values in all the nodes in its left subtree and less than or equal to the values in all the nodes in its 
right subtree. This property allows for efficient **searching, insertion, and deletion** of nodes.

In other words, given a node with a value, if the value you are searching for is **less** than the value of the 
current node, you can eliminate the entire **right** subtree of the current node from consideration. Similarly, 
if the value you are searching for is **greater** than the value of the current node, you can eliminate the entire 
**left** subtree of the current node from consideration. This reduces the search space to a smaller subset of the tree, 
making searches faster.  
  
       8
      / \
     3   10
    / \    \
   1   6    14
      / \   /
     4   7 13


In this example, each node is greater than all nodes in its left subtree and less than all nodes in its right subtree. 
For example, the value of node 3 is less than 8, and all nodes in its left subtree (1 and 6) are also less than 8. 
Similarly, all nodes in the right subtree of node 3 (4 and 7) are also less than 8.

This property makes Binary Search Trees useful for a variety of applications, such as searching for an element in a
collection or implementing a sorted collection.

## Time Complexity

The time complexity of **search, insert, and delete** operations in a binary search tree (BST) is O(h), where h is the 
height of the tree. In a balanced BST, the height is typically O(log n), where n is the number of nodes in the tree. 
This means that the time complexity of search, insert, and delete operations is O(log n) in a balanced BST.

However, in the worst case, a BST can become **unbalanced** and degenerate into a linked list, with a height of O(n). 
In this case, the time complexity of search, insert, and delete operations would be O(n), which is no better than a 
simple list. For example, if elements are inserted in a BST in a **sorted order**, it can create a degenerate tree with
all nodes in a single chain, which can lead to a time complexity of O(n) for searching, inserting, and deleting. 
Therefore, it's important to keep a BST balanced to ensure efficient search, insert, and delete operations.  
  
## Balancing

There are different ways to keep a BST balanced, but the most common approach is to use a self-balancing BST, which is a 
type of data structure that automatically adjusts its shape to maintain a balance between the left and right subtrees. 
There are several types of self-balancing BSTs, such as:

**AVL trees:** AVL trees are the first self-balancing BSTs invented. They maintain a balance factor for each node, which is 
the difference between the heights of its left and right subtrees. The balance factor is always -1, 0, or 1, and the tree 
is rebalanced if the balance factor of any node is outside this range.

**Red-black trees:** Red-black trees are another popular self-balancing BST. They use a coloring scheme to balance the tree, 
where each node is either red or black. The tree is rebalanced by performing rotations and recoloring the nodes after 
insertions and deletions.
