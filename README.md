# Experiment 17
# Aim:
To study and implement Linked Lists.

# Theory:
Singly linked list is a linear collection of data structures which consists of a sequence of elements where each element (also called a node) has two fields: one for storing the information and another which contains the address of the next element in the list. In almost all of the arrays data components are stored together in the memory whilst in a singly linked list, the data components are not kept together in the memory; every component is stored dynamically by pointing to the next one.

Components of Singly Linked Lists:

→ Node:
Each node contains data or the actual information or value of the node and next which is a pointer or reference to the next node in the list. If it’s the last node, this pointer is null or None.

→ Head:
The first node of the linked list. If the list is empty, the head is null.


Characteristics of Singly Linked Lists:

→ Dynamic Size.

→ Efficient insertions/ deletions of elements.

→ No reverse traversals.


# Code:

```
#include <iostream>
using namespace std;

struct node 
{
    int data;     
    node* next;
};

node* createnode(int value) 
{
    node* newnode = new node();  
    newnode->data = value;       
    newnode->next = nullptr; 
    return newnode;
}


void insertdata(node*& head, int value) 
{
    node* newnode = createnode(value);

    if (head == nullptr) 
    {
        head = newnode;
    } 
    
    else 
    {
        node* temp = head;
        while (temp->next != nullptr) 
        {
            temp = temp->next;
        }
        temp->next = newnode;
    }
}

void display(node* head) 
{
    node* temp = head;

    while (temp != nullptr) 
    {
        cout << temp->data << " ";
        temp = temp->next;
    }
}


int main() 
{
    node* head = nullptr;

    insertdata(head, 10);
    insertdata(head, 20);
    insertdata(head, 30);
    insertdata(head, 40);

    cout << "Singly Linked List: ";
    display(head);

    return 0;
}
```

Conclusion:

→ We learnt about singly linked lists in C++.

→ We learnt the use case of singly linked lists in C++.

