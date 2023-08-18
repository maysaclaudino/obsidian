---
date: 2023-08-11
course: "MAC0414"
ordem: 0
annotation-target: slides/aula01_organized.pdf
---
**Matéria:** [[Autômatos, Computabilidade e Complexidade]]

## Definição
_Página 1_
![](https://i.imgur.com/TJLPQp0.png)
Uma linguagem é **regular** se existe algum [[Autômatos finitos Determinísticos|autômato finito determinístico]] que a reconhece. Por exemplo:
$$
A=L(M_{2})=\{ w:w\text{ contém a subtring 11} \}
$$
Logo $A$ é regular.
- $B=\{ w:w\text{ tem um número par de 1's} \}$ **também é regular**
- $C=\{ w:w\text{ tem o mesmo número de 0's e de 1's} \}$ _não é regular_

- Definimos conjuntos infinitos em um sistema compacto.

> pág 5
> $L(M_{1})\cap L(M_{2})$



## União de LR
_Página 9_
### Exemplos
_Página 14_

## Interseção de LR
_Página 21_
- Supomos que os alfabetos são iguais
	- Se um símbolo está em um alfabeto e não em outro, rejeita
	- Estado da morte para esse caso (o outro)
- Somente $(q_{0},r_{0})$ é aceito.

## Concatenação de LR
_Página 24_
- A questão é: definir onde acaba $x$ e começa $y$ em $w$
	- $w=x+y$ 
- A cada estado de aceite de $A_{1}$ checamos se $A_{2}$ aceita
	- Se 1 $A_{2}$ aceitar, então aceita $A_{1}\circ A_{2}$ 
	- Alguma hora "padroniza" então basta 1 caso de $A_{2}$ aceitar, todos aceitam
### Exemplos
_Página 28_

## Conjunto das partes
_Página 41_

## Outro
- A quantidade de estados e possibilidades é finita
	- $Q$ é finito.