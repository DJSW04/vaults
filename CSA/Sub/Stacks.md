[[Data Structures Overview]]

---
- [ ] *Be able to describe and apply the following operations:*
	- push
	- pop
	- peek or top
	- test for empty stack
	- test for stack full.
---
>A stack is a first in, last out (FILO) abstract data structure. Like queues, stacks are often based on an array but have just one pointer: a top pointer.

You can think of stacks as a pile of students’ books which need to be marked by a teacher. The first book to be handed in is placed at the bottom of the stack and is the last to be marked. The last book to be added to the stack is the first to be marked. 

Operations that can be performed on a stack include Push​ (add an item), Pop​ (remove the item at the top) and Peek​. Peek​ is a function which returns the value of the item at the top of the stack without actually removing the item. The functions 'IsFull' and 'isEmpty​' can also be executed on stacks, just like with a queue.

**Insertion:** Check if full, increment pointer, insert at pointer.
**Deletion/Reading:** Check if empty, copy item at pointer, decrement pointer.