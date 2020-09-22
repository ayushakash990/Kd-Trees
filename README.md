# Kd-Trees

we have to write a data type to represent a set of points in the unit square **(all points have x- and y-coordinates between 0 and 1)** using a **2d-tree** to support efficient range search (find all of the points contained in a query rectangle) and nearest-neighbor search (find a closest point to a query point). 2d-trees have numerous applications, ranging from classifying astronomical objects to computer animation to speeding up neural networks to mining data to image retrieval.



![alt text](https://github.com/ayushakash990/Kd-Trees/blob/master/images/Screenshot%20(16).png?raw=true)


![alt text](https://github.com/ayushakash990/Kd-Trees/blob/master/images/Screenshot%20(17).png?raw=true)


![alt text](https://github.com/ayushakash990/Kd-Trees/blob/master/images/Screenshot%20(18).png?raw=true)


### 2d-tree implementation

Write a mutable data type KdTree.java that uses a 2d-tree to implement the same API (but replace PointSET with KdTree). A 2d-tree is a generalization of a BST to two-dimensional keys. The idea is to build a BST with points in the nodes, using the x- and y-coordinates of the points as keys in strictly alternating sequence.

* ### Search and insert

The algorithms for search and insert are similar to those for BSTs, but at the root we use the x-coordinate (if the point to be inserted has a smaller x-coordinate than the point at the root, go left; otherwise go right); then at the next level, we use the y-coordinate (if the point to be inserted has a smaller y-coordinate than the point in the node, go left; otherwise go right); then at the next level the x-coordinate, and so forth.

![alt text](https://github.com/ayushakash990/Kd-Trees/blob/master/images/Screenshot%20(19).png?raw=true)

