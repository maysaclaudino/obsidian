---
date: 2023-08-29
course: "MAC0338"
ordem: 1
annotation-target: slides/aula04_particao.pdf
---

**Matéria:** [[Análise de Algoritmos]]

---
# Problema: Particione
_Página 1_
- A escolha do pivot é o programador que decide aqui escolhemos $r=$ última posição
_Página 5_
- Todo mundo antes de $i$ é $\leq x$ e todo mundo depois é $>$ 

# Outro
- Devolve o índice novo do pivot
# Consumo de tempo
_Página 24_
_Página 26_
- $n\coloneqq r-p+1$ tamanho do trecho
- $O(n)$ pois pode ser que não execute nenhuma vez
# Quicksort
_Página 27_
_Página 41_
- $T(k)$ chamada da esquerda
	- Inclui o pivot
- $T(n-k-1)$ chamada da direita
	- Não inclui o pivot
		- Por isso o $-1$
# Recorrência
_Página 42_
- Pior caso
	- Quando está ordenado
_Página 42_
- $T(n-1)+\Theta(n)=\Theta(n^{2})$ como visto [[Resolução de recorrências|anteriormente]] 
## Recorrência cuidadosa
_Página 45_
_Página 46_
- Estabelecemos as bases $T(0)$ e $T(1)$ 
- Para $n=2$
	- $\text{max}\{ 2, 2 \}$
- Para $n=3$
	- $\text{max}\{ 5, 2, 5 \}$
- Para $n=4$
	- $\text{max}\{  \}$
- Vimos que o $\text{max}$ é nos extremos
![](https://i.imgur.com/IzZGIQb.jpg)
### Prova por indução
_Página 51_
- $k$ e $n-k-1$ são menores que $n$
- Hipótese $\to n^{2}+1$ 
- Função quadrática é uma parábola para cima
	- O máximo de um intervalo é sempre em uma das pontas
		- O máximo dá nas extremidades
	- Nossa parábola está centralizada
	- O [[mínimo é o melhor caso]]
![](https://i.imgur.com/gBLPOI4.jpg)
