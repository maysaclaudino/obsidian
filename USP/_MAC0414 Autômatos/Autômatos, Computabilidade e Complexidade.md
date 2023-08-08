# Aulas

```dataview
TABLE
	date AS Data
WHERE course = "MAC0414" AND file.name != "aula-autômatos"
SORT date ASC
```


# Informações da matéria

**Sigla:** MAC0414
**Moodle:** [Aqui](https://edisciplinas.usp.br/course/view.php?id=111879)

## Datas

### Provas
- [!] **P1:** 14/09
- [!] **P2:** 19/11
- [!] **P3:** 07/12

### EP's
- [*] **EP1:** 
- [*] **EP2:** 
- [*] **EP3:** 

## Monitorias

- Carlos: 
- Henri: 
- João: 

_Horário da monitoria_: 

## Critério de avaliação

### Média de Exercícios (ME)
A média _ME_ desses exercícios será a aritmética: soma das notas obtidas dividido pelo número de exercícios dados.

### Média de Aquecimentos (MA)
Nos passeios teremos atividades de **aquecimento**. Esses aquecimentos deverão ser feitos em cerca de 10 minutos, tipicamente antes de começarmos o passeio do dia. 

A média _MA_ das atividades de aquecimento será a aritmética: soma das notas obtidas dividida pelo número de atividades dadas.

### Média de Provas
Teremos três provas ao longo da jornada. A média _MP_ das provas será

$MP = max(\frac{(P1 + P2 + P3)}{3}, \frac{(MA + P2 + P3)}{3}, \frac{(P1 + MA + P3)}{3}, \frac{(P1 + P2 + MA)}{3})$

### Nota Final (NF)
A nota final _NF_, será calculada pela regra 

- se $MP \ge 5$ e $ME \ge 5$, então $NF = 0.7 x MP + 0.3 x ME$
- senão $NF = min(MP, MEP)$

Aqueles e aquelas com _NF_ maior ou igual a 5 estarão **aprovados**.


## Bibliografia

1. _Introdução à Teoria da Computação_ (Michael Sipser)
2. _Elementos de Teoria da Computação_ (H.R. Lewis e C.H.Papadimitriou)
3. _Introdução à Teoria de Autômatos, Linguagens e Computação_ (J.E. Hopcroft, R. Motwani e J.D. Ullman) 
4. _Computers and Intractabily: A Guide to the Theory of NP-Completeness_ (Michael R. Garey e David S. Johnson)
5. _Introduction to Algorithms_ (Thomas H. Cormen, Charles Eric Leiserson, Ronald Linn Rivest e Clifford Stein)
6. _Slides [CS103 Mathematical Foundations of Computing](https://web.stanford.edu/class/archive/cs/cs103/cs103.1156/)_ (Keith Schwarz)