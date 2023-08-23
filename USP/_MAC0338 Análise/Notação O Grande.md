---
date: 2023-08-10
course: "MAC0338"
ordem: 0
---
**Matéria:** [[Análise de Algoritmos]]

# Intuitivamente...
$O(f (n)) ≈$
- funções que não crescem mais rápido que $f (n)$
- funções menores ou iguais a um múltiplo de $f (n)$

Todas as funções abaixo crescem com a _mesma velocidade_:
- $n^{2}$
- $(3/2)n^{2}$
- $9999n^{2}$
- $n^{2} /1000$

- [ ] $n^{2}+99n$ é $O(n^{2})$
- [ ] $33n^{2}$ é $O(n^{2})$
- [ ] $9n+2$ é $O(n^{2})$
- [ ] $0,00001n^{3}-200n^{2}$ **não é** $O(n^{2})$

# Definição
Sejam $T (n$) e $f (n)$ funções dos inteiros nos reais.
Dizemos que $T (n)$ é $O(f (n))$ se existem constantes positivas $c$ e $n_{0}$ tais que:
$$
T (n) ≤ c f (n)\text{ , para todo } n\geq n_{0}
$$

![](https://i.imgur.com/IpUfItP.png)


## Mais informal
$T (n) é O(f (n))$ se existe $c > 0$ tal que
$$
T (n) ≤ c f (n)
$$
para todo $n$ suficientemente **GRANDE**.
# Ordenação por inserção
Voltando na [[Análise do Insertion Sort]], temos:
![](https://i.imgur.com/USrMUSl.png)

| linha     | consumo das execuções   |                                                    |
| --------- | ----------------------- | -------------------------------------------------- |
| 1         | $O(n)$                  |                                                    |
| 2         | $O(n)$                  | uma função anônima que pertence ao conjunto $O(n)$ |
| 3         | $O(n^{2})$              |                                                    |
| 4         | $O(n^{2})$              |                                                    |
| 5         | $O(n^{2})$              |                                                    |
| 6         | $O(n)$                  |                                                    |
| **total** | $O(3n^{2}+3n)=O(n^{2})$ |                                                    |


Ou seja, o algoritmo ORDENA-POR-INSERÇÃO consome
$O(n^{2})$ unidades de tempo.

Também escreve-se o algoritmo ORDENA-POR-INSERÇÃO consome
tempo $O(n^{2})$.

# Outro
- $O(1)$ é maior que qualquer $O(f(n))$ pois podemos multiplicar por qualquer constante.
- $O(n)$ pode ser um conjunto de funções pois quem é a função não importa.
	- $O(n)=\frac{7}{2}n+1$
	- $\frac{3}{2}n^{2}+\frac{7}{2}n+1=\frac{3}{2}n^{2}+O(n)$
- Agora apenas nos importamos com a ordem de crescimento de cada linha.
