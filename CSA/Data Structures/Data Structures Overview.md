# 4.2 Fundamentals of Data Structures
>DATA STRUCTURES organise/store data to be accessed/modified
# **Data Structures:**
**Arrays:** Stores finite data of the same datatype in a single identifier.
**Records:** Collection of related fields, which are variables.
**Text/Binary Files:** Organised collection of records.
**Record Structure Process:** define record, declare variable/array, assign/retrieve data from record.
## **Static vs. Dynamic Data Structures:**
**Static:** Fixed size, memory immutable, no reallocation.
**Dynamic:** Size can grow/shrink, memory controlled, allocated/deallocated as needed.
### **Advantages/Disadvantages:**
**Static:** + Fixed memory allocation, + Easier programming, - Inefficient use of memory.
**Dynamic:** + Efficient memory usage, - Risk of overflow/underflow, - Harder to program.
## **Algorithms for Queue:**
- **Circular Queues:** Empty when head equals tail, full if tail is one less than head.
- **Priority Queues:** Items join based on priority.
**Insertion:** Check if full, increment tail, insert at tail.
**Deletion/Reading:** Check if empty, copy item at head, increment head.
## **Algorithms for Stack:**
**Insertion:** Check if full, increment pointer, insert at pointer.
**Deletion/Reading:** Check if empty, copy item at pointer, decrement pointer.
## Graph
**Graphs:** Dynamic data structure for navigation, data transmission, etc.
- Graphs consist of vertex/nodes connected by edges/arc
- Edges > Vertex = dense
- Vertex > Edge = sparse
**Weighted Graph:** each edge/arc has a value
**Undirected Graph:** All edges are bidirectional
**Directed:** Some edges are directional
## **Adjacency Matrix vs. Adjacency List:**
**Matrix:** Quick, simple edge management, but wastes memory for sparse graphs.
**List:** Space-efficient, especially for sparse graphs.
## Trees
**Trees:** Connected, undirected, no cycles.
**Binary Trees:**
- Dynamic structure, efficient sorting/searching/retrieval.
- Nodes can have 0/1/2 branches, with left/right pointers.

## Hash Tables
**Hash Tables:** Enables O(1) data retrieval using hashing algorithm and keys.
**Collisions:** Different inputs can produce the same hash. Address collisions through rehashing.
**Hashing Algorithm:**
- A hashing algorithm transforms input into a unique hash value, which cannot be reversed to retrieve the original input.
- It associates values with keys in a table. When inserting a value, it is hashed to generate a key and stored alongside it.
- During lookup, the value is hashed, and the corresponding table position is queried to retrieve the desired information.
**Dictionaries:** Collection of key-value pairs, values accessed by associated key.