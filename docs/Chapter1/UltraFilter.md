<!--
    超フィルター
-->
## 超フィルター
既にフィルター全体が包含に関して順序構造を持つことを見た。このとき与えられた2つのフィルターについて、下限は常に存在するが、上限は必ずしも定義されない。この事実から、大きなフィルターには特別な意味があると推察できる。

**定義**
包含順序に関して極大なフィルターを超フィルター（ultra filter）と呼ぶ。

**例**
点フィルターは超フィルターである。実際フィルター${ \mathscr{F}\subset 2^{X} }$について${ \langle x \rangle\subset\mathscr{F} }$とする。${ F\in\mathscr{F} }$について${ x\notin\mathscr{F} }$なら${ F\cap\lbrace x \rbrace=\emptyset\in\mathscr{F} }$となり矛盾する。従って${ x\in F }$が常に成り立つ。

**定理**
任意のフィルター${ \mathscr{F}\subset 2^{X} }$について、${ \mathscr{F} }$を含む超フィルターが存在する。

（証明）${ X }$のフィルター全体を${ \Phi( X ) }$とする。${ \Psi:=\lbrace \mathscr{G}\in\Phi( X ) : \mathscr{F}\subset\mathscr{G} \rbrace }$の全順序部分集合${ \tau }$を取れば、${ \bigcup_{\mathscr{A}\in\tau}\mathscr{A} }$はフィルターであり、更に${ \tau }$の${ \Psi }$における上界を与えている。故に${ \Psi }$は帰納的であり、Zornの補題より極大元${ \mathscr{U} }$を持つ。これは${ \mathscr{F} }$を含む超フィルターである。${ \square }$

超フィルターは次の特徴付けを持つ。

**補題**
${ \mathscr{U}\subset 2^{X} }$をフィルターとする。以下は同値である。

- ${ \mathscr{U} }$は超フィルターである。
- 任意の${ A\subset X }$について${ A\in\mathscr{U} }$または${ X\setminus A\in\mathscr{U} }$が成り立つ。

（証明）右を仮定しよう。${ \mathscr{U}\subsetneq\mathscr{V} }$とすると、ある${ V\in\mathscr{V}\setminus\mathscr{U} }$が存在する。すると仮定より${ X\setminus V\in\mathscr{U}\subset\mathscr{V} }$となる。${ V, X\setminus V\in\mathscr{V} }$となるがこれは${ \mathscr{V} }$がフィルターであることに矛盾する。

逆に左を仮定しよう。${ A\notin\mathscr{U} }$について、${ \mathscr{U}_{\setminus A}=\lbrace V : \exists U\in\mathscr{U}, U\setminus A\subset V \rbrace }$は${ \mathscr{U} }$を含むフィルターである。ここで${ X\setminus A\in\mathscr{U}_{\setminus A} }$となるが、極大性より${ \mathscr{U}_{\setminus A}=\mathscr{U} }$である。故に${ X\setminus A\in\mathscr{U} }$である。${ \square }$

この特徴付けを用いて、超フィルターに関するいくつかの性質を導いておく。

**命題**
${ \mathscr{U}\subset 2^{X} }$を超フィルターとする。${ S_{1}, \dotsc, S_{n}\subset X }$について${ S_{1}\cup\dotsb\cup S_{n}\in\mathscr{U} }$なら、ある${ j }$について${ S_{j}\in\mathscr{U} }$が成り立つ。

（証明）${ n }$に関する帰納法で示す。${ n=2 }$のとき、${ S_{1}, S_{2}\notin\mathscr{U} }$とする。特徴付けより${ X\setminus S_{1}, X\setminus S_{2}\in\mathscr{U} }$である。しかし${ X\setminus( S_{1}\cup S_{2} )=( X\setminus S_{1} )\cap( X\setminus S_{2} )\in\mathscr{U} }$より、${ S_{1}\cup S_{2}\notin\mathscr{U} }$でなければならない。これは矛盾である。

${ n=k+1 }$のとき、${ ( S_{1}\cup\dotsb\cup S_{k} )\cup S_{k+1}\in\mathscr{U} }$とする。${ S_{k+1}\notin\mathscr{U} }$なら${ n=2 }$とみなして${ S_{1}\cup\dotsb\cup S_{k}\in\mathscr{U} }$である。仮定より、ある${ 1\le j\le k }$について${ S_{j}\in\mathscr{U} }$が従う。${ \square }$

