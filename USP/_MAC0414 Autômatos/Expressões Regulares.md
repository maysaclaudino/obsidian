---
date: 2023-08-22
course: "MAC0414"
ordem: 0
annotation-target: slides/
---

**Matéria:** [[Autômatos, Computabilidade e Complexidade]]

---
- Expressões regulares são strings que representam linguagens
- Ideia: construção de [[Linguagem regular]] "bottom-up"
	- Começamos com linguagens simples
	- Usamos **operações regulares** para construir linguagens mais complexas
- Uma expressão regular sobre $\Sigma$ é 
	-  $a$ para todo $a \in \Sigma$
	-  $\epsilon$
	-  $\emptyset$
	-  $(R_{1}\cup R_{2})$ se $R_{1}$ e $R_{2}$ são expressões regulares
	-  $(R_{1}\circ R_{2})$ se $R_{1}$ e $R_{2}$ são expressões regulares
	-  $(R_{1}*)$ se $R_{1}$ é expressão regular
- Se $R$ é uma ER então as linguagens de $R$ é detonada por $L(R)$
	-  $a$ representa a linguagem $\{ a \}$
	-  $\epsilon$ representa a linguagem $\{ \epsilon \}$
	-  $\emptyset$ representa a linguagem $\{ \emptyset \}$
	-  $(R_{1}\cup R_{2})$ representa a linguagem $L(R_{1})\cup L(R_{2})$
	-  $(R_{1}\circ R_{2})$ representa a linguagem $L(R_{1})\circ L(R_{2})$
	-  $(R_{1})*$ representa a linguagem $L(R_{1})*$
-  $\Sigma=\{ 0,1 \}$
	-  $A=\{ w:w\text{ tem subtring 00} \}$
	-  $L(R)=A$
		-  $L^{0}=\{ \epsilon \}$ 
	-  $(0\cup 1)*00(0\cup 1)*$
		-  $\Sigma*00\Sigma*$
	-  $|w|=$ comprimento da string
-  $\Sigma=\{ 0,1 \}$
	-  $A=\{ w\in \Sigma*:|w|=4 \}$
		-  $(0\cup 1)(0\cup 1)(0\cup 1)(0\cup 1)$
		-  $\Sigma\Sigma\Sigma\Sigma$
		-  $\Sigma ^{4}$
-  $0*10*$ tem exatamente um $1$
-  $(\Sigma\Sigma)*$ tem número par de símbolos
-  $(0\cup\epsilon)(1\cup\epsilon)=\{ 0,1,\epsilon,01 \}$
-  $D=\{ 0,1,2,3,4,5,6,7,8,9 \}$
	-  $(+\cup-\cup\epsilon)(D^{+}\cup D^{+}.D^{*}\cup D^{*}.D^{+})$
	- Linguagens dos `ints` e `floats`
-  $D^{+}=DD^{*}$ reconhece:
	-  $123$
	-  $0.2$
	-  $.2$
	-  $2.$