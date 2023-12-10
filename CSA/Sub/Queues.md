[[Data Structures Overview]]

---
- [ ] *Be able to describe and apply the following to linear queues, circular queues and priority queues:
	- add an item
	- remove an item
	- test for an empty queue
	- test for a full queue.
---
>A queue is an abstract data structure based on an array. Just like a queue at a bus stop, the first item added to a queue is the first to be removed. Because of this, queues are referred to as “first in, first out” (or FIFO) abstract data structures.

- **Circular Queues:** Empty when head equals tail, full if tail is one less than head.
- **Priority Queues:** Items join based on priority.

**Insertion:** Check if full, increment tail, insert at tail.
**Deletion/Reading:** Check if empty, copy item at head, increment head.

---
>a queue is a collection of entities that are maintained in a sequence and can be modified by the addition of entities at one end of the sequence and the removal of entities from the other end of the sequence. By convention, the end of the sequence at which elements are added is called the back, tail, or rear of the queue, and the end at which elements are removed is called the head or front of the queue, analogously to the words used when people line up to wait for goods or services.
## Linear Queues
>A linear queue has two pointers, a front pointer and a rear pointer. These can be used to identify where to place a new item in a queue or to identify which item is at the front of the queue.
## Priority Queues
>In a priority queue, items are assigned a priority. Items with the highest priority are dequeued before low priority items. In the case that two or more items have the same priority, the items are removed in the usual first in, first out order.

Priority queues are frequently used in computer systems. For example, processors assign time to applications according to their priority. Applications currently in use by the user are prioritised over background applications, allowing for a faster user experience. 

A school or college may enforce a priority printer queue, in which staff print jobs are completed before those submitted by students.

## Circular Queues
>A circular queue is a type of queue in which the front and rear pointers can move over the two ends of the queue, making for a more memory efficient data structure.

