---
date: 2023-08-10
course: "MAT3211"
ordem: 1
---

**Matéria:** [[Álgebra Linear]]

---
## Definição
Espaço vetorial sobre um corpo.
Sejam $F$ um corpo, $V$ um conjunto com uma operação de adição indicada por $+$ 
$$
\begin{align}
+: & V\times V\to V \\
	 & (u,v) \mapsto +(u,v)\coloneqq u+v
\end{align}
$$
e uma multiplicação por escalares indicada por $\cdot$
$$
\begin{align}
\cdot: & f\times V\to V \\
	 & (\alpha,u)\mapsto\cdot(\alpha,u)\coloneqq\alpha u
\end{align}
$$
Dizemos que a terna $(V,+,\cdot)$ é um espaço vetorial sobre $F$ ou um $F$-espaço vetorial se valem

### A1: associação da adição
$\forall u,v,w\in V$
$$
(u+v)+w=u+(v+w)
$$
### A2: comutativa da adição
$\forall u,v,w\in V$
$$
u+v=v+u
$$
### A3: elemento neutro
$\exists 0 \in V$ tal que $\forall u\in V$
$$
u+0=u
$$
### A4: elemento oposto
$\forall u\in V, \exists-u\in V$ tal que
$$
u+(-u)=0
$$
### M1: associativa da multiplicação
$\forall \alpha\beta \in F$
$$
\alpha(\beta u)=(\alpha\beta)u
$$
### M2: 
$\forall u\in V$ e $\forall \alpha,\beta \in F$
$$
(\alpha+\beta)u=\alpha u+\beta u
$$
### M3:
$\forall\alpha \in F$ e $\forall u,v \in V$
$$
\alpha(u+v)=\alpha u+\alpha v
$$
### M4:
$\forall u \in V$
$$
1\cdot u=u
$$