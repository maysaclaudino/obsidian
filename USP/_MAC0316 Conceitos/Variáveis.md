---
date: 2023-08-23
course: "MAC0316"
ordem: 0
---

**Matéria:** [[Conceitos Fundamentais de Linguagens de Programação]]

---
# Escopo das variáveis
- Blocos de programas nos quais os valores das variáveis podem ser acessados
# Classificação quanto ao acesso a valores
- **Locais:** relacionado aos blocos de execução do programa nos quais elas estão inseridas
- **Globais:** vinculadas às células de memória antes da execução do programa e assim permanecem até qua a execução do programa se encerre.

# Existência das variáveis
- Uma variável existe no programa a partir do momento em que é _alocada_ no armazenamento
- Uma variável deixa de existir no programa quando é _desalocada_
- **Tempo-devida** da variável: intervalo de tempo entre a alocação e desalocação
# Classificação quanto à existência
- **Variáveis globais:** criadas por uma declaração global
	- Seu tempo de vida coincide com o tempo de execução do prorama
- **Variáveis locais:** criadas por uma declaração dentro de blocos de programas
	- Seu tempo de vida coincide com o tempo de execução do bloco do programa
- **Variáveis heap:** criadas e destruídas por comandos ou expressões do programa e acessadas via apontadores
	- Seu tempo de vida corresponde ao tempo entra a criação e destruição
		- Máximo: tempo de execução do programa
