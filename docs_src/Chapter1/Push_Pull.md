<!--
    フィルターのpush-forward、フィルターのpull-back
-->
## push-forwardとpull-back
集合間の写像が与えられたとき、定義域のフィルターを値域へ押し出したり、あるいは値域のフィルターを定義域へ引き戻したりする操作を考えたくなる。このような操作はフィルターの生成を用いて定義されるが、自然な条件で自然な対応が付く。

**命題**
${ X, Y }$を集合とし、${ \mathscr{A}\subset 2^{X} }$を${ X }$のprefilterとする。写像${ f\colon X\rightarrow Y }$について

$$
\displaystyle f( \mathscr{A} ):=\lbrace f( V )\subset Y : V\in\mathscr{A} \rbrace\subset 2^{Y}
$$

は${ Y }$のprefilterとなる。

（証明）${ V\neq\emptyset }$より${ f( V )\neq\emptyset }$である。${ V, W\in\mathscr{A} }$について${ f( V ), f( W )\in f( \mathscr{A} ) }$を考える。${ \mathscr{A} }$はprefilterであるから${ A\in\mathscr{A} }$を${ A\subset V\cap W }$となるように取れる。${ f( A )\in f( \mathscr{A} ) }$かつ${ f( A )\subset f( V\cap W )\subset f( V )\cap f( W ) }$より、${ f( \mathscr{A} ) }$はprefilterである。${ \square }$

**定義**
特に${ \mathscr{A}=\mathscr{F} }$がフィルターであるとき、

$$
\displaystyle f_{\ast}\mathscr{F}:=\langle f( \mathscr{F} ) \rangle
$$

を${ \mathscr{F} }$のpush-forwardと呼ぶ。

**命題**
${ X, Y }$を集合とし、${ \mathscr{B}\subset 2^{Y} }$を${ Y }$のprefilterとする。写像${ f\colon X\rightarrow Y }$について、任意の${ B\in\mathscr{B} }$が${ f^{-1}( B )\neq\emptyset }$を満たすとする。このとき

$$
\displaystyle f^{-1}( \mathscr{B} ):=\lbrace f^{-1}( W )\subset X : W\in\mathscr{B} \rbrace\subset 2^{X}
$$

は${ X }$のprefilterとなる。

（証明）定義より${ f^{-1}( \mathscr{B} ) }$は空集合を含まない。${ V, W\in\mathscr{B} }$について${ f^{-1}( V ), f^{-1}( W )\in f^{-1}( \mathscr{B} ) }$を考える。${ \mathscr{B} }$はprefilterであるから${ B\in\mathscr{B} }$を${ B\subset V\cap W }$となるように取れる。${ f^{-1}( B )\subset f^{-1}( V\cap W )=f^{-1}( V )\cap f^{-1}( W ) }$かつ${ f^{-1}( B )\in f^{-1}( \mathscr{B} ) }$より、${ f^{-1}( \mathscr{B} ) }$はprefilterである。${ \square }$

**定義**
特に${ \mathscr{B}=\mathscr{G} }$がフィルターであるとき、

$$
\displaystyle f^{\ast}\mathscr{G}:=\langle f^{-1}( \mathscr{G} ) \rangle
$$

を${ \mathscr{G} }$のpull-backと呼ぶ。

- pull-backが定義できる${ \mathscr{G} }$には条件がある。

以下でこれらの性質を示す。まずフィルターの生成という観点から言うと、push-forwardは生成について可換である。

**命題**
${ f\colon X\rightarrow Y }$を写像とする。${ \mathscr{A}\subset 2^{X} }$を${ X }$のprefilterとすると、

$$
\displaystyle f_{\ast}\langle \mathscr{A} \rangle=\langle f( \mathscr{A} ) \rangle
$$

が成り立つ。

（証明）${ f_{\ast}\langle \mathscr{A} \rangle\supset f( \langle \mathscr{A} \rangle )\supset f( \mathscr{A} ) }$なので、生成の最小性より${ f_{\ast}\langle \mathscr{A} \rangle\supset\langle f( \mathscr{A} ) \rangle }$が従う。よって逆を示せば良い。左辺から元を取り${ F\in f_{\ast}\langle \mathscr{A} \rangle }$とする。ある${ G\in\langle \mathscr{A} \rangle }$が存在して${ f( G )\subset F }$が成り立つ。更に${ G }$について、ある${ H\in\mathscr{A} }$が存在して${ H\subset G }$が成り立つ。よって${ f( H )\subset f( G )\subset F }$だから${ F\in\langle f( \mathscr{A} ) \rangle }$を得る。${ \square }$

push-forwardの合成はpush-forwardである。

**命題**
${ X, Y, Z }$を集合とし、${ f\colon X\rightarrow Y, g\colon Y\rightarrow Z }$を写像とすると、

$$
\displaystyle ( g\circ f )_{\ast}=g_{\ast}\circ f_{\ast}
$$

が成り立つ。

