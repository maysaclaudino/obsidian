---
date: 2023-08-11
course: "MAC0338"
---
**Matéria:** [[Análise de Algoritmos]]

## Algoritmo do Insertion Sort

Rearranja o vetor $A[1\dots n]$ em ordem crescente

![](https://i.imgur.com/USrMUSl.png)

## Quantas atribuições o algoritmo faz?
- O loop `for` esconde algumas atribuições.
![](https://i.imgur.com/5QkJydJ.png)
### Linhas 3-6
- Vamos considerar os elementos $(A,j,\text{chave})$
![](https://i.imgur.com/AdRqxCy.png)

| linha     | atribuições (max) |
| --------- | ----------------- |
| 3         | 1                 |
| 4         | 0                 |
| 5         | $\leq j-1$        |
| 6         | $\leq j-1$        |
| **total** | $\leq 2j-1$                 |

- Em termos de $n$ o total é $2n-1$

### Todas as linhas
- Vamos considerar os elementos $(A,n)$
![](https://i.imgur.com/mVH6sEW.png)

| linha     | atribuições (max) |
| --------- | ----------------- |
| 1         | $n-1+1$               |
| 2         | $n-1$             |
| 3-6       | $\leq(n-1)(2n-1)$     |
| 7         | $n-1$             |
| **total** | $2n^{2}-1$        | 

#### E se usarmos $2j-1$ como limitante?
$$
\begin{align}
(n-1)(2n-1) \\
(n-1)(2j-1) \\
(2\cdot 2-1)+(2\cdot 3-1)+\dots+(2\cdot(n-1)+1) & \text{ , para }j=2,\dots,j=n-1 \\
3+5+\dots+(2n-1) \\
\frac{(2n+2)(n-1)}{2} & \text{ , soma da P.A.} \\
(n+1)(n-1) \\
n^{2}-1
\end{align}
$$

Logo, temos:

| linha     | atribuições (max) |
| --------- | ----------------- |
| 1         | $n-1+1$               |
| 2         | $n-1$             |
| 3-6       | $\leq n^{2}-1$     |
| 7         | $n-1$             |
| **total** | $\leq2n^{2}+3n-3$        | 

## $n^{2}+3n-3$ vs. $n^{2}$


a

>[!example] Próximo:
>