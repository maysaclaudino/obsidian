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
- Uma variável
# Classificação quanto à existência
- **Variáveis globais:** criadas por uma declaração
- **Variáveis locais:**
- **Variáveis heap:**
## C
- Variáveis locais e globais
```C
int v0;
void Q()

```
# Tempo de vida das variáveis
# Acesso às variáveis
## Ada
- Variáveis locais e globais
- Ada não tem noção de variável global
# Variáveis na recursão: C
# Variáveis Heap
- Intermitentes
- Dependem de operações de alocação e dasalocação
- Alocação de memória
	- `malloc` C
# Problemas na existência de variáveis
- Desalocação pelo programador é um mecanismo "perigoso"
	- Acesso a células inexistentes
	- Células sem acesso
- C, Pascal, Ada... O programador é responsável pela desalocação
- Java: não há 
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
## Semântica de referência
- Um apontados (referência) é criado para o valor composto, sem a criação de espaço de memória para cada componente (apenas o espaço do apontador)
## Exemplo: funções em C
- Os parâmetros são passados por cópia
	- Exceção: vetores são passados por referência
		- Na lógica dos desenvolvedores copiar o vetor consumiria muita execução e memória
## Simulando as semânticas
- Em C
# Noções de implementação
- Cada variável ocupa um espaço de memória durante seu tempo-de-vida
	- Alocada no início e desalocada no final
- O espaço depende do tipo da variável envolvida
- Se a [[Linguística de Programação|LP]] for [[tipada estaticamente]]:
	- Os tipos são declarados
# Variáveis globais
- Uma variável está ativa no programa duarnte toda a sua execução
- Em tempo de compilação, um tamanho
# Variáveis locais
- Uma variável local está ativa 
- Qaudros de ativação são definidos para semrem utilizados durante a execução dos programas dentro das pilhas de armazenamento
- Para cada função/ procedimento é reservado 
# Funções/ procedimentos e os quadros de ativação
- Colocado na pilha de execução quando a função/ procedimento é chamada
- Retirada
- Sempre temos um apontador para o início e final de cada ativação
# Variáveis heap
- Não seguem um padrão predefinido
