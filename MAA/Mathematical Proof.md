A proof is a logical, structured argument to show that a conjecture is always true.
* statement which has been proven is a **theorem**
* statement which is yet to be proven is a **conjecture**

in a mathematical proof you must:
- state assumptions/information you are using
- show every step logically
- cover all possible cases
- write a statement of proof

### Proof by deduction

>Starting from known facts, using logical steps to reach the desired conclusion

---
### $Ex.1$
$$\text{Prove that} \ n^{2}-n \ \text{is an even number for all values of n}$$
Start by factorising:
$$\quad n^{2}-n=n(n-1)$$
If $n$ is ODD, then $n-1$ is EVEN. Hence:
$$\quad n\times(n-1) \Rightarrow ODD\times EVEN = EVEN $$
if $n$ is EVEN, then $n-1$ is ODD. Hence:
$$\quad n \times\ (n-1) \Rightarrow EVEN \times\ ODD = EVEN$$
Conclusion:
$$\therefore \ n^{2}-n \ \text{is even for all values of} \ n$$
### $Ex.2$
$$
\begin{gathered}
\text{The equation} \ kx^{2}+3kx+2=0, \text{where k is a constant, has no real roots.}\\ \text{Prove that} \ k \ \text{satisfies the inequality} \ 0 \le\ k < \frac{8}{9}
\end{gathered}
$$

$kx^{2}+3kx+2=0$, has no real roots, hence $b^{2}-4ac<0$ :
$$
\begin{aligned}
(3k)^{2}-4(k)(2)<0 \\
9k^{2}-8k<0 \\
k(9k-8) <0
\end{aligned}
$$
$y=k(9k-8)$
```desmos-graph
y=k(9k-8)
```
From the graph, we see that when $\ k(9k-8)<0,\ 0<k<\frac{8}{9}$

$$ When \ k = 0: \\
\begin{align} \quad
(0)x^{2}+3(0){x}+2=0 \\
2=0
\end{align}
$$

This is impossible, which means there is no real roots when $k=0$
Hence, combining $0<k<\frac{8}{9}$ and $k=0$ gives $0 \le k < \frac{8}{9}$
in conclusion, k satisfies the inequality $0 \le\ k < \frac{8}{9}$

### $Ex.3$
$$\text{Prove that} \ (3x+2)(x-5)(x+7)\equiv3x^{3}+8x^{2}-101x-70$$
Expand Brackets
$$
\begin{align}
(3x+2)(x^{2}+2x-35)\equiv3x^{3}+8x^{2}-101x-70 \\
3x^{3}+6x^{2}-105x+2x^{2}+4x-70\equiv3x^{3}+8x^{2}-101x-70 \\
3x^{3}+8x^{2}-101x-70\equiv3x^{3}+8x^{2}-101x-70
\end{align}
$$

---
