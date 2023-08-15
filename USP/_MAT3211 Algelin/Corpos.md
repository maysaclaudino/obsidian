---
date: 2023-08-08
course: "MAT3211"
ordem: 1
---
**Matéria:** [[Álgebra Linear]]

>[!example] Anterior:
>[[Números]]

## Operações + e .
Em $\mathbb{R}$ temos duas operações $+$ e $\cdot$
$$
\begin{align}
+:& \text{  } \mathbb{R}\times \mathbb{R} \mapsto \mathbb{R} \\
&(a,b)\mapsto +(a,b)\coloneqq a+b \\
\\
\cdot: & \text{  }\mathbb{R} \times \mathbb{R} \mapsto \mathbb{R} \\
	 & (a,b) \mapsto \cdot (a,b) \coloneqq ab
\end{align}
$$

## Definição de Corpo
Seja $F$ um conjunto com duas operações $+$ e $\cdot$, isto é, são funções denotadas por:
$$
\begin{align}
+:& \text{  } F \times F \mapsto F \\
&(a,b)\mapsto +(a,b) \coloneqq a+b \\
\\
\cdot: & \text{  }F \times F \mapsto F \\
	 & (a,b) \mapsto \cdot (a,b) \coloneqq ab
\end{align}
$$
Dizemos que a terna $(F, +, \cdot)$ é um corpo se valem os axiomas:
### Axiomas da Adição
#### A1 Associativa
$$
\begin{align}
(a+b)+c=a+(b+c) \\
\forall a, b, c, \in F
\end{align}
$$

#### A2 Comutativa
$$
\begin{align}
a+b=b+a \\
\forall  a, b \in F
\end{align}
$$

#### A3 Elemento Neutro
$$
\begin{align}
\exists e \in \mathbb{R} \text{ tq. } a+e=0 \\
\forall a \in F
\end{align}
$$

#### A4 Elemento Oposto
$$
\begin{align}
\forall a  & \in F \\
\exists  b  & \in F\text{ tq. }  \\
a+b & =0
\end{align}
$$

### Axiomas da Multiplicação
#### M1 Associativa
$$
\begin{align}
(ab)c=a(bc) \\
\forall a, b, c \in \mathbb{R}
\end{align}
$$

#### M2 Comutativa
$$
\begin{align}
ab=ba \\
\forall a, b \in F
\end{align}
$$

#### M3 Elemento Unidade
$$
\begin{align}
\exists f \in F, f\neq e \text{ tq. }  \\
a\cdot f=a \\
\forall a \in F
\end{align}
$$

#### M4 Inverso
$$
\begin{align}
\forall a  & \in F, a \neq 0 \\
\exists a'  & \in F \text{ tq. } \\
aa' & =f
\end{align}
$$

### Distributiva
$$
\begin{align}
a(b+c)=ab+ac \\
\forall a, b, c \in F
\end{align}
$$
- Dá para provar que $e, f$ são únicos.
	- **Notação:** $e=0$ e $f=1$
- Dá para provar que o oposto e o inverso são únicos.
	- **Notação:** $b=-a$ e $a'=a^{-1}$

## Exemplos
1. Racionais ($\mathbb{Q}$)
2. Reais ($\mathbb{R}$)
3. Complexos ($\mathbb{C}$)

### $Z_{m}$
$Z_{m}=\{ 0,1,2,\dots,m-1 \}$, onde $m\in\mathbb{Z}$ e $m\geq 1$

São os restos da divisão de um inteiro por $m$.

Definimos em $Z_{m}$
-  $a \hat{+}b=r$ , onde $r$ é o resto da divisão de $ab$ por $m$
- $a \hat{\cdot}b=s$ , onde $s$ é o resto da divisão de $ab$ por $m$

Aqui estamos usando o algoritmo da divisão
- Sejam $a,b\in\mathbb{Z}$, $b\neq 0$. Existem $q,r\in\mathbb{Z}$, únicos tais que
	- $a=bq+r$ , onde $0\leq r\leq |b|$

**Exemplos:**
$$
Z_{2}=\{ 0,1 \}
$$

| $\hat{+}$ | _0_ | _1_ |     | $\hat{\cdot}$ | _0_ | _1_ |
| --------- | --- | --- | --- | ------------- | --- | --- |
| _0_       | 0   | 1   |     | _0_           | 0   | 0   |
| _1_       | 1   | 0   |     | _1_           | 0   | 1    |

$$
Z_{4}=\{ 0,1,2,3 \}
$$

| $\hat{+}$ | _0_ | _1_ | _2_ | _3_ |     | $\hat{\cdot}$ | _0_ | _1_ | _2_ | _3_ |
| --------- | --- | --- | --- | --- | --- | ------------- | --- | --- | --- | --- |
| _0_       | 0   | 1   | 2   | 3   |     | _0_           | 0   | 0   | 0   | 0   |
| _1_       | 1   | 2   | 3   | 0   |     | _1_           | 0   | 1   | 2   | 3   |
| _2_       | 2   | 3   | 0   | 1   |     | _2_           | 0   | 2   | 0   | 2   |
| _3_       | 3   | 0   | 1   | 2   |     | _3_           | 0   | 3   | 2   | 1    |

- $2$ é um divisor de zero
- $1^{-1}=1$
- $3^{-1}=3$
- $2$ não tem inverso, por isso $Z_{4}$ não é um corpo

- [*] $(Z_{m},+,\cdot)$ é um corpo se e somente se $m$ é um número primo. 
