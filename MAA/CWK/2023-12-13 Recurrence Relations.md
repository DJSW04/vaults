[[2023-12-11 Sigma Notation]]

> *A recurrence relation of the form $U_{n+1} = f(U_n)$ defines each term of a sequence as a function of the previous term*
> *A sequence is increasing if $U_{n+1}>U_{n}$ for all $n \ \epsilon \ N$*
> *A sequence is decreasing if $U_{n+1}<U_{n}$ for all $n \ \epsilon \ N$*
# $Ex.1$
> *Find the first four terms of* $$U_{n+1}=U_n+4$$ Where $U_{1}= 7$

$$
\begin{align}
U_{1}=7 \\
U_{2}=(7)+4=11\\
U_{3}=(11)+4=15\\
U_{4}=(15)+4=19 
\end{align}
$$
---
# $Ex.2$
>*A sequence $a1, a2, a3, ...$ is defined by:* $$\begin{align}a_{1=p}\\ a_{n+1}=(a_{n})^{2}-1, n \ge 1 \end{align}$$ *Where $p<0* 
> 1. *Show that $a_3=p^4-2p^2$*
> 2. *Given that $a_{2}= 0$, find the value of $p$*
> 3. *Find* $\sum\limits_{r=1}^{200}{a_r}$

1. $$
\begin{align}
a_{1}= p \\
a_{2}= p^{2}-1\\
a_{3}= (p^{2}-1)^{2}-1 \\
= p^{4}-2p^{2}+1-1 \\
= p^{4}-2p^{2}
\end{align}
$$
2. $$
\begin{align}
a_{2}=p^{2}-1 \\
p^{2}-1=0 \\
p^{2}=1 \\
p=\sqrt{1} \\
p=\pm 1 \\
p<0 \therefore \ reject \ p=+1 \\
p = -1
\end{align}
$$
3. 
$$
\begin{align}
a_{1}=p=-1\\
a_{2}=(-1)^{2}+1=0 \\
a{3}=(-1)^{4}-2(-1)^{2}=-1 \\ \\
a_{1},a_{2},a_{3},... \\
-1, 0, -1, ... \\ \\
using \ S_{n}=\frac{1}{2}n(a+l)\\
\text{all even numbers = 0, all odd numbers = -1} \ \therefore \ \text{last number (200) } l=0\\
S_{200} = \frac{200}{2}(-1+0)=-100
\end{align}
$$
---
