## 位相的概念とその性質
今回は閉集合について考えてみよう。せっかく収束概念があるので以下のように考える。

**定義**
${ X }$を収束空間とする。${ \Phi( X ) }$を${ X }$のフィルター全体とする。${ A\subset X }$に対し、${ A }$の閉包（closure）を

$$
\displaystyle \mathrm{cl}( A ):=\lbrace x\in X : \exists\mathscr{F}\in\Phi( X ), \mathscr{F}\rightarrow x, A\in\mathscr{F} \rbrace
$$

で定める。つまり${ A }$を含むフィルターの極限点全体を${ \mathrm{cl}( A ) }$とする。

この定義が自然なものであると確認するには、後で述べるフィルターの制限や収束空間の部分空間についての議論が必要となる。今は${ A }$の収束列の収束先という類推で納得しておく。

上の${ \mathrm{cl} }$はKatětov閉包と呼ばれるらしい。

**命題**
閉包は以下を満たす。

1. ${ \mathrm{cl}( \emptyset )=\emptyset }$である。
2. ${ A\subset\mathrm{cl}( A ) }$である。
3. ${ \mathrm{cl}( A\cup B )=\mathrm{cl}( A )\cup\mathrm{cl}( B ) }$が成り立つ。

3番目から特に${ A\subset B }$なら${ \mathrm{cl}( A )\subset\mathrm{cl}( B ) }$が成り立つ。

（証明）フィルターは空集合を含まないから${ \mathrm{cl}( \emptyset )=\emptyset }$である。

${ x\in A }$とすると${ \langle x \rangle\rightarrow x }$かつ${ A\in\langle x \rangle }$が成り立つ。よって${ a\in\mathrm{cl}( A ) }$が従う。

${ x\in\mathrm{cl}( A\cup B ) }$とする。あるフィルター${ \mathscr{F}\rightarrow x }$が存在して${ A\cup B\in\mathscr{F} }$となる。${ A\notin\mathscr{F} }$のとき${ \mathscr{F}_{\setminus A}=\lbrace V : \exists F\in\mathscr{F}, F\setminus A\subset V \rbrace }$は${ \mathscr{F} }$を含むフィルターである。よって${ \mathscr{F}_{\setminus A}\rightarrow x }$であり、一方${ A\cup B\setminus A\subset B }$より${ B\in\mathscr{F}_{\setminus A} }$である。従って${ x\in\mathrm{cl}( B )\subset\mathrm{cl}( A )\cup\mathrm{cl}( B ) }$を得る。

逆に${ x\in\mathrm{cl}( A ) }$なら、あるフィルター${ \mathscr{F}\rightarrow x }$が存在して${ A\in\mathscr{F} }$を満たす。特に${ A\subset A\cup B }$より${ A\cup B\in\mathscr{F} }$であるから${ x\in\mathrm{cl}( A\cup B ) }$となる。${ B }$についても同様である。${ \square }$

さて閉包が${ \mathrm{cl}( \mathrm{cl}( A ) )=\mathrm{cl}( A ) }$を満たせば、これは位相の公理系（Kuratowskiの公理系）を定めることになる。しかし、もちろんこれは一般に成り立たない。この公理系では閉集合を${ \mathrm{cl}( A )=A }$を満たす集合${ A\subset X }$で定めていた。

**定義**
${ X }$を収束空間とする。${ A\subset X }$とする。${ \mathrm{cl}( A )=A }$が成り立つとき、${ A }$は閉（closed）であるという。

**補題**
${ X }$を収束空間とする。${ U\subset X }$とする。以下は同値である。

- ${ U }$はopenである。
- ${ X\setminus U }$はclosedである。

（証明）${ U }$はopenとする。${ \mathrm{cl}( X\setminus U )\subset X\setminus U }$を示せば良い。${ x\in \mathrm{cl}( X\setminus U ) }$に対し、あるフィルター${ \mathscr{F}\rightarrow x }$が存在して${ X\setminus U\in\mathscr{F} }$となる。${ x\in U }$なら${ U\in\mathscr{N}_{x}\subset\mathscr{F} }$より矛盾する。よって${ X\setminus U }$はclosedである。

逆に${ U }$はopenでないとする。ある元${ x\in U }$とフィルター${ \mathscr{F}\rightarrow x }$が存在して${ U\notin\mathscr{F} }$が成り立つ。${ \mathscr{F}_{\setminus U}=\lbrace V : \exists F\in\mathscr{F}, F\setminus U\subset V \rbrace }$は${ \mathscr{F} }$を含むフィルターである。${ X\setminus U\in\mathscr{F}_{\setminus U} }$かつ${ \mathscr{F}_{\setminus U}\rightarrow x }$より${ x\in\mathrm{cl}( X\setminus U ) }$を得る。${ x\notin X\setminus U }$より${ X\setminus U }$はclosedでない。${ \square }$

