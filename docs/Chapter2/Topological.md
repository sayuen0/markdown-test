## トポロジカルな収束構造
位相空間${ ( X, \mathcal{O} ) }$が自然な収束構造を持つことを述べよう。${ N\subset X }$が${ x\in X }$の近傍であるとは、ある${ U\in\mathcal{O} }$が存在して${ x\in U\subset N }$を満たすことだった。${ x }$の近傍全体を近傍系と呼び${ \mathfrak{N}( x ) }$で表せば次が成り立つ。

1. 任意の${ x\in X }$について${ X\in\mathfrak{N}( x ) }$であり、${ N\in\mathfrak{N}( x ) }$なら${ x\in N }$を満たす。
2. ${ N, M\in\mathfrak{N}( x ) }$なら${ N\cap M\in\mathfrak{N}( x ) }$である。
3. ${ N\in\mathfrak{N}( x ) }$かつ${ N\subset M\subset X }$なら${ M\in\mathfrak{N}( x ) }$である。
4. 任意の${ N\in\mathfrak{N}( x ) }$に対して、ある${ M\in\mathfrak{N}( x ) }$が存在して、${ y\in M }$なら${ N\in\mathfrak{N}( y ) }$が成り立つ。

逆にこれらを満たす${ \mathfrak{N}( x ) }$から位相を定義することもでき（Hausdorffの公理系）、その位相における近傍系と両立することが知られている。

さて1番目の前半と、2、3番目はほとんどフィルターの定義である。実際これをフィルターの定義とする流儀もあるが、本稿の定義においても近傍系はフィルターである。また1番目の後半は、収束空間の${ \langle x \rangle\rightarrow x }$に対応していると考えられる。そこで${ \mathscr{F}\rightarrow x }$を${ \mathfrak{N}( x )\subset\mathscr{F} }$で定めよう。この収束構造をtopological convergence structureと呼ぶ。

**定義**
収束空間${ X }$が位相的（topological）とは、収束構造がtopological convergence structureと一致することをいう。つまりある${ X }$の位相${ \mathcal{O} }$が存在して、${ \mathscr{F}\rightarrow x }$と${ \mathfrak{N}( x )\subset\mathscr{F} }$が同値となるときに、トポロジカルであるという。

**注意**
トポロジカルな収束構造とtopological convergence structureは同値の概念だが、出発点が違うという意味で区別している。

**命題**
${ X }$はトポロジカルな収束空間とする。${ \Phi( X ) }$を${ X }$のフィルター全体とする。このとき

$$
\displaystyle \mathfrak{N}( x )=\cap\lbrace \mathscr{F}\in\Phi( X ) : \mathscr{F}\rightarrow x \rbrace
$$

が成り立つ。

（証明）${ \mathscr{F}\rightarrow x }$なら${ \mathfrak{N}( x )\subset\mathscr{F} }$より左辺は右辺に含まれる。逆は近傍系がフィルターであることから${ \mathfrak{N}( x )\rightarrow x }$より従う。${ \square }$

- 位相は近傍系より一意的に定まるから、収束空間がトポロジカルなときその位相は一意的である。

この左辺は収束空間がトポロジカルでなければ定義できないが、右辺は一般の収束空間で定義できることに気付くだろう。

**定義**
${ X }$を収束空間とする。${ X }$のフィルター全体を${ \Phi( X ) }$とする。${ x\in X }$に対し、${ x }$に収束するフィルターの共通部分

$$
\displaystyle \mathscr{N}_{x}:=\cap\lbrace \mathscr{F}\in\Phi( X ) : \mathscr{F}\rightarrow x \rbrace
$$

を${ x }$の近傍フィルター（neighborhood filter）と呼び、この元を${ x }$の近傍と呼ぶ。

- トポロジカルな収束空間において、近傍フィルターは近傍系と一致し、各点の近傍は両者の意味で同一となる。

近傍系から位相を作る方法を思い出せば、位相的概念を収束構造に持ち込むことが出来る。例えば開集合は任意の${ x\in U }$について${ U\in\mathfrak{N}( x ) }$が成り立つ集合${ U\subset X }$である。そこで次を定める。

**定義**
${ X }$を収束空間とする。${ U\subset X }$とする。任意の${ x\in U }$について${ U\in\mathscr{N}_{x} }$が成り立つとき、${ U }$は開（open）であるという。

- トポロジカルな収束空間において、収束構造としてopenであることは、位相構造として開集合であることと同値である。

**補題**
${ X, Y }$をトポロジカルな収束空間とする。${ f\colon X\rightarrow Y }$を写像とする。以下は同値である。

- ${ f }$は収束構造として連続である。
- ${ U\subset Y }$がopenなら、${ f^{-1}( U )\subset X }$もopenである。

