### 2020/07/27 フレッツ光とipv6＆電話加入権の休止表


銅線のBフレッツ VSDL 100Mbps→光ファイバのフレッツ光ギガマンションと変更したが、
あまり速くならなかったので（20Mbpsかそこら）、ipv6を通してもらったところ10倍速くなった。
やったのはNTTのNGN ipv6の接続依頼と、プロバイダであるNIFTYに連絡するだけ。費用かからず。
Wi-Fiルータはipv6非対応だがv6がパススルー設定になっているので、通ってしまうらしい（別に良いことではない）。


フレッツ光ギガマンションにしたのをきっかけに、固定電話をひかり電話に変更した。
これで昔の「[電話加入権](https://ja.wikipedia.org/wiki/%E9%9B%BB%E8%A9%B1%E5%8A%A0%E5%85%A5%E6%A8%A9)」は必要なくなり、郵送で「休止表」と
10年後に権利が消滅するというお知らせが来た。


両方あわせて月々の料金は少し安くなる方向。

### 2020/07/26 HTMLのID属性をMarkdownで書く

Markdownで同じページ内のリンク(id)を作るやり方。

[壁にぶつかるボールが円周率を作る](#ballwallpi)


### 2020/07/25 GitHub Pagesを使ってみる

Markdownで書けるのっていいなと思って使い始めた。2か月くらい前にgithubの設定はしてあった。まったく覚えていなかった。最初に見たのはどこだったか忘れたけれど、

[GitHub Pages を使ってみる](https://docs.github.com/ja/github/working-with-github-pages)

数式を書きたかったので、ここを読んでv2の設定をまるまる写した。

[Github Pages で数式を ～ MathJax v3 設定のポイント](https://qiita.com/memakura/items/e4d2de379f98ad7be498)

Google Search Consoleにこのページは登録したが、sitemapは作っていない。これで様子を見よう。

### 2020/07/25 壁にぶつかるボールが円周率を作る {#ballwallpi}

$m$は静止しており、右から$M$がぶつかってくる。左端には壁がある。
$m$は弾き飛ばされて壁と$M$に何度もぶつかる。$M$はやがて押し戻されて右に戻って行く。この衝突回数が円周率と関係あるという話。


>質量$m, M$の間に $\frac{M}{m} = 100^d, (d=0,1,2...)$ の関係がある時に、衝突の回数が円周率の上位$d$桁になる。（例：$d=3$, $314$）


$M, m$それぞれの速度と衝突後の速度を$v, u$、$v’, u’$とし、エネルギー保存の法則と、運動量保存の法則から
 
$ \frac{1}{2} Mv^2 + \frac{1}{2} 
mu^2 = \frac{1}{2} Mv’^2 + \frac{1}{2} mu’^2 $ 

$ Mv + mu = Mv’ + mu’$ 

となる。壁の方が正の方向である。
これを解くと、以下のようになる。 

$\begin{pmatrix} v' \\\\ u' \end{pmatrix} = 
\frac{1}{M+m} 
\begin{pmatrix} M-m & 2 m \\\\ - 2 M & M-m \end{pmatrix} 
\begin{pmatrix} v \\\\ u \end{pmatrix}  $

（衝突直後の$u'$の符号はこれと逆だが、壁に当たって逆向きになった後のものとして表現している。）

ここで、

$ x=\frac{v}{\sqrt{m}} $、$ y=\frac{u}{\sqrt{M}} $ 

と変数の置き換えをすると、

$ \begin{pmatrix} x' \\\\ y' \end{pmatrix} = 
\frac{1}{M+m} \begin{pmatrix} M-m & 2 \sqrt{mM} \\\\ - 2 \sqrt{mM} & M-m \end{pmatrix} 
\begin{pmatrix} x \\\\ y \end{pmatrix} $


さらに、

$ \cos \theta = \frac{M-m}{M+m}$ 、$ \sin \theta = - 2 \frac{\sqrt{mM}}{M+m} $ 

とすると、

$ \frac{1}{M+m} 
\begin{pmatrix} M-m & 2 \sqrt{mM} \\\\ - 2 \sqrt{mM} &  M-m \end{pmatrix}  = 
\begin{pmatrix} \cos \theta & -\sin \theta \\\\ \sin \theta & \cos \theta \end{pmatrix}  $ 

と円周上の回転であることがわかる。

$x=1, y=0$から$x=0, y=-1$を通過し、$x=-1,y=0$に進んで壁との衝突は終了する。


$\theta$が$M,m$の一回の衝突での回転の角度であって、上の置き換えを見て分かるように定数である。合計で$\pi$回転することになる。また、同じ回数の壁との衝突があるのでその2倍、
つまり$ 2\pi / \theta = 2\pi/\arccos{\frac{M-m}{M+m}} $が衝突回数全体ということになる。


元に戻って、$\frac{M}{m} = 100^d$ということから、

$2/arccos{\frac{100^d-1}{100^d-1}} \approx 10^d$なので、例えば$d=5$の場合$314159$となる。ということで円周率の$d$桁が出てきた。

