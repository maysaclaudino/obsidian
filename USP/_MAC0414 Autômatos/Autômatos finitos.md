---
date: 2023-08-08
course: "MAC0414"
ordem: 0
---
**Matéria:** [[Autômatos, Computabilidade e Complexidade]]

As perguntas de MAC0414 serão do tipo:
- Dado um número inteiro $n$, decidir se $n$ é primo.
- Dado uma string $w$ sobre $\{ 0,1 \}$ decidir se $w$ está em $L$.
	- Onde $L$ é o conjunto de números primos.
## Strings
- _Strings_ são sequências de símbolos de um alfabeto.
	- **Alfabeto** é um conjunto não vazio de símbolos. É representado por letra grega maiúscula.
- $w=w_{1}w_{2}w_{3}\dots w_{n}$ onde $n$ é o _comprimento_ da string.
- São fornecidas através de uma fita dividida em posições.
- Cada posição tem um _símbolo_.
- São representadas por letras minúsculas.
- São finitas

## Máquina de estados
- Uma máquina de estados finitos.
- O coração da máquina é o controle finito que a cada momento está em um estado.
- Em intervalos de tempo regulares:
	1. A _**cabeça de leitura**_ lê o símbolo sob ela na fita, fornece símbolo lido ao controle e se desloca para a posição da direita;
	2. O _**controle**_ vai para um estado que só depende do estado atual e do símbolo lido
- **1.** e **2.** se repetem até que não haja mais símbolos a serem lidos.
- A máquina **aceita** ou **rejeita** a string e para.
![](https://i.imgur.com/rtUpC2F.png)


## "Órgãos" de um autômato $M_{1}$
![](https://i.imgur.com/NngXnkm.png)

- **Estados:** $q_{1}, q_{2}$ e $q_{3}$
- **Transições:** $\xrightarrow{ 1 }$
- **Estado inicial:** ![](https://i.imgur.com/fYO5ZhI.png)
- **Estado de aceitação:** ![](https://i.imgur.com/ZW3v9AO.png)
## Autômato e computação
- **Entrada:** uma string
- **Saída:** aceita ou rejeitada
### Computação
- Começa no estado inicial
- lê um símbolo da string;
- segue a transição correspondente;
- _aceita_ se o estado final é de aceitação e _rejeita_ em caso contrário

No autômato $M_{1}$ acima a string $01101$ é **aceita** e $11000$ é **rejeitada**.

## Componentes
Um **ADF** $M$ consiste de 5 componentes $(Q, \Sigma, \delta, s, F)$ em que:
- $Q$ é um conjunto finito de _estados_
- $\Sigma$ é o _alfabeto_ dos símbolos da entrada ^e4c346
- $\delta:Q\times \Sigma \to Q$ é a _função de transição_
- $s \in Q$ é o estado inicial
- $F\subseteq Q$ é o conjunto de _estados de aceitação_
	- Pode ter mais de um
### Exemplo
![NngXnkm.png](https://i.imgur.com/NngXnkm.png)
Aqui temos $M_{1}=(Q,\Sigma,\delta,q_{1},F)$ em que:
- $Q=\{ q_{1},q_{2},q_{3} \}$
- $\Sigma=\{ 0,1 \}$
- $\delta$ é representada pela tabela:

|       | 0       | 1       |
| ------- | ------- | ------- |
| $q_{1}$ | $q_{1}$ | $q_{2}$ |
| $q_{2}$ | $q_{3}$ | $q_{2}$ |
| $q_{3}$ | $q_{2}$ | $q_{2}$        |

- $q_{1}$ é o _estado inicial_
- $F=\{ q_{2} \}$ é o conjunto de _estados de aceitação_

![](https://i.imgur.com/NngXnkm.png)
## Representação de autômatos
- Um autômato finito determinístico (AFD) é comumente representado ou por uma tabela de transição.
- Essa tabela se assemelha à função de transição.
- **Linhas** correspondem a estados e **colunas** a símbolos de $\Sigma$
- O **estado inicial** é marcado com $\to$ e os **estados de aceitação** com $*$.
![](https://i.imgur.com/rgQGngk.png)
## Linguagem de um autômato
Seja $M_{1}$ um autômato e $w$ uma string se: 
$$
A=\{ w:M_{1}\text{ aceita }w \}
$$
Então dizemos que $A$ é a _linguagem de_ $M$ ou que $M_{1}$ _reconhece_ $A$
- Em símbolos escrevemos $A=L(M_{1})$
- $L(M_{1})$ é a linguagem reconhecida por $M$.
- Não precisa ser finita.
- É um conjunto representado por letras maiúsculas.
## Exemplo
![](https://i.imgur.com/NngXnkm.png)
Aqui $M_{1}$ aceita $01101$ e rejeita $11000$.

Olhando mais cuidadosamente $M_{1}$ aceita, exatamente, as strings em
$$
A=\{ w:w\text{ termina com o símbolo 1 ou com um número par de 0's} \}
$$

## Outro
- Compiladores são maneiras compactas de decidir se uma string (programa) está nalinguagem de programas válidos.

---
>[!example] Próximo:
> [[Linguagem regular]]
