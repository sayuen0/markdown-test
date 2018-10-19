<!--
    収束空間、連続写像、反射的有向グラフ、グラフ準同型
-->
## 収束空間
収束空間の研究はCartanから約10年後にChoquetなどにより始められた。収束空間の定義は様々だが、Eva Lowen-ColebundersのFunction Classes of Cauchy Continuous Maps（1989）で言及されている（らしい）定義を採用する。

**定義**
${ X }$を集合とする。各点${ x\in X }$について${ X }$のフィルターの族${ \lambda( x ) }$が与えられているとする。${ \lambda\colon x\mapsto\lambda( x ) }$が以下を満たすとき、${ ( X, \lambda) }$を収束空間（convergent space）と呼ぶ。

1. ${ \langle x \rangle\in\lambda( x ) }$である。
2. ${ \mathscr{F}\in\lambda( x ) }$とする。フィルター${ \mathscr{G}\subset 2^{X} }$について${ \mathscr{F}\subset\mathscr{G} }$なら${ \mathscr{G}\in\lambda( x ) }$を満たす。
3. ${ \mathscr{F}, \mathscr{G}\in\lambda( x ) }$なら${ \mathscr{F}\cap\mathscr{G}\in\lambda( x ) }$である。

フィルター${ \mathscr{F}\subset 2^{X} }$について${ \mathscr{F}\in\lambda( x ) }$であることを${ \mathscr{F}\rightarrow x }$と書けば${ \lambda }$を明示せずに収束空間を定義できる。この意味で上記を満たす関係${ \rightarrow }$を収束構造（convergent structure）とも呼ぶ。（${ X }$のフィルター全体を${ \Phi( X ) }$とすれば、${ \Phi( X )\times X }$の部分集合としての「関係」である。）また${ \mathscr{F}\rightarrow x }$のことを、${ \mathscr{F} }$が${ x }$に収束するともいう。${ x }$は${ \mathscr{F} }$の極限点や収束先ともいう。

位相空間の近傍系${ x\mapsto\mathfrak{N}( x ) }$は収束構造を定める。これについては後で詳しく扱うとして、ここではもう少し素朴な例を挙げよう。

**例**
有向グラフ（directed graph）とは、頂点の集合${ V }$と、向き付けられた辺の集合${ E\subset V\times V }$の組${ ( V, E ) }$である。（有向辺${ (v, u )\in E }$は始点${ v }$から終点${ u }$への矢印で表す。）有効グラフが反射的（reflexible）とは、任意の頂点${ v\in V }$について${ ( v, v )\in E }$が成り立つことを言う。

さて反射的有向グラフ${ ( V, E ) }$において、頂点${ v\in V }$について${ v }$から出る矢印の終点全体

$$
\displaystyle \overrightarrow{v}:=\lbrace u\in V : ( v, u )\in E \rbrace
$$

を考える。このとき収束構造${ \mathscr{F}\rightarrow v }$を${ \overrightarrow{v}\in\mathscr{F} }$で定めることができる。実際、${ ( v, v )\in E }$より${ v\in\overrightarrow{v} }$だから${ \overrightarrow{v}\in\langle v \rangle }$である。${ \mathscr{F}\rightarrow v, \mathscr{F}\subset\mathscr{G} }$とすれば、${ \overrightarrow{v}\in\mathscr{F}\subset\mathscr{G} }$より${ \mathscr{G}\rightarrow v }$である。${ \overrightarrow{v}\in\mathscr{F}, \mathscr{G} }$なら${ \overrightarrow{v}\in\mathscr{F}\cap\mathscr{G} }$も成り立つ。このようにして反射的有向グラフは収束空間となる。この収束構造において、単項フィルター${ \langle \overrightarrow{v} \rangle }$は${ v }$に収束する。

念頭にあるのは収束空間のカテゴリーである。次は射について考えてみよう。

