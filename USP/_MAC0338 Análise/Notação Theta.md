---
date: 2023-08-10
course: "MAC0338"
ordem: 3
---
**Matéria:** [[Análise de Algoritmos]]

## Definição
Sejam $T (n)$ e $f (n)$ funções dos inteiros no reais.
Dizemos que $T (n)$ é $Θ(f (n))$ se:
- $T (n)$ é $O(f (n))$, e
- $T (n)$ é $Ω(f (n))$

![](https://i.imgur.com/eV4RitT.png)


Em outras palavras, dizemos que $T (n)$é $Θ(f (n))$ se existem constantes positivas $c_{1},c_{2}$ e $n_{0}$ tais que, para todo $n\geq n_{0}$.
$$
c_{1} f (n) ≤ T (n) ≤ c_{2} f (n)
$$

## Outro
- Usamos a notação $\Theta$ quando a função é ao mesmo tempo $O(f(n))$ e $\Omega(f(n))$
