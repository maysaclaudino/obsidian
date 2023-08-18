---
date: 2023-08-15
course: "MAC0414"
ordem: 
annotation-target: slides/
---

**Matéria:** [[Autômatos, Computabilidade e Complexidade]]

---
## Definição
\p
- Quando vai para um caminho que não existe, "explode"
	- Se todos os caminhos explodirem rejeita.
- Aumenta o poder de expressão
### Simulação de aceite
\p
- No final aceita porque um deles aceitou
- Se na árvore de arborescência tiver um que aceita no final, aceita tudo
- Reconhece qualquer string que tem a subtring 101 ou
## $N_{1}$ e suas partes
\p
- Onde tem $\epsilon$ explode

## Outro
- Um AFN tem o mesmo poder computacional que um determinístico
	- Se quero fazer a união é só colocar um estado inicial com transição $\epsilon$ para $M_{1}$ e $M_{2}$ 
- AFN: $(Q,\Sigma,\delta,s,F)$
	- $\delta:Q\times\Sigma \cup \{ \epsilon \}\to P(Q)$
### Anatomia da computação
- Se $N=(Q,\Sigma,\delta,s,F)$ e $w=w_{1}w_{2}\dots w_{n}$, $n$ aceita $w$ se:
	- $w=y_{1}y_{2}y_{3}\dots y_{n}$ 
	- Existem estados $r_{1},r_{2},\dots r_{n}$ tais que:
		- $r_{0}=s$
		- $r_{i+1}=\delta(r_{1},w_{i+1})$ , onde $i=0,\dots,n-1$
		- $r_{n}\in F$ 

## Transformando NFA em [[Autômatos finitos Determinísticos|DFA]]
- Construção por partes
	- Powerset construction
	- Rabin & Scott

- Se um NFA reconhece uma linguagem $A$, então $A$ é regular
	- $N=(Q,\Sigma,\delta,s,F)$ e $A=L(N)$
	- Usamos $N$ para construir $M=(Q',\Sigma,\delta',s',F')$
		- $Q'=\mathcal{P}(Q)$
		- $\delta'(R,a)=\{ q\in Q:q\in E(\delta(r,a))\text{ , } r\in R\}$ 
			- $E(R)=$ $\{$ estado de $Q$ alcançados a partir de $R$ percorrendo 0 ou mais $\epsilon$\-transições $\}$
			- Para $R\in \mathcal{P}(Q)$ e $a\in\Sigma$ 
		- $s'=E(\{ s \})$
		- $F'=\{ R\in\mathcal{P}(Q)\varepsilon \cap F\neq \emptyset \}$ 

- Se $A_{1}$ e $A_{2}$ são linguagens regulares, então $A_{1}\cup A_{2}$ é regular
- Se $A_{1}$ e $A_{2}$ são linguagens regulares, então $A_{1} o A_{2}$ é regular
- Se $A$ é uma linguagem regular, então $A*$ é regular
	- Operador Kleene
		- $\Sigma$ é um alfabeto
			- $\Sigma ^{k}$ são todas as strings com $k$ símbolos
			- $\Sigma=\{ 0,1 \}$
			- $\Sigma ^{0}=\{ \epsilon \}$
			- $\Sigma^{2}=\{ 00,01,10,11 \}$
			- $\Sigma ^{4}=\{ 0000,0001,0010,\dots \}$
			- $\Sigma*=\{ \epsilon,0,1,00,01,\dots,10010 \}$
				- $\Sigma*=\{ w:w=a_{1}a_{2}\dots a_{k}\text{ , }k\geq 0 \text{ e } a_{1},a_{2},\dots,a_{k}\in\Sigma \}$
		- $A=\{ aa,b \}$ e $\Sigma=\{ a,b \}$
			- $A^{2}=\{ abb,baa,aaaa,bb \}$
			- $A*=\{ w=x_{1}x_{2}\dots x_{k},k\geq 0,x_{i}\in A \}$ 