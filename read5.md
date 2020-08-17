# A Linked List
is a sequence of Nodes that are connected/linked to each other. The most defining feature of a Linked List is that each Node references the next Node in the link.
## A Linked types:
- Singly
- Doubly
### Singly - Singly
refers to the number of references the node has. A Singly linked list means that there is only one reference, and the reference points to the Next node in a linked list.
### Doubly - Doubly 
refers to there being two (double) references within the node. A Doubly linked list means that there is a reference to both the Next and Previous node.
### Node - Nodes 
are the individual items/links that live in a linked list. Each node contains the data for each link.
### Next - Each node
contains a property called Next. This property contains the reference to the next node.
Head - The Head is a reference type of type Node to the first node in a linked list.
### Current - The Current
reference is a reference type of type Node that is currently being looked at. This node is traditionally used when traversing through a full linked list. When traversing, you typically reset the current to the head to guarantee you are starting from the beginning of the linked list.


The `Next` property is exceptionally important because it will lead us where the next node is and allow us to extract the data appropriately.
The best way to approach a traversal is through the use of a `while()` loop. This allows us to continually check that the Next node in the list is not null. 

## Parts of a linked list
![img](https://miro.medium.com/max/700/1*K0_eV07tJtKQSVGKfP18bw.jpeg)
- A linked list is made up of a series of nodes, which are the elements of the list.
- The starting point of the list is a reference to the first node, which is referred to as the head. 
- The end of the list isn’t a node, but rather a node that points to null, or an empty value.
- A single node is also pretty simple. It has just two parts: data, or the information that the node contains, and a reference to the next node.
