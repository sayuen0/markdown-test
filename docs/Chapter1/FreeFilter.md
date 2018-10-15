<!--
    自由フィルター
-->
## 自由フィルター
フレシェフィルター${ \mathcal{FC} }$とは、「補集合が有限集合となる部分集合」全体から成る無限集合のフィルターだった。フィルターが自身を含む超フィルターの共通部分として表せたように、フレシェフィルターも自由フィルターを用いて特徴付けることができる。

以下${ X }$は無限集合とする。また${ \mathcal{FC}\subset 2^{X} }$は${ X }$のフレシェフィルターとする。

**定義**
${ \mathscr{F}\subset 2^{X} }$を${ X }$のフィルターとする。

1. ${ \cap\mathscr{F}=\emptyset }$であるとき${ \mathscr{F} }$は自由（free）であるという。
2. ${ \cap\mathscr{F}\neq\emptyset }$であるとき${ \mathscr{F} }$は固定されている（fixed）という。

**命題**
${ \mathscr{G}\subset 2^{X} }$を${ X }$のフィルターとする。以下は同値である。

- ${ \mathscr{G} }$は自由である。
- ${ \mathcal{FC}\subset\mathscr{G} }$を満たす。

（証明）上から下を示す。${ F\in\mathcal{FC} }$について、${ X\setminus F=\lbrace x_{1}, \dotsc, x_{n} \rbrace }$と表せる。${ \cap\mathscr{G}=\emptyset }$より、各${ j }$についてある${ G_{j}\in\mathscr{G} }$が存在して${ x_{j}\notin G_{j} }$を満たす。${ x_{1}, \dotsc, x_{n}\notin G_{1}\cap\dotsb\cap G_{n} }$より${ G_{1}\cap\dotsb\cap G_{n}\subset F }$となるが、${ G_{1}\cap\dotsb\cap G_{n}\in\mathscr{G} }$より${ F\in\mathscr{G} }$を得る。

逆は、任意の${ x\in X }$について${ X\setminus\lbrace x \rbrace\in\mathcal{FC}\subset\mathscr{G} }$より${ \cap\mathscr{G}=\emptyset }$を得る。${ \square }$

- 特にフレシェフィルターは自由である。

**系**
極大な自由フィルターが存在する。

（証明）フレシェフィルターを含む超フィルターを取ればよい。${ \square }$

**定義**
部分集合の族${ \mathscr{S}\subset 2^{X}, \neq\emptyset }$は空でないとする。任意の${ S_{1}, \dotsc, S_{n}\in\mathscr{S} }$について${ S_{1}\cap\dotsb\cap S_{n}\neq\emptyset }$が成り立つとき（つまり任意の${ \mathscr{S} }$の有限交叉が空でないとき）、${ \mathscr{S} }$は有限交叉性（Finite Intersection Property, FIP）を満たすという。

有限交叉性はフィルター順基とも呼ばれる。実際、有限交叉全体${ \mathscr{B} }$はprefilterであり、特に${ \langle \mathscr{B} \rangle }$は${ \mathscr{S} }$を含む最小のフィルターとなる。この意味でフィルター的な定義としては最も弱い概念が有限交叉性である。

**命題**
部分集合の族${ \mathscr{S}\subset 2^{X}, \neq\emptyset }$は空でないとする。任意の${ \mathscr{S} }$の有限交叉は無限集合とする。このとき${ \mathscr{S} }$を含む極大自由フィルターが存在する。

（証明）${ \mathscr{S} }$は有限交叉性を満たすから、有限交叉全体${ \mathscr{B}:=\lbrace S_{1}\cap\dotsb\cap S_{n} : S_{j}\in\mathscr{S} \rbrace }$はprefilterである。${ F\in\mathcal{FC} }$及び${ S\in\mathscr{B} }$について${ F\cap S=\emptyset }$なら${ S\subset X\setminus S }$となり、${ S }$が無限集合であることに矛盾する。故に${ F\cap S\neq\emptyset }$である。すると${ \mathcal{FC} }$と${ \mathscr{B} }$のvel積を考えれば、フィルター${ \langle \mathcal{FC}\vee\mathscr{B} \rangle }$を含む超フィルター${ \mathscr{U} }$が取れる。${ \mathscr{U} }$はフレシェフィルターを含むので、自由である。${ \square }$

**定理**
フレシェフィルターは自由フィルターの共通部分と一致する。

（証明）自由フィルターの共通部分を${ \mathscr{E} }$とする。自由フィルターはフレシェフィルターを含むから${ \mathcal{FC}\subset\mathscr{E} }$が成り立つ。ある${ E\in\mathscr{E} }$が存在して${ E\notin\mathcal{FC} }$を満たすとする。${ \mathcal{FC}_{\setminus E}=\lbrace V : \exists F\in\mathcal{FC}, F\setminus E\subset V \rbrace }$は${ \mathcal{FC} }$を含むフィルターとなる。${ \mathcal{FC}_{\setminus E} }$を含む超フィルター${ \mathscr{U} }$を取れば、${ \mathcal{FC}\subset\mathcal{FC}_{\setminus E}\subset\mathscr{U} }$より${ \mathscr{U} }$は自由フィルターとなる。従って${ E\in\mathscr{E}\subset\mathscr{U} }$となるが、${ X\setminus E\in\mathcal{FC}_{\setminus E}\subset\mathscr{U} }$より矛盾する。${ \square }$

**系**
フレシェフィルターは極大自由フィルターの共通部分と一致する。

（証明）自由フィルターの共通部分を${ \mathscr{E} }$、極大自由フィルターの共通部分を${ \mathscr{F} }$とする。自由フィルターは、自身を含む超フィルターの共通部分である。これらの超フィルターは極大自由フィルターである。故に${ \mathscr{E}\supset\mathscr{F} }$である。逆に極大自由フィルターは自由フィルターなので${ \mathscr{E}\subset\mathscr{F} }$である。従って${ \mathcal{FC}=\mathscr{E}=\mathscr{F} }$である。${ \square }$