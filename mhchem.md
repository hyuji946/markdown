#mhchem
$\require{mhchem}$

###準備
```
$\require{mhchem}$と記述するとmhchemが利用できるようになる。
$\ce{H2SO4 -> 2H+ + SO4^2-}$と書くと、
```

$\ce{H2SO4 -> 2H+ + SO4^2-}$

### 矢印

|コード|出力|
|:-----------:|:---------------:|
|`$\ce{A -> B}$`|$\ce{A -> B}$|
|`$\ce{A <- B}$`|$\ce{A <- B}$|
|`$\ce{A <-> B}$`|$\ce{A <-> B}$|
|`$\ce{A <=> B}$`|$\ce{A <=> B}$|
|`$\ce{A <=>> B}$`|$\ce{A <=>> B}$|
|`$\ce{A <<=> B}$`|$\ce{A <<=> B}$|

###矢印の上添え下添え(Cを付けると化学モード、Tでテキストモード)

|コード|出力|
|:-:|:-:|
|`$\ce{A->[H2O]B}$`|$\ce{A->[H2O]B}$|
|`$\ce{A->C[H2O]B}$`|$\ce{A->C[H2O]B}$|
|`$\ce{A->[up][down]B}$`|$\ce{A->[up][down]B}$|
|`$\ce{A->T[up][down]B}$`|$\ce{A->T[up][down]B}$|

###沈殿とガスの発生

|コード|出力|
|:-:|:-:|
|`$\ce{A->B^}$`|$\ce{A->B^}$|
|`$\ce{A->B v}$`|$\ce{A->B v}$|

###ギリシャ文字なども使えます。

|コード|出力|
|:-:|:-:|
|`$\ce{A ->[\alpha][\beta] B}$`|$\ce{A ->[\alpha][\beta] B}$|
|`$\ce{A->[\delta][\pi]B}$`|$\ce{A->[\delta][\pi]B}$|

###使用例

```
$$\ce{NH3 + H+ <=> NH4+}$$
$$\ce{A ->[h\nu] B}$$
$$\ce{2H2O2 ->C[MnO2] O2 ^ + 2H2O }$$
$$\ce{SO4^2- + Ba^2+ <=>> BaSO4 v}$$  
$$\ce{2CrO4^2- + 2H+ <=>C[H+][OH-] Cr2O7^2- + H2O }$$
```

$$\ce{NH3 + H+ <=> NH4+}$$  

$$\ce{A ->[h\nu] B}$$  

$$\ce{2H2O2 ->C[MnO2] O2 ^ + 2H2O }$$  

$$\ce{SO4^2- + Ba^2+ <=>> BaSO4 v}$$  

$$\ce{2CrO4^2- + 2H+ <=>C[H+][OH-] Cr2O7^2- + H2O }$$