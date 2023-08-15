---
date: 2023-08-10
course: "MAC0338"
ordem: 3
annotation-target: slides/aula02_organized.pdf
---
**Matéria:** [[Análise de Algoritmos]]

Conjunto das notações:
- [[Notação O Grande]]
- [[Notação Omega]]
- [[Notação Theta]]

- Assintótica: não se importa com $n$ pequenos.
- Toda função é $O()$ dela mesma
	- Porém não é relevante, colocamos o que entendemos ou estamos acostumados
- Merge Sort roda em $\Theta(n\lg n)$
## Intuitivamente
#### Página 1

## Nomes de classes
#### Página 2

## Palavras de Cautela
#### Página 3

## Insertion Sort
#### Página 5.
- No vetor ordenado invertido o Insertion Sorte é $n^{2}$.
	- $O(n^{2})$
	- $\Omega(n^{2})$
	- $\Theta(n^{2})$
- É $O(n^{3})$? Sim mas não pode atingir.
- No melhor dos casos roda em $\Omega(\sqrt{ n })$
### Análise do caso médio
_Página 5_
- Temos $t-1$ maiores que $A(j)$
- Divide por $n!$ pois tudo é igualmente provável
- Estamos gerando o vetor de entrada
	- Antes de ordenar qualquer posição
- $k$ é escolhido ordenando o vetor e pegando de trás pra frente o $t$-ésimo elemento.
- Não tem repetição.
- $j$ e $t$ estão fixos

1. Escolhemos o conjunto $B$ quem vai entrar na parte vermelha
	1. $n$ escolhe $j$ possibilidades
	2. Ordena o conjunto $B$ 
2. Pega as últimas $t$ células e o cara imediatamente a esquerda $=k$
	1. Só existe 1 possibilidade
	2. foto lousa
	3. Coloca o $k$ em $j$
3. Aleatoriamente posiciona os demais elementos de $B$ em $S$
	1. O começo do vetor
	2. $(j-1)!$ possibilidades
4. Preenche o resto do vetor $A$ em qualquer ordem
	1. $(n-j)!$ possibilidades

_Página 13_
- Somatório de $t$ ponderado com a probabilidade de acontecer que encontramos: $\frac{1}{j}$
- Soma da PA
	- $\frac{(n+4)(n-1)}{4}$

_Página 14_
- No caso médio é ideal descrever que casa permutação tem probabilidade uniforme
- Qualquer função é $\Omega(1)$ pois trabalhamos com funções crescentes maiores que 0