（証明）${ \mathscr{F}\subset 2^{X} }$を${ X }$のフィルターとする。${ ( g\circ f )_{\ast}\mathscr{F}=g_{\ast}( f_{\ast}\mathscr{F} ) }$を示せば良い。左辺から元を取り${ F\in( g\circ f )_{\ast}\mathscr{F} }$とする。ある${ G\in\mathscr{F} }$が存在して${ g\circ f( G )\subset F }$が成り立つ。${ g\circ f( G )=g( f( G ) ) }$だから${ f( G )\in f( \mathscr{F} )\subset f_{\ast}\mathscr{F} }$より${ F\in g_{\ast}( f_{\ast}( \mathscr{F} ) ) }$を得る。逆に${ F\in g_{\ast}( f_{\ast}\mathscr{F} ) }$とすると、ある${ G\in f_{\ast}\mathscr{F} }$が存在して${ g( G )\subset F }$が成り立つ。同様にある${ H\in\mathscr{F} }$が存在して${ f( H )\subset G }$が成り立つから、${ ( g\circ f )( H )\subset g( G )\subset F }$を得る。故に${ F\in ( g\circ f )_{\ast}\mathscr{F} }$となる。${ \square }$

push-forwardとpull-backの間には以下の関係がある。

**命題**
${ f\colon X\rightarrow Y }$を写像とする。${ \mathscr{F}\subset 2^{X}, \mathscr{G}\subset 2^{Y} }$を${ X, Y }$のフィルターとする。以下が成り立つ。

1. ${ f_{\ast}\mathscr{F} }$のpull-backは常に定義できて${ \mathscr{F}\subset f^{\ast}( f_{\ast}\mathscr{F} ) }$を満たす。
2. 任意の${ G\in\mathscr{G} }$が${ f^{-1}( G )\neq\emptyset }$を満たすなら（${ \mathscr{G} }$のpull-backが定義できるなら）${ \mathscr{G}\subset f_{\ast}( f^{\ast}\mathscr{G} ) }$が成り立つ。

（証明）上は自明。下は${ G\in\mathscr{G} }$に対し、${ f( f^{-1}( G ) )\subset G }$より${ G\in f_{\ast}( f^{\ast}\mathscr{G} ) }$を得る。${ \square }$

写像が全射のときpush-forwardはフィルターの像と一致する。

**補題**
${ f\colon X\rightarrow Y }$は全射とする。${ \mathscr{F}\subset 2^{X} }$を${ X }$のフィルターとすると、${ f_{\ast}\mathscr{F}=f( \mathscr{F} ) }$が成り立つ。特に${ f( \mathscr{F} ) }$はフィルターである。

（証明）左辺から元を取り${ G\in f_{\ast}\mathscr{F} }$とする。ある${ F\in\mathscr{F} }$が存在して${ f( F )\subset G }$が成り立つ。${ F\subset f^{-1}( f( F ) )\subset f^{-1}( G ) }$より${ f^{-1}( G )\in\mathscr{F} }$だが、${ f }$は全射なので${ G=f( f^{-1}( G ) )\in f( \mathscr{F} ) }$を得る。（一般には${ f( f^{-1}( G ) )\subset G }$なので成立しない。）${ \square }$

写像が全射のときはpull-backも定義できる。更にpull-backがフィルターの逆像と一致するには、写像が全単射であることが十分である。

**補題**
${ f\colon X\rightarrow Y }$は全単射とする。${ \mathscr{G}\subset 2^{Y} }$を${ Y }$のフィルターとすると、${ f^{\ast}\mathscr{G}=f^{-1}( \mathscr{G} ) }$が成り立つ。特に${ f^{-1}( \mathscr{G} ) }$はフィルターである。

（証明）左辺から元を取り${ F\in f^{\ast}\mathscr{G} }$とする。${ f }$は単射なので${ F=f^{-1}( f( F ) ) }$が成り立つから、${ f( F )\in\mathscr{G} }$を示せば良い。（一般には${ F\subset f^{-1}( f( F ) ) }$である。）${ F\in f^{\ast}\mathscr{G} }$より、ある${ G\in\mathscr{G} }$が存在して${ f^{-1}( G )\subset F }$が成り立つ。${ f( f^{-1}( G ) )\subset f( F ) }$となるが、${ f }$は全射なので${ G=f( f^{-1}( G ) )\subset f( F ) }$を得る。${ G\in\mathscr{G} }$から${ f( F )\in\mathscr{G} }$が従う。${ \square }$

**系**
${ f\colon X\rightarrow Y }$は全単射とする。${ \Phi( X ), \Phi( Y ) }$は${ X, Y }$のフィルター全体の集合とする。このとき

$$
\displaystyle \begin{alignedat}{2} f^{\ast}\circ f_{\ast}&=\mathrm{id}_{\Phi( X )}, &\qquad f_{\ast}\circ f^{\ast}&=\mathrm{id}_{\Phi( Y )} \end{alignedat}
$$

が成り立つ。