### 2020/07/25 壁にぶつかるボールが円周率を作る

$m$は静止しており、$M$がぶつかってくる。左端には壁がある。
$m$は弾き飛ばされて壁と$M$に何度もぶつかる。

質量$m, M$の間に $\frac{M}{m} = 100^d, (d=0,1,2...)$ の関係がある時に、
衝突の回数が$314$のように、円周率の$d$桁になる。


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

ここで、

$ x=\frac{v}{\sqrt{m}} $

$ y=\frac{u}{\sqrt{M}} $ 

とすると、

$ \begin{pmatrix} x' \\\\ y' \end{pmatrix} = 
\frac{1}{M+m} \begin{pmatrix} M-m & 2 \sqrt{mM} \\\\ - 2 \sqrt{mM} & M-m \end{pmatrix} 
\begin{pmatrix} x \\\\ y \end{pmatrix} $


さらに、

$ \cos \theta = \frac{M-m}{M+m}$ 

$ \sin \theta = - 2 \frac{\sqrt{mM}}{M+m} $ 

とすると、

$ \frac{1}{M+m} 
\begin{pmatrix} M-m & 2 \sqrt{mM} \\\\ - 2 \sqrt{mM} &  M-m \end{pmatrix}  = 
\begin{pmatrix} \cos \theta & -\sin \theta \\\\ \sin \theta & \cos \theta \end{pmatrix}  $ 

と円周上の回転であることがわかる。$\theta$が$M,m$の一回の衝突での回転の角度であって、定数である。合計で$\pi$回転すればよい。
つまり$ 2\times \pi / \theta = 2\times\pi/\arccos{\frac{M-m}{M+m}} $が衝突回数全体ということになる。

