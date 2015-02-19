#mathjaxで数式の書き方。
```
MathJax はMathML、LaTeX、ASCIIMathML（英語版）で記述された数式を
ウェブブラウザ上で表示するクロスブラウザ（英語版）のJavaScriptライブラリである。
MathJaxはApache Licenseのもとでオープンソースソフトウェアとしてリリースされている。
先行のJavaScript数式フォーマットライブラリのjsMath（英語版）の後継として
MathJaxプロジェクトは2009年に開始し、アメリカ数学会によって管理されている。
~~wikipediaより
```
Latexで書かれた数式をブラウザで表示出来る。
例えば`$\LaTeX$`と書くと$\LaTeX$になる。  
$\alpha\beta\pi$などのよく使うギリシャっ文字などが綺麗に表示できる。

|     $\LaTeX$    |    display    |   |   $\LaTeX$  |  display  |
|-----------------|:-------------:|---|-------------|:---------:|
| `$\alpha$`      | $\alpha$      |   | `$\theta$`  | $\theta$  |
| `$\beta$`       | $\beta$       |   | `$\eta$`    | $\eta$    |
| `$\gamma$`      | $\gamma$      |   | `$\lambda$` | $\lambda$ |
| `$\delta$`      | $\delta$      |   | `$\mu$`     | $\mu$     |
| `$\epsilon$`    | $\epsilon$    |   | `$\nu$`     | $\nu$     |
| `$\varepsilon$` | $\varepsilon$ |   | `$\pi$`     | $\pi$     |

|  $\LaTeX$  | display  |   |      $\LaTeX$     |     display     |
|------------|:--------:|---|-------------------|:---------------:|
| `$\times$` | $\times$ |   | `$\pm$  $\mp$`    | $\pm$  $\mp$    |
| `$\div$`   | $\div$   |   | `$\leq$ $\geq$`   | $\leq$ $\geq$   |
| `$\dots$`  | $\dots$  |   | `$\equiv$`        | $\equiv$        |
| `$\cdots$` | $\cdots$ |   | `$\sim$ $\simeq$` | $\sim$ $\simeq$ |
| `$\ldots$` | $\ldots$ |   | `$\ll$ $\gg$`     | $\ll$ $\gg$     |
| `$\neq$`   | $\neq$   |   | `$\quad \qquad$`  | 空白            |

日本でよく使う￥≒　≦　∴はない、全角を使う。

| $\LaTeX$                  | display                 |     | $\LaTeX$                  | display                 |
| ------------------------- | :---------------------: | --- | ------------------------- | :---------------------: |
| `$\sum$`                  | $\sum$                  |     | `$\int$`                  | $\int$                  |
| `$\sum_{a}^{b}$`          | $\sum_{a}^{b}$          |     | `$\int_{a}^{b}$`          | $\int_{a}^{b}$          |
| `$\sum\limits_{a}^{b}$`   | $\sum\limits_{a}^{b}$   |     | `$\int\limits_{a}^{b}$`   | $\int\limits_{a}^{b}$   |


###複数行の数式
####Align
番号が付く＆で位置合わせ。
```
$
\begin{align}
y&=(x-1)(x+1)\\
&=x^2-1
\end{align}
$

```
$
\begin{align}
y&=(x-1)(x+1)\\
&=x^2-1
\end{align}
$

`align*`で番号なし
```
$
\begin{align*}
y&=(x-1)(x+1)\\
&=x^2-1
\end{align*}
$

```

$
\begin{align*}
y&=(x-1)(x+1)\\
&=x^2-1
\end{align*}
$

何故か左寄せになるけど、これだと中央揃え
```
$$
\begin{align*}
y&=(x-1)(x+1)\\
&=x^2-1
\end{align*}
$$
```
$$
\begin{align*}
y&=(x-1)(x+1)\\
&=x^2-1
\end{align*}
$$

一部分番号をつけないようにするにはnotagを付ける。
```
$
\begin{align}
y&=(x-1)(x+1)  \notag \\
&=x^2-1
\end{align}
$

```
$
\begin{align}
y&=(x-1)(x+1)  \notag \\
&=x^2-1
\end{align}
$

tagを使用して独自に番号を付ける事ができる。
```
$
\begin{align}
x+y=1  \tag{a}\\
A+B=0  \tag{式１}\\
C+D=0
\end{align}
$

```
$
\begin{align}
x+y=1  \tag{a}\\
A+B=0  \tag{式１}\\
C+D=0
\end{align}
$


###大きなカッコleft,rightや分数fracなど
```
$
\begin{align*}
\left( \frac12  \right)\\
\left[ \frac{a}{b}  \right]\\
\left\{ \frac23  \right\}
\end{align*}
$
　｛は＼が必要になる　．を使うと半分省略
$
\begin{align*}
\left. \frac{1/2}{\frac{2}{\pi}}  \right)\\
\left[ \frac12  \right.\\
\left< \frac12  \right>
\end{align*}
$
```
$
\begin{align*}
\left( \frac12  \right)\\
\left[ \frac{a}{b}  \right]\\
\left\{ \frac23  \right\}
\end{align*}
$
　｛は＼が必要になる　．を使うと半分省略
$
\begin{align*}
\left. \frac{1/2}{\frac{2}{\pi}}  \right)\\
\left[ \frac12  \right.\\
\left< \frac12  \right>
\end{align*}
$

###条件などはcases文を使う


```
$
\begin{cases}
x\neq 0の時\\
y=1/x
\end{cases}
$
```

$
\begin{cases}
x\neq 0の時\\
y=1/x
\end{cases}
$

###簡単な表はarray文で、c中央合わせ、l左合わせ、r右あわせ
```
$
\begin{array}{clr}
\hline
abc&de&fgh\\
\hline
1&234&56\\
中央&左&右\\
\hline
\end{array}
$
```
$
\begin{array}{clr}
\hline
abc&de&fgh\\
\hline
1&234&56\\
中央&左&右\\
\hline
\end{array}
$

縦の線の入れ方
```
$
\begin{array}{|c|lr|}
\hline
abc&de&fgh\\
\hline
1&234&56\\
中央&左&右\\
\hline
\end{array}
$
```
$
\begin{array}{|c|lr|}
\hline
abc&de&fgh\\
\hline
1&234&56\\
中央&左&右\\
\hline
\end{array}
$

###color文による色指定
```
$\color{red}{赤} \color{green}{緑} \color{blue}{青} $

$
\frac{2}{3}+\frac{1}{2}
=\frac{2\times\color{green}{2}}{3\times\color{green}{2}}
+\frac{1\times\color{blue}{3}}{2\times\color{blue}{3}}
=\frac{4+3}{6}=\frac{7}{6}=1\frac{1}{6}
$
```
$\color{red}{赤} \color{green}{緑} \color{blue}{青} $

$
\frac{2}{3}+\frac{1}{2}
=\frac{2\times\color{green}{2}}{3\times\color{green}{2}}
+\frac{1\times\color{blue}{3}}{2\times\color{blue}{3}}
=\frac{4+3}{6}=\frac{7}{6}=1\frac{1}{6}
$
