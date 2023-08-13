---
date: 2023-08-11
course: "MAC0316"
---

**Matéria:** [[Conceitos Fundamentais de Linguagens de Programação]]

---
## Introdução
- Linguística de Programação
	- Conceitos e paradigmas
	- Sintaxel, semântica e paradigmas
	- Processadores de linguagens
- Histórico do desenvolvimento de paradigmas

## Linguística de Programação
- Estudo das Linguagens de Programação (LPs)
- Análogo a linguística das linguagens naturais: sintaxe e semântica
- Linguagens naturais são muito mais expressivas e os linguistas se concentram em seus estudos
- Cientistas de computação precisam projetar, especificar e implementar novas linguagens de programação

- Linguística de programação é mais restrita que a natural

## Para que usamos LPs?
- Solucionar problemas que não "queremos" resolver manualmente
- Programa:
	- Documento (descrição)
		- Detalhamento de solução do problema (computacional) que temos
	- Máquina Abstrata
		- Descreve os passos computacionais da solução

## O que é uma LP?
- Determina os recursos disponíveis e sua forma de utilização para construir máquinas abstratas específicas (para ser simulada por um computador)

## Visões distintas das LPs
- Usuário
- Projetista
	- O quão fácil ou difícil é do ponto de vista dos processadores

## Como projetar uma LP?
- Quais os problemas a resolver? Requisitos
- Como representar, de forma natural, os requisitos desejados? Expressividade.
	- Adaptar o domínio do que temos para o usuário final
- Como solucionar os problemas de forma adequada? Paradigma.
- Os requisitos são implementáveis? Implementação
- Dá para implementar de forma eficiente? Eficiência.

## Propriedade importante das LPs: universalidade
- Uma LP deve ser universal: expressar qualquer computação
	- Não universal: linguagens sem iteração ou recursão
	- Universais: funções recursivas ou iteração + recursão
		- Turing completas, implementam a teoria da máquina de Turing
		- Precisa dos comandos de atribuição, if else e loop
			- Os demais comandos são definidos em cima disso

## Características desejáveis das LPs
- Legibilidade
	- Simplicidade
	- Ortogonalidade
		- Os comandos também funcionam combinados
	- Instruções significativas (clareza)
	- Facilidade para representar tipos e estruturas
- Facilidade de escrita
- Confiabilidade
- Custo
	- De desenvolvimento da linguagem
	- De execução

- Repertório mais enxuto que compreenda as necessidades da linguagem

## Fatores de influência no projeto
- Arquitetura de máquinas
- Metodologias de desenvolvimento

## Conceitos das LPs
- Elementos para a construção das LPs e programas
	- Valores e tipos
	- Variáveis
	- Vinculação e escopo
	- Abstração de processos
	- Abstração de dados
	- Concorrência
		- Distribuir as tarefas nos processadores
		- Paralelizar na compilação
			- Mas é menos eficiente que o programador paralelizar

- Vincular um valor a uma variável, uma definição a uma função
## Paradigmas de programação
- Paradigma é um estilo de programação relacionado a conceitos fundamentais
- Vinculado a forma de organizar
- **Imperativo:** variáveis, comandos, procedimentos
	- O programador define explicitamente os valores dos elementos
	- É eficiente para a arquitetura de computadores que temos atualmente
	- C
- **Orientado por objetos (OO):** objetos, métodos, classes
	- Java, C++
- **Concorrente:** processos, comunicação
- **Funcional:** valores, expressões, funções
	- Olha o mapeamento do domínio e contra-domínio
	- Haskell
- **Lógico:** asserções, relações
	- Prolog

## O que é necessário para construir uma LP?
- Sintaxe
- Semântica
	- Operacional
		- Ordem de operações e funções
	- Denotacional
		- Como avaliar computacionalmente os elementos
		- Próximo da intepretação de processadores
	- Axiomática
		- Semântica da [Lógica de Hoare](https://pt.wikipedia.org/wiki/L%C3%B3gica_de_Hoare) (que vimos em MAC0239 - Lógica)
- Processadores
	- Interpretadores
	- Compiladores
	- Editores
	- Debuggers

- [BNF](https://pt.wikipedia.org/wiki/Formalismo_de_Backus-Naur): forma de descrever a sintaxe da linguagem