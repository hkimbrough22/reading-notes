# Code 401 - Reading Notes
<!-- All references used were from Code 401 reading
assignment 10-->
[comment]: <> (https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/stacks_and_queues.html)
## Stacks and Queues
- A stack is a data structure that consists of Nodes. Each Node references the next Node in the stack, but does not reference its previous.
- Common Terms:
  - Push - Nodes or items that are put into the stack are pushed
  - Pop - Nodes or items that are removed from the stack are popped. When you attempt to pop an empty stack an exception will be raised.
  - Top - This is the top of the stack.
  - Peek - When you peek you will view the value of the top Node in the stack. When you attempt to peek an empty stack an exception will be raised.
  - IsEmpty - returns true when stack is empty otherwise returns false.

![Stack](../stack1.png)

## Queue
- Common terminology:
  - Enqueue - Nodes or items that are added to the queue.
  - Dequeue - Nodes or items that are removed from the queue. If called when the queue is empty an exception will be raised.
  - Front - This is the front/first Node of the queue.
  - Rear - This is the rear/last Node of the queue.
  - Peek - When you peek you will view the value of the front Node in the queue. If called when the queue is empty an exception will be raised.
  - IsEmpty - returns true when queue is empty otherwise returns false.

![Queue](../Queue.png)



[BACK TO HOME](../README.md)