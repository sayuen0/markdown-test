<!--
    フィルターの大小、prefilterのfiner/coarser、フィルターのwedge積、prefilterのvel積、フィルターのvel積、フィルター化
-->
## フィルターの大小
まずはフィルターの大小を言い換えよう。

**命題**
${ \mathscr{F}, \mathscr{G}\subset 2^{X} }$をフィルターとする。以下は同値である。

- ${ \mathscr{F}\subset\mathscr{G} }$である。
- 任意の${ F\in\mathscr{F} }$について、ある${ G\in\mathscr{G} }$が存在して${ G\subset F }$が成り立つ。

上から下は全ての集合族で成り立つので自明である。一方で下から上はフィルターの性質による。つまり下の条件の方が強いため、これをprefilterに対する大小として採用しよう。

**定義**
${ \mathscr{A}, \mathscr{B}\subset 2^{X} }$をprefilterとする。このとき関係${ \mathscr{A}\dashv\mathscr{B} }$を、

- 「任意の${ A\in\mathscr{A} }$について、ある${ B\in\mathscr{B} }$が存在して${ B\subset A }$が成り立つ」

で定める。このとき${ \mathscr{B} }$は${ \mathscr{A} }$より細かい（finer）、あるいは${ \mathscr{A} }$は${ \mathscr{B} }$より粗い（coarser）と言う。

この関係は次の命題により生成されたフィルターの大小で言い換えることができる。

**命題**
${ \mathscr{A}, \mathscr{B}\subset 2^{X} }$をprefilterとする。以下は同値である。

- ${ \mathscr{A}\dashv\mathscr{B} }$である。
- ${ \langle \mathscr{A} \rangle\subset \langle \mathscr{B} \rangle }$である。

ちなみに関係${ \dashv }$は反射的（${ \mathscr{A}\dashv\mathscr{A} }$）かつ推移的（${ \mathscr{A}\dashv\mathscr{B}, \mathscr{B}\dashv\mathscr{C} }$なら${ \mathscr{A}\dashv\mathscr{C} }$）である。よって関係${ \sim }$を${ \mathscr{A}\dashv\mathscr{B} }$かつ${ \mathscr{B}\dashv\mathscr{A} }$のとき（つまり${ \langle \mathscr{A} \rangle=\langle \mathscr{B} \rangle }$のときに）${ \mathscr{A}\sim\mathscr{B} }$と定めれば、これはprefilterに対する同値関係を与える。

次に与えられたフィルターから、より粗いフィルターを作る方法について考える。${ \mathscr{F}, \mathscr{G}\subset 2^{X} }$をフィルターとしよう。このとき集合としての共通部分${ \mathscr{F}\cap\mathscr{G} }$もまたフィルターである。より一般に${ \mathscr{F}_{\lambda} }$を${ \lambda\in\Lambda }$で添え字付けられたフィルターの族とすると、集合としての共通部分${ \bigcap_{\lambda\in\Lambda}\mathscr{F}_{\lambda} }$はフィルターとなる。これは各${ \mathscr{F}_{\lambda} }$より粗いフィルターのうち最も大きいものとなる。（フィルターについての粗い・細かいは包含関係による順序を定めるが、その順序に関する下限を与える。）

**定義**
上記のフィルター

$$
\displaystyle \begin{alignedat}{2} \mathscr{F}\wedge\mathscr{G}&:=\mathscr{F}\cap\mathscr{G}, &\qquad \bigwedge_{\lambda\in\Lambda}\mathscr{F}_{\lambda}&:=\bigcap_{\lambda\in\Lambda}\mathscr{F}_{\lambda} \end{alignedat}
$$

をフィルターのwedge積と呼ぶ。（次のvel積との対比で定義するが、分かり易さを踏まえて以降は共通部分の記号を用いる。）

続いて、より細かいフィルターを作る方法について考える。こちらの方が重要であり、一般に存在するとは限らない。

**補題**
${ \mathscr{A}, \mathscr{B}\subset 2^{X} }$をprefilterとする。任意の${ A\in\mathscr{A}, B\in\mathscr{B} }$について${ A\cap B\neq\emptyset }$であるとする。このとき

$$
\displaystyle \mathscr{A}\vee\mathscr{B}:=\lbrace A\cap B : A\in\mathscr{A}, B\in\mathscr{B} \rbrace
$$

は${ \mathscr{A}, \mathscr{B} }$を含むprefilterとなる。

特に${ \mathscr{F}, \mathscr{G}\subset 2^{X} }$がフィルターのとき、${ \mathscr{F}\vee\mathscr{G} }$は${ \mathscr{F}, \mathscr{G} }$を含むフィルターとなり、更に包含順序に関する上限を与える。

（証明）定義より${ \mathscr{A}\vee\mathscr{B} }$は空集合を含まない。${ A_{1}, A_{2}\in\mathscr{A}, B_{1}, B_{2}\in\mathscr{B} }$について${ V=A_{1}\cap B_{1}, W=A_{2}\cap B_{2}\in\mathscr{A}\vee\mathscr{B} }$とする。${ \mathscr{A} }$はprefilterだから、ある${ A\in\mathscr{A} }$が存在して${ A\subset A_{1}\cap A_{2} }$となる。同様にある${ B\in\mathscr{B} }$が存在して${ B\subset B_{1}\cap B_{2} }$となる。${ A\cap B\in\mathscr{A}\vee\mathscr{B} }$であり、${ A\cap B\subset A_{1}\cap A_{2}\cap B_{1}\cap B_{2}\subset V\cap W }$より${ \mathscr{A}\vee\mathscr{B} }$はprefilterとなることが分かる。また${ X\in\mathscr{A}, \mathscr{B} }$より${ \mathscr{A}, \mathscr{B}\subset\mathscr{A}\vee\mathscr{B} }$が従う。

