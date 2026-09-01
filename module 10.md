EXP NO:16 C PROGRAM TO SEARCH A GIVEN ELEMENT IN THE GIVEN LINKED LIST.
Aim:
To write a C program to search a given element in the given linked list.

Algorithm:
1.	Define the structure for a node in a linked list.
2.	Define the search function to find a specific character in the linked list.
3.	Initialize the head of the linked list as needed.
4.	Call the search function and perform other linked list operations as needed.
 
Program:

```
struct Node{
    char data; 
    struct Node *next;
}*head;

void search(char data)
{
struct Node*ptr;
int i=0,flag=0;
ptr=head;
if(ptr==NULL)
{
printf("Empty List\n");
return;
}
while(ptr!=NULL)
{
i++;
if(ptr->data==data)
{
printf("item %c found at location %d",ptr->data,i);
flag=1;
}
ptr=ptr->next;
}
if(!flag)
{
printf("Item not found");
}
}

```

Output:

<img width="863" height="528" alt="image" src="https://github.com/user-attachments/assets/54b2dcf5-3272-4210-a0fe-c8afc5949cbc" />



Result:
Thus, the program to search a given element in the given linked list is verified successfully.


 
EXP NO:17  PROGRAM TO INSERT A NODE IN A LINKED LIST.
Aim:
To write a C program to insert a node in a linked list.
Algorithm:
1.	Define the structure for a node in a linked list
2.	Define the insert function to insert a new node with character data at the end of the linked list.
3.	Initialize the head of the linked list as needed.
4.	Call the insert function and perform other linked list operations as needed.
 
Program:

```

struct Node{
    char data; 
    struct Node *next;
}*head;


void insert(char data)
{
    struct Node *n=(struct Node*)malloc(sizeof(struct Node));
    struct Node*temp;
    if(head==NULL)
    {
        head=n;
        head->data=data;
        n->next=NULL;
        return;
    }
    temp=head;
    while(temp->next!=NULL)
    {
        temp=temp->next;
    }
    n->data=data;
    n->next=NULL;
    temp->next=n;
}
    
```

Output:

<img width="431" height="558" alt="image" src="https://github.com/user-attachments/assets/3f15ce9c-0687-40d5-9b78-2d35a4a9d05d" />

 
Result:
Thus, the program to insert a node in a linked list is verified successfully.


 
EXP NO:18 C PROGRAM TO TRAVERSE A DOUBLY LINKED LIST
Aim:
To write a C program to traverse a doubly linked list.

Algorithm:
1.	Initialize a temporary pointer (temp) to the head of the list.
2.	Use a while loop to traverse the list until the end (temp == NULL) is reached.
3.	Inside the loop, print the data of the current node.
4.	Move to the next node by updating the temp pointer to point to the next node (temp = temp->next).
 
Program:

```

struct Node
{
    struct Node *prev;
    struct Node *next;
    int data;
}*head;

void display()
{
    if(head==NULL)
    {
        return;
    }
    struct Node*temp=head;
    while(temp!=NULL)
    {
        printf("%d\n",temp->data);
        temp=temp->next;
    }
}
     
```

Output:

<img width="437" height="522" alt="image" src="https://github.com/user-attachments/assets/bb80b278-4925-4417-8948-9e5d9d21b916" />



Result:
Thus, the program to traverse a doubly linked list is verified successfully. 



EXP NO:19 C PROGRAM TO INSERT AN ELEMENT IN DOUBLY LINKED LIST
Aim:
To write a C program to insert an element in doubly linked list

Algorithm:
1.	Create a new node (newNode) and allocate memory for it.
2.	Set the data of the new node to the provided value.
3.	If the list is empty, set the new node as the head.
4.	If the list is not empty, traverse the list to find the last node.
5.	Set the new node's prev pointer to the last node and update the last node's next pointer to the new node.
 
Program:

```

struct Node {
    float data;
    struct Node* prev;
    struct Node* next;
};
struct Node* head = NULL;
void insert(float value) {
    struct Node* newNode = (struct Node*)malloc(sizeof(struct Node));
    newNode->data = value;
    newNode->prev = NULL;
    newNode->next = NULL;
    if (head == NULL) {
        head = newNode;
    } else {
        struct Node* temp = head;
        while (temp->next != NULL) {
            temp = temp->next;
        }
        temp->next = newNode;
        newNode->prev = temp;
    }
}

```

Output:

<img width="765" height="520" alt="image" src="https://github.com/user-attachments/assets/5693a1ca-89de-44fc-94a5-b6c4a9f7a0ab" />



Result:
Thus, the program to insert an element in doubly linked list is verified successfully.




EXP NO:20 C FUNCTION TO DELETE A GIVEN ELEMENT IN THE GIVEN LINKED LIST




Aim:
To write a C function that deletes a given element from a linked list.

Algorithm:
1.	Check if the Linked List is Empty:
o	If the head of the linked list is NULL, print a message indicating the list is empty and exit the function.
2.	Traverse the Linked List:
o	Start from the head node and iterate through the list to find the node that contains the given element (data).
3.	Handle Deletion of the First Node:
o	If the element to be deleted is found in the head node:
	Update the head of the linked list to point to the next node (i.e., head = head->next).
	Free the memory allocated to the node to be deleted.
	Exit the function.
4.	Traverse and Delete from the Middle or End:
o	If the element is not in the head node, continue traversing the list by checking each node’s next pointer.
o	When the node with the element is found, update the previous node’s next pointer to point to the next node of the node to be deleted (prev->next = current->next).
o	Free the memory allocated to the node to be deleted.
5.	Handle the Case when the Element is Not Found:
o	If the element is not found in any node, print a message indicating the element is not present in the list.
6.	End the Function.


Program:

```

struct Node{
char data;
struct Node*next;
}*head;
void delete()
{
if(head==NULL)
{
printf("List is empty");
return;
}
struct Node*ptr=head;
printf("Node deleted from the begining...\n");
head=head->next;
free(ptr);
}

    
```

Output:

<img width="843" height="597" alt="image" src="https://github.com/user-attachments/assets/e5ff7b97-e5db-4e14-afbb-422be82c89cb" />






Result:
Thus, the function that deletes a given element from a linked list is verified successfully.