## C
- Variáveis locais e globais
```C
int v0;
void Q () {
	int q;
};

void P () {
	float p1, int p2;
	... Q;
	...
};

int main() {
	int v1; float v2;
	... P; ... Q; ...
};
```
# Tempo de vida das variáveis
![](https://i.imgur.com/J6hQnrz.png)
# Acesso às variáveis
![](https://i.imgur.com/yMrKOdH.png)
## Ada
- Variáveis locais e globais
- Ada não tem noção de variável global
```Ada
procedure main is
	v0: Integer;
	v1: Integer;
	v2: Float;
begin ... P; ... Q; ... end;
procedure P is
	p1: Float; p2: Integer;
	begin ... Q; ... end;
procedure Q is
	q: Integer;
	begin ... end;
```
# Variáveis na recursão
## C  
```C
int v0;
void P () {
	float p;
	... P; ...
};

int main () {
	int v1; float v2;
	... P; ...;
};
```
### Tempo de vida das variáveis
![](https://i.imgur.com/hkmaybR.png)
### Acesso às variáveis
![](https://i.imgur.com/my8dlLL.png)
## Ada
```Ada
procedure main is
	v0: Integer; v1: Integer;
	v2: Float;
	begin
		... P; ...
	end;
procedure P is
	p: Integer;
	begin
	... P; ...
	end;
```
### Tempo de vida das variáveis
![](https://i.imgur.com/CGPBNsB.png)

# Variáveis Heap
- Intermitentes
- Dependem de operações de alocação e desalocação
- Alocação de memória
	- C:  `malloc`
	- Ada e Java: `new`
- Desalocação de memória
	- C: `free`
	- Ada: `unchecked_deallocation`
# Variáveis compostas
- Tipos recursivos
- Lista C
```C
typedef struct NoIntlist* IntListC;
struct NoIntlist {
	int valor
	intListC *prox;
}

IntlistC prim, ult; ...
prim = malloc(sizeof *prim);
prim->valor = 10;
prim->prox = malloc(sizeof *prim);
ult = *prim.prox
ult->valor = 20;
ult->prox = NULL;
...
```
## Tempo de vida
- Ativação com a alocação
- Final da existência mediante desalocação explícita
![](https://i.imgur.com/2j6rypd.png)

- Célula desalocada, e os apontadores têm valores definidos
![](https://i.imgur.com/8rNImDU.png)

- Célula desalocada, e o apontador `ult` não aponta mais para células existentes (`NULL`)
![](https://i.imgur.com/incvygs.png)

- Novo nó inserido
![](https://i.imgur.com/aQbmsM0.png)

- Apontador "perdido"
![](https://i.imgur.com/UUU5Iwd.png)

- Célula sem acesso
![](https://i.imgur.com/BWgQo98.png)

- Célula sem acesso
![](https://i.imgur.com/BYGcay2.png)
# Problemas na existência de variáveis
- Desalocação pelo programador é um mecanismo "perigoso"
	- Acesso a células inexistentes
	- Células sem acesso
- C, Pascal, Ada... O programador é responsável pela desalocação
- Java: não há desalocação pelo programador
	- Mecanismo mais caro
	- Faz uma varredura nas variáveis heap e se não tiver sendo apontada por ninguém, libera (as vezes rearruma) a memória
		- Diminui o desempenho de execução
# Semântica de atribuição
- O que acontece quando uma variável composta é atribuída a uma outra variável do mesmo tipo?
$$
V_{1}=V_{2}
$$
# Duas semânticas diferentes
## Semântica de cópia
- Todos os valores dos componentes são copiados para os correspondentes da variável que recebe a atribuição
### C
![](https://i.imgur.com/GYQE1VC.png)

## Semântica de referência
- Um apontados (referência) é criado para o valor composto, sem a criação de espaço de memória para cada componente (apenas o espaço do apontador)
### Java
![](https://i.imgur.com/7BOdWbq.png)
## Nas linguagens de programação:
- C, Pascal e Ada usam a semântica de cópia
	- Em C os parâmetros são passados por cópia
		- Exceção: vetores são passados por referência
			- Na lógica dos desenvolvedores copiar o vetor consumiria muita execução e memória
- Java usa semântica de cópia para os tipos primitivos e semântica de referência para os objetos.
## Simulando as semânticas
- Em C a semântica de referência pode ser obtida através de apontadores
- Em Java a semântica de cópia pode ser obtida através de clones
# Noções de implementação
- Cada variável ocupa um espaço de memória durante seu tempo de vida
	- Alocada no início e desalocada no final
- O espaço depende do tipo da variável envolvida
- Se a [[Linguística de Programação|LP]] for [[tipada estaticamente]]:
	- Os tipos são declarados os tipos são declarados explicitamente ou o compilador poderá inferi-los
# Variáveis globais
- Uma variável está ativa no programa durante toda a sua execução
- Em tempo de compilação, um tamanho fixo de memória pode ser alocado para cada variável global
# Variáveis locais
- Uma variável local está ativa no programa durante o tempo de execução do bloco de programa no qual ela foi declarada
- Os escopos podem ser aninhados e as variáveis locais são alocadas em pilhas de execução de blocos
- **Quadros de ativação** são definidos para serem utilizados durante a execução dos programas dentro das pilhas de armazenamento
- Para cada função/ procedimento é reservado espaço suficiente em um quadro para que ela seja ativada
# Funções/procedimentos e os quadros de ativação
- Colocado na pilha de execução quando a função/procedimento é chamada
- Retirada da pilha de execução quando a função/procedimento é encerrada (`return`)
- As funções recursivas seguem esta mesma estratégia de alocação de quadros de ativação
- Sempre temos um apontador para o início e final de cada ativação
## Exemplo de alocação
**Ada:**
```Ada
procedure main is
	v1: Integer;
	v2: Float;
begin ... P; ... Q; ... end;
procedure P is
	p1: Float; p2: Integer;
	begin ... Q; ... end;
procedure Q is
	q: Integer;
	begin ... end;
```
![](https://i.imgur.com/TqAdAIL.png)
# Variáveis heap
- Não seguem um padrão predefinido
- Tempo de vida: alocação-desalocação
- Ocupam um espaço de memória chamado memória heap
	- Quando a variável é alocada, um espaço da memória heap é procurada/reservada
	- Quando a variável é desalocada, o espaço é liberado
# Memória heap
- **Gerenciador:** mantém a informação do que está ocupado e o que está livre
## Garbagge collection
- **Garbage collection:** desaloca todos os espaços inacessíveis pelo programa em um dado instante
	- Linguagens de programação que não possuem desalocação pelo programador
	- _Prós:_ elimina variáveis inacesíveis e não deixa destruir variáveis sendo apontadas
	- _Contra:_ muito caro - execução
### Algoritmo
- To collect garbage
	- For each variable $v$ in the heap:
		- Mark $v$ as unreachable
	- For each pointer $p$ in the stack:
		- Scan all variables that can be reached from $p$
	- For each variable $v$ in the heap:
		- If $v$ is marked as unreachable:
			- Deallocate $v$
- To scan all variables that can be reached from $p$:
	- Let variable $v$ be the referent os $p$
	- If $v$ is marled as unreachable:
		- Mark $v$ as reachable
		- For each pointer $q$ in $v$:
			- Scan all variables that can be reached from $q$
