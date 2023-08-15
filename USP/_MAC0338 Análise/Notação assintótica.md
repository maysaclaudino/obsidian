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
- Temos $t-1$ maiores que $A(j)$
- Divide por $n!$ pois tudo é igualmente provável
- Estamos gerando o vetor de entrada
- $k$ é escolhido ordenando o vetor e pegando de trás pra frente o $t$-ésimo elemento.
- Não tem repetição.