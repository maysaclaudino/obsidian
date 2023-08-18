---
numero: 1
course: "MAC0338-lista"
---

**Matéria:** [[Análise de Algoritmos]]

---
# Exercício 1b

Seja $c=1$ e $n_{0}=1$. Queremos mostrar que $\log_{10}n \leq\lg n$, $\forall n\geq n_{0}$. Portanto, como $\lg n=\log_{2}n$:
$$
\begin{align}
\log_{10}n & \leq \log_{2}n \\
\log_{10}n & \leq \frac{\log_{10}n}{\log_{10}2} \\
\log_{10}n \cdot \log_{10}2 & \leq \log_{10}n \\
\log_{10}2 & \leq 1
\end{align}
$$
Que é válido pois $\log_{10}2\cong 0,3\leq 1$.

# Exercício 2d

Seja $c=1$ e $n_{0}=1$. Queremos mostrar que $n\leq 2^{n}$, $\forall n\geq n_{0}$. Por indução:
Base: $n=1$
$$
1\leq 2^{1}
$$
Fixe $n\geq 2$ e assuma que $n-1\leq 2^{n-1}$.
$$
\begin{align}

n & \leq 2^{n} \\
n & \leq 2\cdot n^{n-1} \\
n-1+1 & \leq 2\cdot{2}^{n-1} \\

\end{align}
$$
Pela hipótese de indução:
$$
\begin{align}

\frac{n-1}{n-1}+\frac{1}{n-1} & \leq \frac{2\cdot n^{n-1}}{2^{n-1}} \\
\frac{1}{n-1} & \leq 2 \\
1 & \leq 2n-2 \\
3 & \leq 2n

\end{align}
$$
Que é valido pois fixamos $n\geq 2$.
# Exercício 3b

Se $f(n)=\Theta(g(n))$, então existem $c_{1},c_{2},n_{0}$ tais que para todo $n\geq n_{0}$:
$$
c_{1}g(n)\leq f(n)\leq c_{2}g(n)
$$
Se $g(n)=\Theta(h(n))$, então existem $d_{1},d_{2},m_{0}$ tais que para todo $n\geq m_{0}$:
$$
d_{1}h(n)\leq g(n)\leq d_{2}h(n)
$$
Assim, temos:
$$
\begin{align}
d_{1}h(n) & \leq g(n) \\
c_{1}d_{1}h(n) & \leq c_{1}g(n)
\end{align}
$$
E, também:
$$
\begin{align}
g(n) & \leq d_{1}h(n) \\
c_{2}g(n) & \leq c_{2}d_{2}h(n)
\end{align}
$$
Portanto, para todo $n\geq m_{0}$:
$$
(c_{1}d_{1})h(n)\leq f(n)\leq(c_{2}d_{2})h(n)
$$
Logo, $f(n)=\Theta(h(n))$ 
# Exercício 4a