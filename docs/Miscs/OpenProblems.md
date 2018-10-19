## 未解決問題集
ノートを書いていて疑問に思ったけど解決できなかったもの、考えていないもの、後で考える予定のものを置いておきます。何かあったら[マストドンの私のアカウント](https://mathtod.online/@mathmathniconico)までご連絡下さい。GitHub上でもいいです。

**問題1（Easy）**
${ f\colon X\rightarrow Y }$を収束空間の間の写像とする。以下の関係を調べよ。

- ${ C }$：${ f }$は連続である。
- ${ To }$：${ U\subset Y }$がopenなら${ f^{-1}( U ) }$はopenである。
- ${ Tc }$：${ F\subset Y }$がclosedなら${ f^{-1}( F ) }$はclosedである。
- ${ N }$：${ x\in X }$について、${ N\subset Y }$が${ f( x ) }$の近傍なら${ f^{-1}( N ) }$は${ x }$の近傍である。
- ${ A }$：${ A\subset X }$について${ f( \mathrm{cl}( A ) )\subset\mathrm{cl}( f( A ) ) }$が成り立つ。

（解説）${ To\Leftrightarrow Tc }$なので${ T }$とする。

- ${ C\Rightarrow T, N, A }$である。
- ${ N\Rightarrow T }$である。
- ${ A\Rightarrow T }$である。
- ${ X, Y }$がトポロジカルなら全て同値となる。
- ${ Y }$がプレトポなら${ N\Rightarrow C }$である。

まとめると

| ${ X }$ | ${ Y }$ | ${ T\Rightarrow C }$ | ${ A\Rightarrow C }$ | ${ N\Rightarrow C }$ | ${ T\Rightarrow A }$ | ${ T\Rightarrow N }$ |
|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
| top | top | 真 | 真 | 真 | 真 | 真 |
| conv | pretop | ？ | ？ | 真 | ？ | ？ |

反例が知りたい。${ \heartsuit }$

