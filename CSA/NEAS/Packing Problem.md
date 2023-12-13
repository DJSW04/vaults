[[NEA Analysis]]
Packing problems use optimisation to pack a storage container as densely as possible (maximising the cargo in the container while minimising the amount of left over space). 

The **Packing Problem** is a well known problem in the field of mathematics.

One of the most common approaches is the Best Fit Decreasing algorithm.
The algorithm starts by ordering the cargo from largest to smallest based on size, and then places the first one in the container in the best spot possible. Then the next one is placed in the best remaining spot (that takes up the least space) in the container (if it fits into it). This process is repeated until the container is full or all cargo has been loaded. If the container isn't full yet, the algorithm goes through the cargo in the same order, but this time it tries 
