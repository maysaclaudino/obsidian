---
date: 2023-08-25
course: "MAC0316"
ordem: 0
---

**Matéria:** [[Conceitos Fundamentais de Linguagens de Programação]]

---
- Nos projetos das LPs devemos determinar
	- **Entidades vinculáveis**
	- **Forma de vinculação:** mostra como os atributos são associados às entidades nas linguagens (construtores)
	- **Tempo de vinculação** de cada entidade vinculável na linguagem 
# Contexto de programas
- Cada programa em execução contém um conjunto de vinculações necessárias à sua execução:
	- Valores
	- Tipos
	- Variáveis
	- Abstrações...
# Exemplo de vinculações em C
```C
#define a 0
int int v0;
	void Q () {
		int q;
		...
	}; // AAA
	void P () {
		float p1;
		int p2 = 3;
		... Q; ...
	}; // BBB
	int main() {
		int v1; float v2;
		... P; ...Q; ... // CCC
	};
```

**AAA***
- $a\to$ const, int, 0
- $v_{0}\to$ var, int
- $Q\to$ func, sem params
- $q\to$ var, int

**BBB**
- $a\to$ const, int, 0
- $v_{0}\to$ var, int
- $Q\to$ func, sem params
- $P\to$ func, sem params
- $p_{1}\to$ var, float
- $p_{2}\to$ var, int, 3

**CCC**
- $a\to$ const, int, 0
- $v_{0}\to$ var, int
- ???
# Formas de vinculação
- Declarações/ definições implícitas
- Declarações/ definições explícitas
## Declarações implícitas
- Atributos são inferidos pelo processador sem que tenham sido declarados explicitamente
	- `#define a 0`
		- Tipo `int` inferido através do valor, sem que haja uma declaração explícita do tipo
	- Em Fortran, variáveis podem aparecer no corpo do programa _sem declaração_ (`I-N` tipo `INTEGER`, outros tipo `REAL`)
## Declaração de constantes
- Associa um valor a um identificados
- Alguns outros atributos são associados, tal como o tipo, espaço de memória...
- Em algumas LPs os valores associados precisam ser literais ou expressões resolvíveis em tempo de compilação
### C
```C
#define a 65
```
- Declara que `a` é uma constante de forma explícita e infere (implícito) o tipo `int`
### Ada
```Ada
a: constant Integer := 65;
```
- Declara que `a` é uma constante de forma explícita
### SML
```SML
val a : int = 65;
```
- Declara que `a` é uma constante de forma explícita
```SML
fun somalago (i:int) =
	let val algo = if i < 0
		then -5
		else 5
	in
		algo + i
	end
```
## Declaração de variáveis
- Vincula um identificador a uma variável
- Alguns outros atributos são associados, tal como o tipo, espaço de memória, valor...
- As variáveis podem ser simples, compostas
## Renomeação de variáveis
**Ada**
```Ada
type Cores is (vermelho, azul);
	v : array (Cores) of Natural;
	declare
		c : Cores := azul;
		p : Integer renames v(c);
	begin
		...
		p := p + 1;
		---
	end;
```
# Declaração de tipos
## Pascal  
```pascal
type MesesP = (jan, fev, mar, abr, mai, jun, jul, ago, set, out, nov, dez);

type DiasP = 1..31

type DataP = record
	m : MesesP
	d : DiasP
	end;
```
## C  
```C
typedef int inteiro;
typedef float decimal;

typedef struct estrut1 MinhaEstrutura;
struct estrut1 {
	int var1;
	float var2;
};
struct estrut2 {
	int var3;
	MinhaEstrutura var4;
}
```
## SML
```SML
datatype traffic_light = red
					   | green
					   | amber

datatype inttree =
	empty
	| node of int * inttree * inttree
```
- `node` $\to$ construtor
# Definição de abstrações
- Vincula um identificador a uma abstração
- Além disso, os parâmetros e seus tipos também devem ser vinculados
- O identificador que em geral precisa de mais atributos vinculados
- A maioria das LPs possui abstração de processos. As linguagens de programação orientadas a objetos possuem abstrações de dados
## Definição de abstração de processos
### C
```C
void Q (int a, float, b) {
	int q;
	...
}
```
- Quais elementos são vinculados quando definimos $Q$?
### Ada
```Ada
function quadrado1 (n: Integer)
	returb Boolean is
	begin
		return n * n;
	end
procedure quadrado2 (n: in out Integer) is
	begin
		n := n * 2;
	end;
```
- Quais elementos são vinculados?
### SML
```SML
val even = fn (n:int) => (n mod 2 = 0)
```
- Identificador vinculado à variável `even`

```SML
fun even (n:int) = (n mod 2 = 0)
```
- Identificador vinculado à abstração `even`
# Tempo de vinculação
- Determina a visibilidade dos identificadores em tempo de execução
- Depende:
	- Escopo da declaração dos identificadores
		- Construtores de blocos da linguagem
	- Modo de vinculação tipos:
		- Estático
		- Dinâmico
	- Modo de vinculação do escopo
		- Estático
		- Dinâmico
# Construtores de blocos
- Determinam o escopo das declarações
- Exemplos
	- **C:** `{...}`, funções...
	- **Java:** blocos de comandos, métodos, classes, pacotes...
	- **Ada:** `declare ... begin ... end;`, procedimentos, funções, pacotes...
# Estrutura
## Monolítica
- Declara $x$
- Declara $y$
- Declara $z$
## Blocos lineares
- Declara $x$
	- Declara $y$
	- Declara $z$
## Blocos aninhados
- Declara $x$
	- Declara $y$
		- Declara $z$
		- Declara $x$
# Modo de vinculação de tipos
## Estático
- Identificadores têm seus tipos definidos em tempo de compilação
## Dinâmico
- Os valores possuem um tipo fixo, mas as variáveis ou parâmetros das funções não possuem um tipo predeterminado
- As variáveis podem assumir valores de tipos diferentes em diferentes estágios da computação do programa
- Maior flexibilidade
	- Os programas podem ser "genéricos" porque os tipos são vinculados às variáveis mediante os dados
- Custo elevado na execução
- Exemplos: Lisp, SML, Haskell, Smalltalk, Java (objetos genéricos)
# Modo de vinculação de escopo
- Declaração de um bloco de programa
	- Vinculação de um identificador a um bloco de execução do programa
- Aplicação de um bloco de programa
	- Bloco de execução que será efetivamente utilizado no momento de uso do identificador
## Vinculação estática de escopo
- Na grande maioria das linguagens de programação
- Um identificador é sempre vinculado única e exclusivamente a um bloco de execução - em tempo de compilação
- Raras linguagens:
	- Smalltalk, Lisp
- Um identificador é vinculado a um bloco de execução obedecendo a hierarquia de blocos e ordem de execução (a última vinculação)
### Exemplo: escopo estático
```
program main;
	var x : integer;
	procedure sub1;
		var x: integer;
		begin
			...x...;            // definido em sub1
		end; {sub1}
	procedure sub2;
		begin
			sub1;
			...x...;            // definido no main
		end; {sub2}
	begin {main}
		...
	end; {main}
```

### Exemplo: escopo dinâmico
```
program main;
	var x : integer;
	procedure sub1;
		var x: integer;
		begin
			...x...;            // definido em sub1
		end; {sub1}
	procedure sub2;
		begin
			sub1;
			...x...;            // definido no sub1
		end; {sub2}
	begin {main}
		...
	end; {main}
```