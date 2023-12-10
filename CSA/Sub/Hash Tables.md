[[Data Structures Overview]]

---
- [ ] *Be familiar with the concept of a hash table and its uses.*
- [ ] *Be able to apply simple hashing algorithms.*
- [ ] *Know what is meant by a collision and how collisions are handled using rehashing.*
---
**Hash Tables:** Enables O(1) data retrieval using hashing algorithm and keys.
**Collisions:** Different inputs can produce the same hash. Address collisions through rehashing.
**Hashing Algorithm:**
1. A hashing algorithm transforms input into a unique hash value, which cannot be reversed to retrieve the original input.
2. It associates values with keys in a table. When inserting a value, it is hashed to generate a key and stored alongside it.
3. During lookup, the value is hashed, and the corresponding table position is queried to retrieve the desired information.
