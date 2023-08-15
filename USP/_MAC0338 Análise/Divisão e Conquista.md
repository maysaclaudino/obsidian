---
date: 2023-08-15
course: "MAC0338"
ordem: 0
annotation-target: slides/aula03_div_conq.pdf
---

**Matéria:** [[Análise de Algoritmos]]

---
## Definição
_Página 1_
- Instância: entrada
	- Vetor por exemplo
## Mergesort
_Página 2_
- $p$ e $r$ são índices do vetor $A$
- Se $p=r$ a instância já está ordenada (1 elemento só)
- **Divisão:** linha 2
- **Conquista:** linhas 3-4
### Intercalação
_Página 3_
_Página 6_
- Copia a parte azul de $A$ em $B$ ao contrário
_Página 7_
- O vetor $B$ é crescente de fora para dentro
- Se o $j$ chega em $q$, o $i$ sempre será menor. O vermelho sempre "ganha".
#### Consumo de tempo do intercala
_Página 21_
_Página 22_
- Linhas 1-2 aprox. $\frac{n}{2}$
### Consumo de tempo do Mergesort
_Página 25_
- Linha 3: Chamei recursivamente num vetor de $\frac{n}{2}$ teto
- Linha 3: Chamei recursivamente num vetor de $\frac{n}{2}$ piso
- $T(n)$ tempo de consumo do Mergesort
	- Essa função está sendo definida recursivamente, para descobrir $T(n)$ temos que primeiro calcular $T\left( \frac{n}{2} \right)$.
_Página 26_
- Como descobrir ordem de funções definidas por recorrência?
	- Recorrência: um termo definido por ele mesmo
_Página 28_
- Queremos nos livrar da notação assintótica
_Página 30_
- Definimos $T(1)=1$
- [[Árvore de recorrência]]
#### Expansão
_Página 32_
_Página 36_
- Renomeou $n$ para $m$ por que sim, para não confundir
	- $n$ não significa nada
_Página 38_
- $m=\frac{n}{2}$ pq queremos calcular a instância menor de $T(n)$
_Página 42_
- Chute: $2^{k}T\left( \frac{n}{2^{2}}+kn \right)$
	- Agora precisa provar por indução
- $k=\lg n$ foi escolhido conforme onde eu quero chegar para transformar em $T(1)$.
##### Conferência
_Página 49_
- Provar o chute por indução em $k$
_Página 52_
- Base está certa
_Página 54_
- Provamos para $n$'s em potência de 2