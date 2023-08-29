---
date: 2023-08-29
course: "MAC0338"
ordem: 0
annotation-target: slides/aula03_resolucao-recorrencias.pdf
---
**Matéria:** [[Análise de Algoritmos]]

---
# Algoritmo da resolução
_Página 1_
[[Árvore de recorrência]] 
- Depois de um numero finito de expansões, chega na base
	- Senão está mal definida
**Exemplos:**
- Busca binária. $O(\lg n)$
	- Selection sort $O(n^{2})$ 
_Página 4_
- Prova por indução para conferir se a conclusão está correta.
	- Conclusão: $O(\lg n)$ 
# Prova por indução
- O certo é fazer indução em $\lg n$ porque só vale para $n$ potência de 2
- $\lg\left( \frac{n}{2} \right)=\lg n-1$
![](https://i.imgur.com/i5PqAId.jpg)
- Definimos a base $=1$ pois independente do valor o termo variante irá dominar
	- O valor 1 é mais simples
# Expansão
_Página 7_
- Não somar $(n-1)$ e $n$ para não complicar
	- Deixa explícito
- Expandimos até chegar no $T(1)$ 
- Progressão Aritmética de razão 1
	- Usa a fórmula da soma da PA
_Página 8_
- Note que não temos restrição no $n$ nesse caso
- Só faça a conta quando os termos que saem da recorrência são o mesmo
	- Como o $n$ na recorrência do Mergesort, e o 1 na anterior
# $T(n)=3T\left( \lfloor \frac{n}{2}\rfloor \right)+\Theta(n)$
_Página 9_
_Página 11_
- Soma da PG de razão $\frac{3}{2}$ 
_Página 13_
- O expoente $\lg n$ cresce mais devagar que $n$
- $3^{\lg n}$ vs $n^{2}$ 
	- $2^{\lg n}=n$
	- $4^{\lg n}=n^{2}$ 
	- Escrever o $3^{\lg n}$ na base $2$ 
		- $3^{\lg n}=(2^{\lg 3})^{\lg n}=(2^{\lg n})^{\lg 3}=n^{\lg 3}$ 
			- $3=2^{\lg 3}$ 
			- Pior que linear, melhor que $n^{2}$ 
				- $\lg {3}=1,57\dots$ 

![](https://i.imgur.com/oxfeXo2.jpg)
## Outro
- Como usamos $=$ em tudo podemos dizer que é $\Theta$
	- Se usássemos $\leq$ ou $\geq$ diria que é $O$ ou $\Omega$ 