**定義**
${ X, Y }$を収束空間、${ f\colon X\rightarrow Y }$を写像とする。${ x\in X }$とする。任意のフィルター${ \mathscr{F}\subset 2^{X} }$について、${ \mathscr{F}\rightarrow x }$なら${ f_{\ast}\mathscr{F}\rightarrow f( x ) }$が成り立つとき、写像${ f }$は${ x }$で連続（continuous）であるという。任意の点${ x\in X }$で${ f }$が連続なとき、${ f }$は連続であるという。

**命題**
${ X, Y, Z }$を収束空間、${ f\colon X\rightarrow Y, g\colon Y\rightarrow Z }$を写像とする。${ f, g }$が連続なら${ g\circ f }$も連続である。

（証明）${ f, g }$は連続とする。${ \mathscr{F}\rightarrow x }$に対し${ f_{\ast}\mathscr{F}\rightarrow f( x ) }$であるから${ g_{\ast}( f_{\ast}\mathscr{F} )\rightarrow g( f( x ) ) }$を得る。${ g_{\ast}\circ f_{\ast}=( g\circ f )_{\ast} }$より、${ g\circ f }$も連続となる。${ \square }$

**例**
反射的有向グラフの例で連続写像を見てみよう。${ f\colon( V_{1}, E_{1} )\rightarrow( V_{2}, E_{2} ) }$をグラフ間の写像として、${ v\in V_{1} }$とする。${ f }$が${ v }$で連続であるとしよう。このとき単項フィルター${ \langle \overrightarrow{v} \rangle }$は${ v }$に収束するから${ \langle \overrightarrow{v } \rangle\rightarrow v }$である。故に${ f_{\ast}\langle \overrightarrow{v} \rangle\rightarrow f( v ) }$が成り立つ。つまり${ \overrightarrow{f( v )}\in f_{\ast}\langle \overrightarrow{v} \rangle }$であって、従って${ f( \overrightarrow{v} )\subset \overrightarrow{f( v )} }$が成り立つ。逆に${ f( \overrightarrow{v} )\subset\overrightarrow{f( v )} }$が成り立つなら、${ \mathscr{F}\rightarrow v }$について${ \overrightarrow{v}\in\mathscr{F} }$より${ f( \overrightarrow{v} )\in f( \mathscr{F} )\subset f_{\ast}\mathscr{F} }$である。よって${ \overrightarrow{f( v )}\in f_{\ast}\mathscr{F} }$となり${ f }$は${ v }$で連続となる。従って次が成り立つ。

**定理**
${ f\colon( V_{1}, E_{1} )\rightarrow( V_{2}, E_{2} ) }$を反射的有向グラフの間の写像とする。${ v, u\in V_{1} }$とする。以下は同値である。

- ${ f }$は${ v }$で連続である。
- ${ f( \overrightarrow{v} )\subset\overrightarrow{f( v )} }$が成り立つ。

更に以下も同値である。

- ${ f }$は連続である。
- ${ ( v, u )\in E_{1} }$なら${ ( f( v ), f( u ) )\in E_{2} }$が成り立つ。（つまり${ f }$はグラフ準同型である。）

カテゴリー論的に言えば、反射的有向グラフとグラフ準同型の為す圏は、収束空間と連続写像の為す圏に忠実充満に埋め込める。この意味で連続性は自然な定義と言える。実はそれだけでなく、位相空間の圏もまた忠実充満に埋め込める。後で述べるが、収束空間の圏はカルテシアン閉であり、特に${ X }$から${ Y }$への連続写像全体${ C( X, Y ) }$もまた「自然な」収束構造を持つ。位相空間の圏はこの性質を持たない（反射的有向グラフの圏も持たない？）ため、我々が収束空間について考える良い動機付けになっている。(なお位相空間が特別な場合には、コンパクト開位相という自然な位相が入る。これはこれで考察する意義がある。)

**定義**
収束空間の間の写像${ f\colon X\rightarrow Y }$が全単射で${ f }$及び${ f^{-1} }$が連続のとき、${ X }$と${ Y }$は収束空間として同型（isomorphic）であるという。