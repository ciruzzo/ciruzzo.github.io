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

$\left( \begin{matrix} v' \\ u' \end{matrix} \right) = 
\frac{1}{M+m} 
\left( \begin{matrix} M-m & 2 m \\ - 2 M & M-m \end{matrix} \right)
\left( \begin{matrix} v \\ u \end{matrix} \right) $

$ \cos \theta = \frac{M-m}{M+m}$ 

$ \sin \theta = - 2 \frac{\sqrt{mM}}{M+m} $ 

とすると、

$ \frac{1}{M+m} 
\left( \begin{matrix} M-m & 2 \sqrt{mM} \\ - 2 \sqrt{mM} &  M-m \end{matrix} \right) = 
\left( \begin{matrix} \cos \theta & -\sin \theta \\ \sin \theta & \cos \theta \end{matrix} \right) $ 
