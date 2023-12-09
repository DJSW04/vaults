
**MAIN FEATURES OF FUNCTIONAL PROGRAMMING**
- **Statements** written as a series of functions
- **Statements** accepts inputs as arguments & returns outputs
- **Stateless** & **Immutability**

_**ADVANTAGES**_
- Code easier to write & interpret
- Easier to predict program behaviour
- Less prone to bugs
- Ideal for processing big data (CPU parallel processing)

---

>A **function** is a rule, that for each element of set A (domain) of inputs, assigns an output chosen from set B (co-domain), but without necessarily using eery member of B.

**FUNCTIONS ARE FIRST-CLASS OBJECTS**
$$ {A ⇒ B \quad Where: f(x) = x^{2}} $$
$\text{A = argument type, B = result type}$

---

>**Function Application** is the process of giving inputs to functions
* Functions only takes one argument (in Haskell)

>**Partial Function Application** is the process of decomposing multi-argument functions into smaller functions with less arguments
- Partial application results in ‘binding’ the value of some of the inputs to a function to produce another more specific function

---

>**Composition of Functions** is the idea that you can combine two functions to get a new function

$$L : A \rightarrow B \Rightarrow K \circ L : A \rightarrow C$$
$A = domain, B = co\text{-}domain$

Function $K \circ L$  is known as the composition of K and L
- Co-domain of L must be the same as the domain of K

---
**HIGHER ORDER FUNCTIONS**
- Takes a function as an argument
- or returns a function as a result
- or does both