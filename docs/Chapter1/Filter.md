## フィルターとは
まず始めにフィルターを定義する。本稿では集合上のフィルターを扱い、一般に真のフィルターと呼ばれるものを考える。

**定義**
${ X }$を集合とする。部分集合の族${ \mathscr{F}\subset 2^{X}, \neq \emptyset }$は空でないとする。更に${ \mathscr{F} }$は以下を満たすとする。

1. ${ \emptyset\notin\mathscr{F} }$である。
2. ${ V\in\mathscr{F}, V\subset W }$なら${ W\in\mathscr{F} }$が成り立つ。
3. ${ V, W\in\mathscr{F} }$なら${ V\cap W\in\mathscr{F} }$が成り立つ。

このとき${ \mathscr{F} }$を${ X }$のフィルター（filter）と呼ぶ。
 
例を挙げるとキリがないので重要なものを一つだけ挙げよう。

**例**
${ X }$を無限集合とする。${ X\setminus S }$が有限集合となるような${ S\subset X }$全体をフレシェ（Fréchet）フィルターと呼び、${ \mathcal{FC} }$で表す。

この他にも位相空間${ X }$においてある集合${ A\subset X }$（あるいは一点${ x\in X }$）を内部に含む集合全体はフィルターを成す。ここからフィルターは近傍系の一般化であることが分かる。というよりもむしろ、位相はフィルターの場に遠近感を加えたものと捉えることができる。

次に、フィルターの作り方について学ぶ。色々と方法はあるが、以下の構成法が基本的だろう。

**定義**
部分集合の族${ \mathscr{B}\subset 2^{X}, \neq \emptyset }$は空でないとする。更に${ \mathscr{B} }$は以下を満たすとする。

1. ${ \emptyset\notin\mathscr{B} }$である。
2. ${ A, B\in\mathscr{B} }$なら、ある${ C\in\mathscr{B} }$が存在して${ C\subset A\cap B }$が成り立つ。

このとき${ \mathscr{B} }$を${ X }$のプレフィルター（prefilter）と呼ぶ。

**注意**
本稿ではprefilterと書くが、普通はフィルター基（filter base）と呼ぶ。prefilterという語を採用した理由は、filterとfilter baseでは個人的に視認性が悪いからである。prefilterと調べても出てこないので悪しからず。

* filterはprefilterである。

**命題**
${ \mathscr{B}\subset 2^{X} }$はprefilterとする。このとき${ \mathscr{B} }$を含む最小のフィルターが存在する。

（証明）各${ B\in\mathscr{B} }$について${ B }$より大きな集合を全て集めたもの

$$
\displaystyle \mathscr{F}=\lbrace F : \exists B\in\mathscr{B}, B\subset F \rbrace
$$

が${ \mathscr{B} }$を含む最小のフィルターとなる。実際${ \emptyset\notin\mathscr{B} }$より${ \emptyset\notin\mathscr{F} }$であり、${ V\in\mathscr{F}, V\subset W }$について${ B\in\mathscr{B} }$が存在して${ B\subset V\subset W }$が成り立つから${ W\in\mathscr{F} }$が従う。${ V, W\in\mathscr{F} }$とすると${ A, B\in\mathscr{B} }$が存在して${ A\subset V, B\subset W }$となるが、ここでprefilterの定義より、ある${ C\in\mathscr{B} }$が存在して${ C\subset A\cap B\subset V\cap W }$となる。つまり${ V\cap W\in\mathscr{F} }$を得る。最小性は明らかだろう。${ \square }$

最小性から一意性が従うので、フィルターの生成を定義することができる。

**定義**
prefilter${ \mathscr{B} }$を含む最小のフィルターを${ \langle \mathscr{B} \rangle }$で表し、${ \mathscr{B} }$が生成するフィルターと呼ぶ。具体的には
 
$$
\displaystyle \langle \mathscr{B} \rangle = \lbrace F : \exists B\in\mathscr{B} , B\subset F \rbrace
$$

で実現される。

* filterはprefilterとして生成するフィルターと等しい。

**定義**
部分集合${ A\subset X, \neq \emptyset }$は空でないとする。このとき${ \langle A \rangle:=\langle \lbrace A \rbrace \rangle }$で表されるフィルターを単項フィルター（principal filter）と呼ぶ。特に${ x\in X }$について${ A=\lbrace x \rbrace }$のとき${ \langle x \rangle:=\langle \lbrace x \rbrace \rangle=\langle \lbrace \lbrace x \rbrace \rbrace \rangle }$を点フィルター（point filter）と呼ぶ。