（証明）上から下は常に成り立つ。実際${ U\subset Y }$をopenとすると、${ x\in f^{-1}( U ) }$について${ f( x )\in U }$より、${ U\in\mathscr{N}_{f( x )} }$が成り立つ。${ f^{-1}( U )\in\mathscr{N}_{x} }$を示したい。${ \mathscr{F}\rightarrow x }$を取る。${ f }$は連続だから${ f_{\ast}\mathscr{F}\rightarrow f( x ) }$である。${ U }$はopenだから${ U\in f_{\ast}\mathscr{F} }$となる。つまり、ある${ F\in\mathscr{F} }$が存在して${ f( F )\subset U }$となる。${ F\subset f^{-1}( U ) }$より${ f^{-1}( U )\in\mathscr{F} }$を得る。従って${ f^{-1}( U )\in\mathscr{N}_{x} }$つまり${ f^{-1}( U ) }$はopenである。

下から上を示すのにトポロジカルであることが必要となる。${ X, Y }$の位相を${ \mathcal{O}_{X}, \mathcal{O}_{Y} }$とする。${ \mathscr{F}\rightarrow x }$とする。${ f }$が収束構造として連続であることを示すには${ f_{\ast}\mathscr{F}\rightarrow f( x ) }$つまり${ \mathfrak{N}( f( x ) )\subset f_{\ast}\mathscr{F} }$を示せば良い。${ N\in\mathfrak{N}( f( x ) ) }$を取ると、ある開集合${ V\in\mathcal{O}_{Y} }$が存在して${ f( x )\in V\subset N }$となる。${ x\in f^{-1}( V )\subset f^{-1}( N ) }$だが、仮定より${ f^{-1}( V ) }$は開集合、特に${ f^{-1}( V )\in\mathfrak{N}( x ) }$となる。故に${ f^{-1}( N )\in\mathfrak{N}( x ) }$だから${ f( f^{-1}( N ) )\subset N }$より${ N\in f_{\ast}\mathfrak{N}( x )\subset f_{\ast}\mathscr{F} }$が従う。${ \square }$

**定理**
${ X }$を収束空間、${ Y }$を位相空間とする。${ Y }$はtopological convergence structureで収束空間とみなす。${ f\colon X\rightarrow Y }$が収束空間としての同型を与えているなら、${ X }$はトポロジカルであり、${ f }$は同相写像となる。

（証明）${ \mathcal{O}_{Y} }$を${ Y }$の位相とする。必然的に

$$
\displaystyle \mathcal{O}_{X}:=\lbrace U\subset X : f( U )\in\mathcal{O}_{Y} \rbrace
$$

と置くしかない。${ f }$は全単射なので、これが${ X }$上の位相を定めることは明らかだろう。${ \mathscr{F}\rightarrow x }$と${ \mathfrak{N}( x )\subset\mathscr{F} }$が同値となることを示せば良い。

${ \mathscr{F}\rightarrow x }$とする。${ N\in\mathfrak{N}( x ) }$とすると、ある${ U\in\mathcal{O}_{X} }$が存在して${ x\in U\subset N }$が成り立つ。${ f( x )\in f( U )\subset f( N ) }$だが、${ f( U ) }$は開集合なので${ f( N )\in\mathfrak{N}( f( x ) ) }$である。ここで${ f }$は連続なので${ f( \mathscr{F} )\rightarrow f( x ) }$が成り立つ。よって${ \mathfrak{N}( f( x ) )\subset f( \mathscr{F} ) }$が成り立つ。つまり${ f( N )\in f( \mathscr{F} ) }$を得る。${ f }$は全単射だから${ N\in\mathscr{F} }$である。

${ \mathfrak{N}( x )\subset\mathscr{F} }$とする。${ \mathscr{F}\rightarrow x }$を示したい。${ f }$は同型なので${ f( \mathscr{F} )\rightarrow f( x ) }$を示せば良い。更に${ Y }$はトポロジカルだから${ \mathfrak{N}( f( x ) )\subset f( \mathscr{F} ) }$を示せばよい。${ N\in\mathfrak{N}( f( x ) ) }$とする。ある開集合${ V\in\mathcal{O}_{Y} }$が存在して${ f( x )\in V\subset N }$となる。従って${ x\in f^{-1}( V )\subset f^{-1}( N ) }$となる。定義より${ f^{-1}( V )\in\mathcal{O}_{X} }$だから、仮定より${ f^{-1}( N )\in\mathfrak{N}( x )\subset\mathscr{F} }$を得る。故に${ N=f( f^{-1}( N ) )\in f( \mathscr{F} ) }$が分かる。

${ f }$が同相写像となることは、前の補題より明らかだろう。${ \square }$
