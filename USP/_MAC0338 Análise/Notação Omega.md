---
date: 2023-08-10
course: "MAC0338"
ordem: 2
---
**Matéria:** [[Análise de Algoritmos]]

Dizemos que $T (n)$ é $Ω(f (n))$ se existem constantes positivas $c$ e $n_{0}$ tais que, para todo $n\geq n_{0}$:
$$
c f (n) ≤ T (n)
$$

![](https://i.imgur.com/oGQJ4KE.png)

### Mais informal
$T (n) = Ω(f (n))$ se existe $c > 0$ tal que
$$
c f (n) ≤ T (n)
$$
para todo $n$ suficientemente GRANDE.
## Exemplos
### Exemplo 1
Se $T (n) ≥ 0.001n^{2}$ para todo $n ≥ 8$, então $T (n)$ é $Ω(n^{2})$.
_Prova:_ Aplique a definição com $c = 0.001$ e $n_{0}=8$.

### Exemplo 2
O consumo de tempo do ORDENA-POR-INSERÇÃO é $O(n^{2})$ e $Ω(n)$.
![](https://i.imgur.com/USrMUSl.png)

| linha     | mínimo de execuções |
| --------- | ------------------- |
| 1         | $=n$                |
| 2-3       | $=n-1$              |
| 4         | $\geq n-1$          |
| 5-6       | $\geq 0$            |
| 7         | $=n-1$              |
| **total** | $\geq 4n-3=\Omega(n)$                    |

## Outro
- Usamos a notação $\Omega$ para limitantes inferiores
- $n$ é sempre inteiro
- Insertion sort é $O(n)$ quando o vetor está ordenado