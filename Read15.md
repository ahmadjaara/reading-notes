# Tree data 

tree data structure is a kind of hierarchal data arranged in a tree-like structure. It consists of a central node, structural nodes, and sub nodes, which are connected via edges. We can also say that tree data structure has roots, branches, and leaves connected with one another.  

- Node - A Tree node is a component which may contain its own values, and references to other nodes
- Root - The root is the node at the beginning of the tree
- K - A number that specifies the maximum number of children any node may have in a k-ary tree. In a binary tree, k = 2.
- Left - A reference to one child node, in a binary tree
- Right - A reference to the other child node, in a binary tree
- Edge - The edge in a tree is the link between a parent and child node
- Leaf - A leaf is a node that does not have any children
- Height - The height of a tree is the number of edges from the root to the furthest leaf

## Traverse

Traversing a tree allows us to search for a node, print out the contents of a tree, and much more! There are two categories of traversals when it comes to trees:

- Depth First

- Breadth First

The most common way to traverse through a tree is to use recursion. With these traversals, we rely on the call stack to navigate back up the tree when we have reached the end of a sub-path.

**breadth first** traversal uses a queue (instead of the call stack via recursion) to traverse the width/breadth of the tree

## Binary Tree Vs K-ary Trees

**Binary Trees** restrict the number of children to two (hence our left and right children).

There is no specific sorting order for a binary tree. Nodes can be added into a binary tree wherever space allows

If Nodes are able have more than 2 child nodes, we call the tree that contains them a **K-ary Tree**. In this type of tree we use K to refer to the maximum number of children that each Node is able to have.

## Binary Search Trees

A Binary Search Tree (BST) is a type of tree that does have some structure attached to it. In a BST, nodes are organized in a manner where all values that are **smaller** than the root are placed to the **left**, and all values that are **larger** than the root are placed to the **right**.