${ \mathscr{F}\vee\mathscr{G} }$がフィルターであることを示すには、自身の生成するフィルターと一致することを示せば良い。${ V\subset X }$について、ある${ F\in\mathscr{F}, G\in\mathscr{G} }$が${ F\cap G\subset V }$を満たすとする。${ \mathscr{F}, \mathscr{G} }$はフィルターなので${ F\cup V\in\mathscr{F}, G\cup V\in\mathscr{G} }$が成り立つ。故に${ V=V\cup( F\cap G )=( V\cup F )\cap( V\cup G )\in\mathscr{F}\vee\mathscr{G} }$である。上限、つまり最小上界となることは明白だろう。${ \square }$

**定義**
上記の${ \mathscr{A}\vee\mathscr{B} }$をprefilterのvel積と呼ぶ。同様に${ \mathscr{F}\vee\mathscr{G} }$はフィルターのvel積と呼ぶ。

- prefilterのvel積は一般に包含順序に関する上限を与えるとは限らない。（ちなみに関係${ \dashv }$は順序ではない。）

prefilterのvel積は生成と可換になる。

**命題**
${ \mathscr{A}, \mathscr{B}\subset 2^{X} }$はprefilterとする。このとき

$$
\displaystyle \langle \mathscr{A} \rangle\vee\langle \mathscr{B} \rangle=\langle \mathscr{A}\vee\mathscr{B} \rangle
$$

が成り立つ。

（証明）${ \mathscr{A}, \mathscr{B}\subset\mathscr{A}\vee\mathscr{B}\subset \langle \mathscr{A}\vee\mathscr{B} \rangle }$より、最小性から${ \langle \mathscr{A} \rangle, \langle \mathscr{B} \rangle\subset\langle \mathscr{A}\vee\mathscr{B} \rangle }$となる。よって${ \langle \mathscr{A} \rangle\vee\langle \mathscr{B} \rangle\subset\langle \mathscr{A}\vee\mathscr{B} \rangle }$も従う。逆も同様に${ \mathscr{A}\vee\mathscr{B}\subset\langle \mathscr{A} \rangle\vee\langle \mathscr{B} \rangle }$から従う。${ \square }$

もう一つ細かいフィルターを与える方法について紹介しておく。

**補題**
${ \mathscr{A}\subset 2^{X} }$をprefilterとする。${ S\subset X }$について${ S\notin\mathscr{A} }$であるとする。

$$
\displaystyle \mathscr{A}_{\setminus S}:=\lbrace V : \exists A\in\mathscr{A}, A\setminus S\subset V \rbrace
$$

は${ \mathscr{A} }$を含むフィルターとなる。

（証明）${ A\backslash S=\emptyset }$なら${ A\subset S }$となるので${ A\notin\mathscr{A} }$である。よって${ \emptyset\notin\mathscr{A}_{\setminus S } }$である。${ V\in\mathscr{A}_{\setminus S}, V\subset W }$とする。ある${ A\in\mathscr{A} }$が存在して${ A\setminus S\subset V }$が成り立つ。${ A\setminus S\subset V\subset W }$より${ W\in\mathscr{A}_{\setminus S} }$を得る。${ V, W\in\mathscr{A}_{\setminus S} }$とする。ある${ A, B\in\mathscr{A} }$が存在して${ A\setminus S\subset V, B\setminus S\subset W }$が成り立つ。${ \mathscr{A} }$はprefilterなので、ある${ C\in\mathscr{A} }$が存在して${ C\subset A\cap B }$が成り立つ。${ V\cap W\supset( A\setminus S )\cap( B\setminus S )=( A\cap B )\setminus S\supset C\setminus S }$より、${ V\cap W\in\mathscr{A}_{\setminus S} }$を得る。また任意の${ A\in\mathscr{A} }$について、${ A\setminus S\subset A }$より${ A\in\mathscr{A}_{\setminus S} }$である。つまり${ \mathscr{A}\subset\mathscr{A}_{\setminus S} }$が成り立つ。${ \square }$

${ \mathscr{A}_{\setminus S} }$は${ \mathscr{A} }$と${ X\setminus S }$を含む最小のフィルターでもある。実際、${ \mathscr{A} }$と${ X\setminus S }$を含むフィルター${ \mathscr{F} }$を取る。任意の${ V\in\mathscr{A}_{\setminus S} }$について、ある${ A\in\mathscr{A} }$が存在して${ A\setminus S\subset V }$が成り立つ。${ A\setminus S=A\cap( X\setminus S )\in\mathscr{F} }$より${ V\in\mathscr{F} }$を得る。

**定義**
上記の${ \mathscr{A}_{\setminus S} }$を${ S }$を通すフィルター化と呼ぶ。