**命題**
${ \mathscr{U}_{1}, \dotsc, \mathscr{U}_{n}\subset 2^{X} }$を超フィルターとする。超フィルター${ \mathscr{V}\subset 2^{X} }$について${ \mathscr{U}_{1}\cup\dotsb\cup\mathscr{U}_{n}\subset\mathscr{V} }$なら、ある${ j }$について${ \mathscr{V}=\mathscr{U}_{j} }$が成り立つ。

（証明）任意の${ j }$について${ \mathscr{U}_{j}\neq\mathscr{V} }$であるとしよう。${ \mathscr{U}_{j} }$の極大性より${ \mathscr{U}_{j}\subsetneq\mathscr{V} }$であるから、ある${ U_{j}\in\mathscr{U}_{j}\setminus\mathscr{V} }$が存在する。${ \mathscr{V} }$は超フィルターだから${ X\setminus U_{j}\in\mathscr{V} }$である。${ X\setminus( \bigcup_{k=1}^{n}U_{k} )=\bigcap_{k=1}^{n}( X\setminus U_{k} )\in\mathscr{V} }$だから${ \bigcup_{k=1}^{n}U_{k}\notin\mathscr{V} }$となる。ところが${ U_{j}\subset\bigcup_{k=1}^{n}U_{k} }$より${ \bigcup_{k=1}^{n}U_{k}\in\mathscr{U}_{j} }$であり、従って${ \bigcup_{k=1}^{n}U_{k}\in\mathscr{U}_{1}\cap\dotsb\cap\mathscr{U}_{n}\subset\mathscr{V} }$を得る。これは矛盾である。${ \square }$

例でも示したが点フィルターは超フィルターであった。逆に超フィルターは有限集合を要素とするなら点フィルターである。

**命題**
超フィルターが有限集合を要素とするなら、それは点フィルターである。

（証明）${ \mathscr{U}\subset 2^{X} }$を超フィルターとする。${ F\in\mathscr{U} }$を元の個数が最小の有限集合とする。任意の${ G\subsetneq F }$について${ G\notin\mathscr{U} }$であるから、${ \mathscr{U}_{\setminus G}=\lbrace V : \exists U\in\mathscr{U}, U\setminus G\subset V \rbrace }$は${ \mathscr{U} }$を含むフィルターとなる。極大性より${ \mathscr{U}=\mathscr{U}_{\setminus G} }$だが、特に${ F\in\mathscr{U} }$より${ F\setminus G\in\mathscr{U}_{\setminus G}=\mathscr{U} }$となる。しかし${ F }$の最小性より${ G=\emptyset }$でなければならず、そのためには${ F }$の要素は1つでなければならない。点フィルターは超フィルターであるから、${ \langle F \rangle=\mathscr{U} }$が従う。${ \square }$

**系**
${ X }$が有限集合のとき、以下が成り立つ。

1. 超フィルターは点フィルターである。
2. フィルターは単項フィルターである。

（証明）1つ目は上の命題より明らか。2つ目は、フィルター${ \mathscr{F}\subset 2^{X} }$に対し、元の個数が最小の要素を${ F\in\mathscr{F} }$とする。${ G\in\mathscr{F} }$について${ F\cap G\in\mathscr{F} }$だから、最小性より${ F\subset G }$が従う。故に${ \mathscr{F}=\langle F \rangle }$である。${ \square }$

系の観察が重要な性質を示唆してくれる。単項フィルター${ \langle F \rangle }$について${ F=\lbrace x_{1}, \dotsc, x_{n} \rbrace }$とすれば、${ \langle F \rangle=\langle x_{1} \rangle\cap\dotsb\cap\langle x_{n} \rangle }$が成り立つ。${ X }$が有限集合のとき、任意のフィルターは単項フィルターで表せるが、その要素の点フィルターは超フィルターであって、更に共通部分が元のフィルターと一致する。この事実は任意の集合上でも成り立つ。

**定理**
${ \mathscr{F}\subset 2^{X} }$をフィルターとする。このとき${ \mathscr{F} }$は${ \mathscr{F} }$を含む超フィルターの共通部分と一致する。