収束空間がトポロジカルなときopenと開集合であることは同値だった。従って補題より${ A }$が閉集合であることと、${ A }$がclosedであることは同値となる。よって次が成り立つ。

**命題**
${ X }$をトポロジカルな収束空間とする。閉包は位相空間の閉包と一致する。

（証明）${ A\subset X }$に対し、位相空間の閉包を${ \overline{A} }$で表す。

${ A\subset\overline{A} }$より、${ \overline{A} }$はclosedだから${ \mathrm{cl}( A )\subset\mathrm{cl}( \overline{A} )=\overline{A} }$が成り立つ。

逆を示すために${ x\in X\setminus\mathrm{cl}( A ) }$とする。${ x\in\overline{A} }$とすると、任意の${ N\in\mathfrak{N}( x ) }$について${ N\cap A\neq\emptyset }$が成り立つ。このときフィルター${ \langle A \rangle }$についてvel積${ \mathscr{G}:=\mathfrak{N}( x )\vee\langle A \rangle }$が定義できる。今${ x\notin\mathrm{cl}( A ) }$より任意のフィルター${ \mathscr{F}\rightarrow x }$について${ A\notin\mathscr{F} }$が成り立つが、${ \mathscr{G}\supset\mathfrak{N}( x )\rightarrow x }$より矛盾する。従って${ x\notin\overline{A} }$である。${ \square }$

以上により、トポロジカルな収束空間において、近傍、開、閉、閉包の概念は全て同一のものであることが分かる。

**命題**
${ X }$を収束空間とする。${ x\in X, N\subset X }$とする。以下は同値である。

- ${ N }$は${ x }$の近傍である。
- ${ x\notin\mathrm{cl}( X\setminus N ) }$である。

（証明）${ x\in\mathrm{cl}( X\setminus N ) }$とする。あるフィルター${ \mathscr{F}\rightarrow x }$が存在して${ X\setminus N\in\mathscr{F} }$を満たす。${ N\notin\mathscr{F} }$より${ N\notin\mathscr{N}_{x} }$である。

逆に${ N\notin\mathscr{N}_{x} }$なら、あるフィルター${ \mathscr{F}\rightarrow x }$が存在して${ N\notin\mathscr{F} }$となる。ここで${ \mathscr{F}_{\setminus N}=\lbrace V : \exists F\in\mathscr{F}, F\setminus N\subset V \rbrace }$は${ \mathscr{F} }$を含むフィルターとなる。${ X\setminus N\in\mathscr{F}_{\setminus N} }$かつ${ \mathscr{F}_{\setminus N}\rightarrow x }$より${ x\in\mathrm{cl}( X\setminus N ) }$が従う。${ \square }$

**定理**
${ f\colon X\rightarrow Y }$は収束空間の間の連続写像とする。このとき以下が成り立つ。

1. ${ U\subset Y }$がopenなら${ f^{-1}( U ) }$はopenである。
2. ${ F\subset Y }$がclosedなら${ f^{-1}( F ) }$はclosedである。
3. ${ x\in X }$について、${ N\subset Y }$が${ f( x ) }$の近傍なら${ f^{-1}( N ) }$は${ x }$の近傍である。
4. ${ A\subset X }$について${ f( \mathrm{cl}( A ) )\subset\mathrm{cl}( f( A ) ) }$が成り立つ。

（証明）1は前節で示した。2は1と${ f^{-1}( Y\setminus F )=X\setminus f^{-1}( F ) }$より分かる。

3を示そう。${ \mathscr{F}\rightarrow x }$なら${ f_{\ast}\mathscr{F}\rightarrow f( x ) }$だから、${ \mathscr{N}_{f( x )}\subset f_{\ast}\mathscr{F} }$である。よって${ N\in\mathscr{N}_{f( x )} }$について、ある${ F\in\mathscr{F} }$が存在して${ f( F )\subset N }$となる。${ F\subset f^{-1}( N ) }$より${ f^{-1}( N )\in\mathscr{F} }$を得る。従って${ f^{-1}( N )\in\mathscr{N}_{x} }$が成り立つ。

4を示そう。${ x\in\mathrm{cl}( A ) }$とすると、あるフィルター${ \mathscr{F}\rightarrow x }$が存在して${ A\in\mathscr{F} }$を満たす。${ f_{\ast}\mathscr{F}\rightarrow f( x ) }$より${ f( A )\in f( \mathscr{F} )\subset f_{\ast}\mathscr{F} }$から${ f( x )\in\mathrm{cl}( f( A ) ) }$を得る。${ \square }$