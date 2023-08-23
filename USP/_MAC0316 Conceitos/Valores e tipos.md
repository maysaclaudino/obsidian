---
date: 2023-08-16
course: "MAC0316"
ordem: 0
---

**Matéria:** [[Conceitos Fundamentais de Linguagens de Programação]]

---
## Valores e tipos
- Tipos de valores
- Tipos fundamentais
	- primitvos
	- compostos
	- recursivos
## Definições
- **Valores:** representações simbólicas de conceitos
	- Ideia semântica por trás
	- São elementos que podem ser avaliados, armazenados, atualizados e transmitidos durante a execução de um programa.
- **Tipo:** classes de valores
	- Organização de valores
	- São conjuntos de calores semanticamente relacionados.
- **[[Variáveis]]:** um programa geralmente é composto por mais de uma expressão. As variáveis servem como repositório para passagem de valores de uma expressão a outra do programa.
## O porquê dos tipos
- E se não tivéssemos os tipos?
	- As operações precisariam ser definidas para valores particulares
- E com os tipos?
	- Podemos definir regras unificadas para as operações sobre tipos. Desta forma, grupos de valores são tratados, em vez de tratar valores particulares

- Queremos definir um conjunto de operações que queremos fazer
- Exemplo: Números reais
	- Conjunto: $\{ 1.0,2.0,3.0,\dots \}$
	- Operação de soma definida
		- $1.0+_{\mathbb{R}}2.0$
		- $2.0+_{\mathbb{R}}3.5$

## Todo conjunto de valores é um tipo?
- Um tipo é um conjunto de valores
	- E um conjunto de operações sobre esses valores
	- $v$ é um valor do tipo $T$ se $v\in T$

- Essas definições vêm da noção matemática que temos
- Conseguimos mapear coisas bem diferentes para elementos simples
- Exemplo: linguagem C
	- Soma de dois inteiros resulta em inteiro
	- Soma de inteiro e real resulta em real
	- Sempre rebate o tipo de inteiro menor para o maior
	- Tem linguagens que não permite essa mistura
		- Fortemente tipificadas

- $E$ é uma expressão do tipo $T$ se $E$ é sempre avaliada com um valor do tipo $T$
- Quais conjuntos são tipos? Tratamento uniforme de valores
	- $\{ \text{false, true} \}$ é um tipo: `not, and, or` são operações aplicadas de maneira uniforme sobre esses valores.
	- $\{ \dots,-2,-1,0,+1,+2,\dots \}$ é um tipo: $+,-,*,/$ são aplicadas sobre todos os valores uniformemente
	- $\{ 20,\text{true},\text{Tuesday} \}$ não é um tipo

- A rigor um número real não tem o mesmo significado que um número inteiro
- Elementos com semântica parecida

## Definições perdi esse slide
Algo sobre cardinalidade

## Uso de valores na programação
- Modelar soluções de problemas científicos
- Os valores básicos que usamos em programação são inspirados em valores matemáticos que conhecemos
- Novos valores/tipos são incorporados à medida que ampliamos os domínios de aplicação

## Tipos em Linguagens de Programação
- akgo

### Tipos primitivos
- **Valor primitivo:** atômico, não 
	- Exemplo: caracteres, números reais, números inteiros
		- Números reais são acessados como números inteiros
#### Tipos primitivos definidos

#### Cardinalidade de tipos predefinidos
- \#Boolean = 2
	- Precisamos de apenas 1 bit
- \#Character = 128 (ASCII), 256 (ISO-L)

- A representação interna depende da cardinalidade que estamos trabalhando

#### Tipos primitivos construídos
- Novos tipos construídos
	- **C:** `enum MesesC {jan, fev, mar, abr, mai, jun, jul, ago, set, out, nov, dez}`
	- Enumeração de novos valores
	- **Pascal:** `type`
- Quero definir um novo conjunto de valores para tratar como um tipo
- Existe uma relação de ordem entre os elementos ( `dez < nov` )
- A linguagem Ada também permite isso

- Poderíamos construir nossos próprios tipos na linguagem, mas daria trabalho
- Algumas linguagens permitem que criemos novos tipos
- Às vezes é main intuitivo dar soluções com tipos que criamos
- Orientação à objetos: em teoria, as classes que definimos são tipos abstratos

- A partir de tipos existentes
- Novo conjunto de valores a partir de um intervalo

##### Operações sobre tipos construídos
- Em C conseguimos somar `jan` com `fev`
	- Faz uma representação de inteiros
$$
\begin{align}
x\gets jan \\
y\gets fev \\
z\gets x+y
\end{align}
$$
- $z\gets x+3$ faz mais sentido, apesar de continuar errado
- Não tem significado intuitivo

### Tipos compostos
- **Valor composto:** não-atômico, pode ser desmembrado em valores mais simples
	- Tipos que conseguimos ter acesso a partes diferentes dos valores
- **Tipo composto:** conjunto formado por valores compostos

- Um programa bom é aquele escrito de forma clara intuitivamente a solução do problema

#### Principais tipos compostos
- Produto cartesiano
- União disjunta
- Mapeamentos
- Conjunto Potência
- algo

##### Produto cartesiano
- O produto cartesiano do conjunto $S$ pelo conjunto $T$ é definido por:
	- $C=S\times T=\{ (x,y)|\x \in S; y\in T \}$
	- $(x,y)$ é uma tupla do produto
	- Pode ser generalizado para vários conjuntos
- Cardinalidade
	- $\#C=\#S \cdot \#T$


- A tupla é um valor
	- Do ponto de vista de programação, conseguimos ter acesso a cada um dos valores da tupla
	- Tratamos de forma desmembrada, primeiro valor da tupla e segundo valor da tupla
**Exemplo:**
- $A=\{ \text{jan,} \}$

**Exemplo em C:**

```
enum MesesC {jan, fev, mar, abr, mai, jun, jul, ago, set, out, nov, dez}

enum 
```

- `DataC` é definido a partir da combinação de `MesesC` e `DiasC` 

**Exemplo Pascal:**
- Astuplas sao dadas por essa orde `DataP`

**Exemplo Ada:**

```
type MesesA
```

## União Disjunta
### União disjunta discriminada
prim e seg é um identificador do tipo

- Todos os elementos do conj com essa identificação
**Exemplo Pascal:**

- Se for exato é inteiro, se é aproximado é real

**Exemplo Ada:**
### União disjunta livre
- União de todos os elementos de $S$ e todos os elementos de $T$
**Exemplo C:**
- Temos o conjunto de todos os inteiros e todos os reais
- Assume ou o valor de um inteiro ou o valor de um real
	- Não assume os dois ao mesmo tempo
	- Acomoda espaço para um número real, porque toma mais espaço
**Exemplo Ada:**

#### Mapeamento
- O mapeamento do conjunto $S$ para o conjunto $T$ é definido por:
	- $m:S\to T=\{ m|x \in S \implies m(x) \in T \}$
- Cardinalidade
	- $\#(s\to T)=(\#T)^{\#S}$ 
**Exemplos:**
- $A=\{ \text{jan, fev, mar} \}$ 
**C, Pascal e Ada:**

#### Conjunto Potência
- $\mathcal{P}(A)$ 
**Exemplo Pascal:**