（証明）${ \mathscr{F} }$を含む超フィルターの共通部分を${ \Upsilon }$とする。定義より${ \mathscr{F}\subset\Upsilon }$は明らかなので、逆を示そう。${ \mathscr{F}\subsetneq\Upsilon }$とすれば、ある${ U\in\Upsilon\setminus\mathscr{F} }$が存在する。このとき${ \mathscr{F}_{\setminus U}=\lbrace V : \exists F\in\mathscr{F}, F\setminus U\subset V \rbrace }$は${ \mathscr{F} }$を含むフィルターとなる。さて、${ \mathscr{U}_{\setminus U} }$を含む超フィルターが存在するから、その1つを${ \mathscr{V} }$としよう。このとき${ \mathscr{F}\subset\mathscr{F}_{\setminus U}\subset\mathscr{V} }$より、${ \mathscr{V}\in\Upsilon }$である。${ X\setminus U\in\mathscr{F}_{\setminus U}\subset\mathscr{V} }$だが${ U\in\Upsilon\subset\mathscr{V} }$より矛盾する。${ \square }$

最後にpush-forwardと超フィルターの関係について述べよう。

**命題**
${ f\colon X\rightarrow Y }$を写像とする。${ \mathscr{U}\subset 2^{X} }$を${ X }$の超フィルターとすると、${ f_{\ast}\mathscr{U}\subset 2^{Y} }$は${ Y }$の超フィルターである。

（証明）${ W\notin f_{\ast}\mathscr{U} }$とする。${ f^{-1}( W )\in\mathscr{U} }$なら${ f( f^{-1}( W ) )\subset W }$より${ W\in\langle f( \mathscr{U} ) \rangle=f_{\ast}\mathscr{U} }$となり矛盾する。故に${ f^{-1}( W )\notin\mathscr{U} }$だから特徴付けより${ X\setminus f^{-1}( W )\in\mathscr{U} }$が従う。${ f( X\setminus f^{-1}( W ) )\subset Y\setminus W }$より${ Y\setminus W\in\langle f( \mathscr{U} ) \rangle=f_{\ast}\mathscr{U} }$を得る。${ \square }$

**命題**
${ f\colon X\rightarrow Y }$を写像とする。${ \mathscr{F}\subset 2^{X} }$を${ X }$のフィルターとする。${ f_{\ast}\mathscr{F} }$を含む${ Y }$の超フィルター${ \mathscr{V}\subset 2^{Y} }$について、ある${ X }$の超フィルター${ \mathscr{U}\subset 2^{X} }$が存在して、${ \mathscr{U} }$は${ \mathscr{F} }$を含み、${ f_{\ast}\mathscr{U}=\mathscr{V} }$を満たす。

（証明）直観的には${ \mathscr{F} }$と${ f^{\ast}\mathscr{V} }$を含む超フィルターを取ればよい。まずはpull-backが定義できることを示そう。${ V\in\mathscr{V} }$とする。${ f( X )\subset Y\setminus V }$なら${ Y\setminus V\in f_{\ast}\mathscr{F}\subset\mathscr{V} }$より矛盾する。よって${ f^{-1}( V )\neq\emptyset }$である。次に${ \mathscr{F}\vee f^{\ast}\mathscr{V} }$を考えるため、交叉の条件を見る。prefilterのvel積は生成と可換だったので、${ F\in\mathscr{F} }$及び${ V\in\mathscr{V} }$について${ F\cap f^{-1}( V )\neq\emptyset }$であることを示せば良い。実際${ f( F )\cap V=\emptyset }$なら${ f( F )\subset Y\setminus V }$となり、先ほどと同様に${ Y\setminus V\in\mathscr{V} }$となって矛盾する。以上より、${ \mathscr{F} }$と${ f^{\ast}\mathscr{V} }$を含むフィルターを構成することができた。後はこれを含む超フィルター${ \mathscr{U} }$を取ればよい。このとき${ \mathscr{F}\subset\mathscr{U} }$であり、${ \mathscr{V}\subset f_{\ast}( f^{\ast}\mathscr{V} )\subset f_{\ast}\mathscr{U} }$と極大性より${ \mathscr{V}=f_{\ast}\mathscr{U} }$が従う。${ \square }$