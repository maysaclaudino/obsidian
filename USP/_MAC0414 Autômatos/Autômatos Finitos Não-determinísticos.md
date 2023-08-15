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