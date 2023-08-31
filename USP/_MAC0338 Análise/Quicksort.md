---
date: 2023-08-31
course: "MAC0338"
ordem: 0
annotation-target: slides/aula04_quicksort.pdf
---

**Matéria:** [[Análise de Algoritmos]]

---
# No melhor caso
_Página 2_
# Caso médio
_Página 4_
# Exercício
_Página 5_
- Supomos que ele sempre divide o vetor em $\frac{1}{3}$ e $\frac{2}{3}$ 
	- É $\Theta(n\lg n)$. Porque?
- $T\left( \frac{n}{3}+T\left( \frac{2n}{3}+\Theta(n) \right) \right)$
	- Substituímos $\Theta(n)$ por somente $n$
# Árvore da recorrência
_Página 6_
- Cada nó é uma chamada recursiva
	- Colocamos a constante de cada chamada
- Faz até chagar na base da recursão
- Não é uma prova, é para ganhar intuição
- Esses $n+n+n\dots$ é a soma de cada nível
	- A soma é no máximo $n$ pois uma hora "acaba" os níveis da esquerda
_Página 7_
- Os $1+\dots+1$ vem das folhas
- A notação $O()$ permite fazermos a mudança de base
- O ramo da esquerda chega na base na altura $\log_{3}n$ e o da direita em $\log_{\frac{3}{2}}n$ 
# Recorrência
_Página 8_
- $n\geq 4$ 
- Por que $20$? Porque sim. Não tem algoritmo que determina.
	- Chute
_Página 10_
- $\lceil \frac{n}{3}\rceil$ vira $\frac{n+2}{3}$ pois o máximo acontece quando somamos 2
	- Tem que fazer essas manipulações pra tirar o teto
	- O piso não precisa pois já é o mínimo
- $\lg \frac{n}{3} +1$ vira $\frac{\lg(2n)}{3}$ pois $1=\lg 2$ 
# Intuição
- O que muda é a base do $\log$ 
# Outro
- O quicksort é melhor que o Mergesort pois tem constantes menores e consome menos memória
	- Mas varia com a implementação