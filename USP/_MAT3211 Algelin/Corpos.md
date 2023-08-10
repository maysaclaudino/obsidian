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
+:& \text{  } \mathbb{R}\times \mathbb{R}\implies \mathbb{R} \\
&(a,b)\mapsto +(a,b)\coloneqq a+b \\
\\
\cdot: & \text{  }\mathbb{R} \times \mathbb{R} \mapsto \mathbb{R} \\
	 & (a,b) \mapsto \cdot (a,b) \coloneqq ab
\end{align}
$$

## Definição de Corpo
Seja $F$ um conjunto com duas operações $+$ e $\cdot$, isto é
$$
\begin{align}
+:& \text{  } F \times F \implies F \\
&(a,b)\mapsto +(a,b) \coloneqq a+b \\
\\
\cdot: & \text{  }F \times F \mapsto F \\
	 & (a,b) \mapsto \cdot (a,b) \coloneqq ab
\end{align}
$$
Então $(F, +, \cdot)$ é um corpo de valores:
### Axiomas da Adição
#### Associativa
$$
\begin{align}
(a+b)+c=a+(b+c) \\
\forall a, b, c, \in F
\end{align}
$$

#### Comutativa
$$
\begin{align}
a+b=b+a \\
\forall  a, b \in F
\end{align}
$$

#### Elemento Neutro
$$
\begin{align}
\exists e \in \mathbb{R} \text{ tq. } a+e=0 \\
\forall a \in F
\end{align}
$$

#### Elemento Oposto
$$
\begin{align}
\forall a  & \in F \\
\exists  b  & \in F\text{ tq. }  \\
a+b & =0
\end{align}
$$

### Axiomas da Multiplicação
#### Associativa
$$
\begin{align}
(ab)c=a(bc) \\
\forall a, b, c \in \mathbb{R}
\end{align}
$$

#### Comutativa
$$
\begin{align}
ab=ba \\
\forall a, b \in F
\end{align}
$$

#### Elemento Unidade
$$
\begin{align}
\exists f \in F, f\neq e \text{ tq. }  \\
a\cdot f=a \\
\forall a \in F
\end{align}
$$

#### Inverso
$$
\begin{align}
\forall a  & \in F, a \neq 0 \\
\exists a'  & \in F \text{ tq. } \\
aa' & =f
\end{align}
$$

#### Distributiva
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

---
>[!example] Próximo tópico
>
