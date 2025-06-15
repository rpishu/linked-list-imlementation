# linked-list-imlementation
company: CODTECH IT SOLUTIONS
NAME: Rishu Priyadarshi
INTREN ID: CTO4DN1458
DURATION: 4 WEEKS
MENTOR: Neela Santhosh kumar




A linked list is a sequential data structure that stores the data in non-contiguous memory locations unlike array. In a linked list, each element is referred to as a node. Each node in the linked list stores data and a pointer to the next node present in the list.

Example

Input: 1 -> 2 -> 3 -> 4 -> NULL
Output: 1 2 3 4
Explanation: The linked list is created with nodes containing values 1, 2, 3, and 4 in sequence.

Input: 10 -> 20 -> 30 -> NULL
Output: 10 20 30
Explanation: The linked list is created with nodes containing values 10, 20, and 30 in sequence.

Create a Linked List in C
Even the simplest linked list node needs to contain a pointer to the next and at least one data field. In C, we can use the structure type to group the multiple data types in a single variable. So, we can represent a linked list node using the structure. The whole linked list can be then represented using the pointer to the head node (first node in the list).

Below is the step-by-step guide to create a linked list in C language:

1. Representation of Linked List Node in C
Below is an example structure that represents a linked list node:

struct Node {

    // Example data field
    int data;

    // Example of the next pointer
    Node* next;
}
2. Creating a Node of Linked List
We can create the structure variables i.e. nodes using dynamic memory allocation and structure pointer. Although, we can also do it statically, dynamic allocation is preferred to make the full use of the abilities of the linked list.

struct Node* node2 = (struct Node*)malloc(sizeof(struct Node));
Shortening the Node Declaration


If you feel that using the struct Node* every time makes the statement unnecessarily complex, you can use the typedef to define an alias for it.

typedef struct node {
   int data;
   struct node* next;
}Node;
Then we can create the Node as:

Node* node2 = (Node*) malloc(sizeof(Node));
3. Chaining/Linking the Nodes of the Linked List
The created nodes can be joined by placing the pointer of the next node in the next variable of the current node resulting in the linked list data structure. The last node in the list should contain the NULL as its next pointer to mark the end of the list.

// Assigning data
node1->data = valid_value
// Assigning Next node
node1->next = node2

// Same for node 2
node2->data = valid_value;
node2->next = NULL;
C Program Create a Linked List
The below example implements the above approach and create a linked list in C:




// C Program to create a Linked List
#include <stdio.h>
#include <stdlib.h>
​
// Define the structure of Node
typedef struct Node {
  
    // Data field. Can add more data according to our need
    int data;
​
    // Pointer to the next node
    struct Node *next;
} Node;
​
int main() {
  
    // Create the First Node of the Linked List
    // This will serve as the head of the list
    Node *first = (Node *)malloc(sizeof(Node));
​
    // Assigning data
    first->data = 10;
​
    // Creating the second node in the list
    Node *second = (Node *)malloc(sizeof(Node));
​
    // Assigning data
    second->data = 20;
​
    // Creating the third node
    Node *third = (Node *)malloc(sizeof(Node));
​
    // Assigning data
    third->data = 30;
​
    // Linking the nodes
    first->next = second; // This will create: 10 -> 20
    second->next = third; // This will create: 10 -> 20 -> 30
    third->next = NULL;   // This will create: 10 -> 20 -> 30 -> NULL
​
    printf("Linked List: ");
    Node* temp = first;
    while(temp) {
      printf("%d ", temp->data);
      temp = temp->next;
    }
​
    return 0;
}

Output
Linked List: 10 20 30 
Time Complexity: O(N) where N is the total number of nodes in the linked list.
Auxiliary Space: O(N)

Note: Although we haven't done it hereA linked list is a sequential data structure that stores the data in non-contiguous memory locations unlike array. In a linked list, each element is referred to as a node. Each node in the linked list stores data and a pointer to the next node present in the list.

Example

Input: 1 -> 2 -> 3 -> 4 -> NULL
Output: 1 2 3 4
Explanation: The linked list is created with nodes containing values 1, 2, 3, and 4 in sequence.

Input: 10 -> 20 -> 30 -> NULL
Output: 10 20 30
Explanation: The linked list is created with nodes containing values 10, 20, and 30 in sequence.

Create a Linked List in C
Even the simplest linked list node needs to contain a pointer to the next and at least one data field. In C, we can use the structure type to group the multiple data types in a single variable. So, we can represent a linked list node using the structure. The whole linked list can be then represented using the pointer to the head node (first node in the list).

Below is the step-by-step guide to create a linked list in C language:

1. Representation of Linked List Node in C
Below is an example structure that represents a linked list node:

struct Node {

    // Example data field
    int data;

    // Example of the next pointer
    Node* next;
}
2. Creating a Node of Linked List
We can create the structure variables i.e. nodes using dynamic memory allocation and structure pointer. Although, we can also do it statically, dynamic allocation is preferred to make the full use of the abilities of the linked list.

struct Node* node2 = (struct Node*)malloc(sizeof(struct Node));
Shortening the Node Declaration


If you feel that using the struct Node* every time makes the statement unnecessarily complex, you can use the typedef to define an alias for it.

typedef struct node {
   int data;
   struct node* next;
}Node;
Then we can create the Node as:

Node* node2 = (Node*) malloc(sizeof(Node));
3. Chaining/Linking the Nodes of the Linked List
The created nodes can be joined by placing the pointer of the next node in the next variable of the current node resulting in the linked list data structure. The last node in the list should contain the NULL as its next pointer to mark the end of the list.

// Assigning data
node1->data = valid_value
// Assigning Next node
node1->next = node2

// Same for node 2
node2->data = valid_value;
node2->next = NULL;
C Program Create a Linked List
The below example implements the above approach and create a linked list in C:




// C Program to create a Linked List
#include <stdio.h>
#include <stdlib.h>
​
// Define the structure of Node
typedef struct Node {
  
    // Data field. Can add more data according to our need
    int data;
​
    // Pointer to the next node
    struct Node *next;
} Node;
​
int main() {
  
    // Create the First Node of the Linked List
    // This will serve as the head of the list
    Node *first = (Node *)malloc(sizeof(Node));
​
    // Assigning data
    first->data = 10;
​
    // Creating the second node in the list
    Node *second = (Node *)malloc(sizeof(Node));
​
    // Assigning data
    second->data = 20;
​
    // Creating the third node
    Node *third = (Node *)malloc(sizeof(Node));
​
    // Assigning data
    third->data = 30;
​
    // Linking the nodes
    first->next = second; // This will create: 10 -> 20
    second->next = third; // This will create: 10 -> 20 -> 30
    third->next = NULL;   // This will create: 10 -> 20 -> 30 -> NULL
​
    printf("Linked List: ");
    Node* temp = first;
    while(temp) {
      printf("%d ", temp->data);
      temp = temp->next;
    }
​
    return 0;
}

Output
Linked List: 10 20 30 
Time Complexity: O(N) where N is the total number of nodes in the linked list.
Auxiliary Space: O(N)

Note: Although we haven't done it here for simplicity, it is recomfor simplicity, it is recom

output 


