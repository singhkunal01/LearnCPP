# Table of content
- [Construct and Display Genric Tree](#construct-and-display-genric-tree)
    - [Properties](#properties)
    - [Algorithm](#algorithm)
    - [Time Complexity](#time-complexity)
    - [Advantages](#advantages)
    - [Disadvantage](#disadvantages)
    
 - [Minimum distance between two nodes in a Genric Tree](#minimum-distance-between-two-nodes-in-a-genric-tree) 
    - [Properties](#properties-1)
    - [Algorithm](#algorithm-1)
    - [Time Complexity](#time-complexity-1)
    - [Advantages](#advantages-1)
    - [Disadvantage](#disadvantages-1)
    
- [Diameter of a Genric Tree](#Diameter of a Genric Tree)
    - [Properties](#Properties)
    - [Algorithm](#Algorithm)
    - [Time Complexity](#Complexity)
    - [Advantages](#advantages)
    - [Disadvantage](#disadvantage)

# Construct and Display Genric Tree

- Generic trees are a collection of nodes where each node is a data structure that consists of records and a list of references to its children  (duplicate references are not allowed).  
- Unlike the linked list, each node stores the address of multiple nodes.
- Every node stores address of its children and the very first node’s address will be stored in a separate pointer called root.

![generic-tree_gfg](https://user-images.githubusercontent.com/55774240/158732482-11f84781-453f-4d25-8826-8ef54a5b0490.png)


### Properties

- Many children at every node.
- The number of nodes for each node is not known in advance.

### Algorithm

- use Dynamic Arrays for storing the address of  children’s address
- construct node class to understand structure of genric tree.
member values of node class are 
int data;
vector<node*> children;
- Create newnode and add data in it and push back in array as  st.top()->children.push_back(newnode);
- fetch root node and use recursion to print rest of the node in the display function 
for(node*child:root->children){
display(child);
}

### Time Complexity
```
- For creatingtreee()
  O(n) ,where n is the number of node
- For display()
  O(n) ,where n is the number of node
 ``` 
### Advantages 

- Memory efficient – No extra links are required, hence a lot of memory is saved.
- Treated as binary trees – Since we are able to convert any generic tree to binary representation, we can treat all generic trees with a first child/next sibling representation as binary trees. Instead of left and right pointers, we just use firstChild and nextSibling.
- Many algorithms can be expressed more easily because it is just a binary tree.
- Each node is of fixed size no auxiliary array or vector is required.

### Disadvantages

- Memory Wastage – All the pointers are not required in all the cases. Hence, there is lot of memory wastage.
- Unknown number of children – The number of children for each node is not known in advance.




# Minimum distance between two nodes in a Genric Tree

- Distance refers to the edges between them. Now in a tree, there is always one path from one node to another.
- So the distance between two nodes must pass through their ancestor from the defination of generic tree.
- Ancestor will have refrence to both of the node.

![some1](https://user-images.githubusercontent.com/55774240/158732716-cfea4195-85db-4631-9ec4-f6ca50000875.jpg)


### Properties

- Minimum distance between two nodes will contains parent node.
- Atleast one valid path always exists between any two nodes in a tree.

### Algorithm

- Calculate node to root path for both the nodes
- Keep iterating from the end and the last equal items in the path of both the nodes becomes the LCA
- Now the distance between two nodes will be the distance of node 1 from LCA in addition to the distance of node 2 from LCA.

### Time Complexity
```
- For creatingtreee()
  O(n), where is number of nodes. 
- Finding the node in the entire tree to get the node to the root path takes O(n), where is number of nodes.
- just traversing the node-to-root path (arrays) takes O(d) where d = depth of the node.
  In the worst case, d can be equal to n, hence total time complexity will be O(n) only, where is number of nodes.
```
### Advantages 

- Memory efficient – No extra links are required, hence a lot of memory is saved.
- We even can visualise how parent node plays vital role.
- Many algorithms can be expressed more easily because it is just a binary tree.
- Each node is of fixed size no auxiliary array or vector is required.

### Disadvantages

- Memory Wastage – All the pointers are not required in all the cases. Hence, there is lot of memory wastage.
- Unknown number of children – The number of children for each node is not known in advance.


# Diameter of a Genric Tree

- The diameter is defined as the maximum number of edges between any two nodes in the tree.
- So the diameter between two nodes must contains two leaf nodes so as it can be longest as per it's defination.
- In the left tree, diameter is 5 and in the right tree, the diameter is 8 in the pic below.


![Screenshot (488)](https://user-images.githubusercontent.com/98539013/159484343-7982a5eb-94b9-4c84-bd3c-b4cca6dc3ead.png)

- To be noted that the diameter may not necessarily include the root node as shown in the right tree.

### Properties

- Diameter of a genric tree may not necessarily include the root node.
- Diameter of a genric tree necessarily include two leaf node.

### Algorithm

- Maximize the number of edges between any two nodes to calculate diameter.
- To be noted that to maximize the number of edges have to always consider the leaf nodes.
- Find a diameter that passes through current node,in the function below.
diameter(Node* root)
- Find it by adding the deepest subtree and second deepest subtree and adding 2 to their sum.
- Getting the deepest and second deepest subtree ensures that the maximum possible edges from the current node and 2 is added to link both the leaves.
-  After that compare this ch with ht, if ch is greater than ht then update sh with ht and then ht with ch.
- Once we out of the for loop, compare values of dia (largest diameter) and diameter of current node (ht + sh + 2).
- If the value of diameter of the current node is greater than the value of dia, then update dia with (ht + sh + 2).
- Update ht by adding 1 to it, which gives the height of the node, finally return the updated height.

### Time Complexity
```
- For construct()
O(n), where is number of nodes. 
- The time complexity for the function is linear as tree traversal is involved which is linear in terms of time complexity
O(n), where is number of nodes.
```
### Advantages 

- Memory efficient – No extra links are required, hence a lot of memory is saved.
- We even can visualise how leaf node plays vital role.
- Many algorithms can be expressed more easily because it is just a binary tree.
- Each node is of fixed size no auxiliary array or vector is required.

### Disadvantages

- Need to traverse all the tree to find diameter.
- Unknown number of children – The number of children for each node is not known in advance.

