
<!-- Table of content -->
# Table of content
  - [Segregate Even Odd](#segregate-even-odd)
    - [Algorithm](#algorithm)
    - [Properties](#properties)
    - [Advantages](#advantages)
    - [Disadvantage](#disadvantage)
  - [Palindrome linked list](#palindrome-linked-list)
  - [Reverse a Linked List](#Reverse-Linked-List)

# Segregate Even Odd

The Problem Statement : Give a Linked List of integer, write a function to modify the linked list such that all even numbers appear before all the odd numbers in the modified linked list. Also, keep the order of even and odd numbers the same

### Task perform 
- Comparision Linkedlist elements
- Insertion a node in Linkedlist in Front
- Insertion a node in Linkedlist in End


### Explanation 
 - First Step is we take a length of LinkedList as input.
 - Second Step is to take input of the Head Node.
 - Pointing tail and head to the Head node.
 - Create a for loop in length -1 times because we alrady take the head.
 - We create a function who compair the input element passing with Head and tail  with the input data.
 -  Oddevenchecker funciton to check if the data is odd the call InsertAtTail function to Insert in End of the Head Node of the LinkedList. Or if the data is even the call InsertAtHead function to insert Node in Front Head of the LinkedList.
 - After all thing call function print to print LinkedList.

![screenshot-185-7838](https://user-images.githubusercontent.com/55774240/158155742-e661bcba-296a-47f8-b43f-bd65c603d053.png)
### Algorithm

```
Write Pseudo code for your algorithm here
```

### Properties

- Time Complexity : Insert element at front O(1), Insert element at end O(N) = O(N)
- Auxillary Space : No extra space used = O(1)

### Advantages

- 

### Disadvantage

- 

---

### Singly Linked List 

1. Create a SLL 
2. Display a SLL 
3. Insert a node in SLL 
4. Delete a node in SLL 

### Creating Singly Linked List 

**Steps :**  

1. Create an array and store elements in array.
2. Create nodes using malloc function and store elements of array in Linked List. 

**Space Complexity** 

Extra space is used to store elements of LL in array.  
Space Complexity : O(n) 

### Displaying the Singly Linked List 

**Steps :**

1. Use the pointer and display node data until node becomes null.

**Time Complexity** 

1. Displaying the first node => O(1) 
2. Displaying a node in between => O(n) 
3. Displaying the last node => O(n) 

**Space Complexity** 

No extra space is used.   
Space Complexity : O(1)  

### Inserting a node in Singly Linked List 

**Steps :** 

1. Inserting a node at first position will shift first or head pointer to new node.
2. For inserting a node in between, bring temporary pointer p to the position. 

Inserting at first position : 

![Linkedlist_insert_at_start](https://user-images.githubusercontent.com/81226536/157304956-2cee37f1-5cda-455a-ad4a-477b74cdad01.png) 


Insert a node at nth position in the linked list
---
To insert a node at nth position, we need to follow these steps-
* Create a new node
* Iterate to the previous of the nth node
* Set newnode's ‘next’ pointer to the ‘next’ pointer of the previous of the nth node
* Set previous node's next to the new node
* Return the head pointer

Time Complexity
------------------------
* Insertion at head node - O(1).
* Insertion at last node - O(n).
* Insertion in middle - O(n). 

Space Complexity
-----------
* Space complexity: O(1).


Image to show the insertion
---

![insertion-in-singly-linked-list-at-beginning](https://user-images.githubusercontent.com/86103131/157711281-4a6a00be-1a58-4fca-af71-e5b5a1a31e89.png)

 
**Time Complexity** 

1. Inserting the first node => O(1) 
2. Inserting a node in between => O(n) 
3. Inserting the last node => O(n) 

**Space Complexity** 

No extra space is used.  
Space Complexity : O(1) 

### Deleting a node in Singly Linked List 

**Steps :**

1. Find the previous node of the node to be deleted. 
2. Change the next of the previous node. 
3. Free memory for the node to be deleted.


Deleting a node  : 

![Linkedlist_deletion](https://user-images.githubusercontent.com/81226536/157306410-645f3871-7d8d-4f01-8492-66862d6da268.png) 

**Time Complexity** 

1. Deleting the first node => O(1) 
2. Deleting a node in between => O(n) 
3. Deleting the last node => O(n) 

**Space Complexity** 

No extra space is used.   
Space Complexity : O(1)
***
# Palindrome linked list

In this approach, I have used a stack to store all the elements after the middle
element so that We have to compare only (n/2)-1 elements to find out the list is palindrome or not.

### Algorithm

* Find the middle node of the linked list
* Add all the elements after the middle element in the stack
* Compare the elements of the linked list with the top element of the stack
* If the element of the stack and the linked list is same,
  Iterate to the next element in the linked list and pop the element of the stack
* Repeat 4th point till stack is empty (or we have reached the middle element of the list)
* If we have successfully popped all the element of the stack, Return 1

  Else Return 0

### Time Complexity

* The time complexity of this approach will be O(n)
  - But we have to compare only (n/2)-1 time as we have stored all the elements after the middle in the stack and we are comparing 
    the elements of the linked list only till the previous of the middle node.

### Space Complexity

* Space complexity will be O(n) as we are using a stack to store the elelments of the linked list.

### Advantages

* Less comparison
* Easy approach

### Disadvantage
* Takes O(n) Auxilary space.


# To reverse a Linked List 
Given pointer to the head node of a linked list, the task is to reverse the linked list. We need to reverse the list by changing the links between nodes.
## Example
Input: Head of following linked list 
1->2->3->4->NULL 
Output: Linked list should be changed to, 
4->3->2->1->NULL
### To reverse a linked list, do the following.
1. Initialize three pointers prev as NULL, curr as head and next as NULL
2. Iterate through the linked list. In loop, do following,
    
    
    
    next = curr->next
    
    
    
    curr->next = prev 
    
    
    
    prev = curr 
    
    
    
    curr = next
## Time Complexity and Space Complexity
1.Time Complexity: O(n) 
2.Space Complexity: O(1)

## Image for Reference
![image](https://user-images.githubusercontent.com/74498344/158961580-61a95b47-fa77-4547-bfe1-7288fb8aa88b.png)

