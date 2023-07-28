### 关于 Lie 群, 量子群, 晶体基等的历史事件综述. 

#### Part I  Lie 群的一致正定性理论

**简介** 一致正定性研究一列关联对象的正定性关系, 具体应用如编码理论, 统计, 生成矩阵分解算法及不等式等. 

(1930s-, Gantmacher, Krein, and Schoenberg 等人为主的老派) 矩阵的一致正定性, 如行列式中非负子式之和等. 如正项 Vandermonde 矩阵中子方阵行列均非负, $G_{2,4}$​ 型 Grassmannian 的 Plücker 坐标 满足形如 Ptolemy 定理的恒等式
$$
\Delta_{12,12}\Delta_{12,34}+\Delta_{12,14}\Delta_{12,23}=\Delta_{12,13}\Delta_{12,24}.
$$
即后文所见的 A_2 型丛代数. 

* (1994, Lusztig) 于 [[Luz93]](https://link.springer.com/chapter/10.1007/978-1-4612-0261-5_20) 提出研究一般代数群中的一致正定性. 主要是 Lie 群 $G$ 中的某一幂幺根 $N_\pm $ 的正定部分, 记做 $G_{\geq0}\cap N_\pm$. 例如典型群 $\mathrm{SL}(3,\mathbb R)$ 中 
  $$
  N=\left\{\begin{pmatrix}1&\ast&\ast\\&1&\ast\\&&1\end{pmatrix}\right\}
  $$
  的一致正定性 $\Delta_{1,2}$, $\Delta_{1,3}$, $\Delta_{2,3}$, $\Delta_{12,23}$. 满足 $A_2$ 型丛代数关系 
  $$
  \Delta_{12,23}+\Delta_{1,3}=\Delta_{1,2}\Delta_{2,3}.
  $$

* (Bruhat 2-胞腔分解的一致正定性理论) Bruhat 胞腔即 Lie 群以 Weyl 群元素的为指标的分解, 对有限域上的 Lie 理论与组合学极有作用, 早期工作如 [[Iwa65]](http://www.numdam.org/item/PMIHES_1965__25__5_0.pdf). 

**例子** $\mathrm{SL}(2,\mathbb C)$ ($A_2$ 型 Lie 群)的丛代数结构.

Lie 理论汇总

* $G$ 为单连通半单复 Lie 群, $B_\pm$ 为 Borel 子群, $N_\pm$ 为相应的幂幺根, $H$ 为极大环面.  $G$ 中具有 Gauss 分解的元素 $x=[x]_-[x]_0[x]_+$ 构成开集 $G_0=N_-HN$. 

* 记 $G$ 对应的 Lie 代数为 $\mathfrak g:=\mathrm{Lie\,} G$, 则 $\mathfrak h:=\mathrm{Lie\,}H$ 为 Cartan 子代数. 记 $\Phi\subseteq \mathrm{Hom}_{\mathbb C}(\mathfrak h,\mathbb C)\setminus\{0\}$ 为根系, 则有分解
  $$
  \mathfrak g=\mathfrak h\oplus \bigoplus _{\alpha\in \Phi}\mathfrak g_\alpha.
  $$
  记 $\Pi=\{\alpha_1,\ldots, \alpha_r\}\subseteq \Phi$ 为单根, 此处 $r$ 为 Lie 群的秩. 取 $\{\alpha_i^\vee\}_{i=1}^r\subseteq \mathfrak h$ 为单余根, 记 $C=(c_{i,j})_{r\times r}$ 为 Cartan 矩阵, 其中 $c_{i,j}:=\left<\alpha_i^\vee,\alpha_j\right>:=\alpha_j(\alpha_i^\vee)$. 

* 对 $\alpha_i\in \Pi$, 总有 $\dim\mathfrak g_{\alpha_i}=1$, 从而 $\langle \mathfrak g_{\pm\alpha_i}\rangle$ 生成同构于 $\mathfrak{sl}(2,\mathbb C)$ 的 Lie 子代数. 记 Lie 代数嵌入同态 $\iota_i:\langle \mathfrak g_{\pm\alpha_i}\rangle\hookrightarrow \mathfrak g$ 对应 Lie 群间同态 $\phi_i:\mathrm{SL}(2,\mathbb C)\to G$, 即交换图

  <img src="C:\Users\czhan\AppData\Roaming\Typora\typora-user-images\image-20230326165734896.png" alt="image-20230326165734896" style="zoom: 20%;" />

  记单参数子群
  $$
  \begin{align*}
  x_i(t)&=\exp(e_it)=\phi_i\begin{pmatrix}1&t\\0&1\end{pmatrix}\in N,\\
  x_{- i}(t)&=\exp(f_it)=\phi_i\begin{pmatrix}1&0\\t&1\end{pmatrix}\in N_-,\\
  h_{i}(t)&=\exp(h_it)=\phi_i\begin{pmatrix}t&0\\0&t^{-1}\end{pmatrix}\in H.
  \end{align*}
  $$

* 记 Weyl 群为 $\mathrm{span}_{\mathbb Z}(\Phi)$ 之自同构群的子群, 其生成元为一切垂直于 $\alpha_i$ 的反射 $s_i$, 此处 $\alpha_i\in \Pi$ 为任意单根. 另一方面, 可视 $W:=\mathrm{Norm}_G(H)/H$. 即, 
  $$
  s_i=\overline{s_i}H,\quad \overline{s_i}:=\phi_i\begin{pmatrix}0&-1\\1&0\end{pmatrix}\in \mathrm{Norm}_G(H). 
  $$
  任取 $ w\in W$, 规定其长度为表示自身所需的最小反射数量, 记 
  $$
  \ell( w):=\min \{k\mid{s_{i_1}}\cdots {s_{i_k}}=w\}\in\mathbb N.
  $$

* 记 $\dot\cup$ 为无交并. $G$​ 有 Bruhat 胞腔分解
  $$
  G=\dot\bigcup_{ w\in W}B wB=\dot\bigcup_{ w\in W}B_- wB_-.
  $$
  任取 $u,v\in W$, 记 $G^{u,v}=BuB\cap B_-vB_-$, 则有 Bruhat 双胞腔分解
  $$
  G=\dot\bigcup_{u,v\in W}G^{u,v}.
  $$

$\mathrm{SL}(n,\mathbb C)$ 中 Bruhat 双胞腔 $G^{u,v}$ 的丛代数结构由以下算法给出. 

1. 以 $S_3\simeq W=\left<s_1,s_2\mid s_1^2=s_2^2=(s_1s_2)^3\right>$ ($r=2$) 为例. 

2. 令 $u=\prod_{k}s_{i_k}$, $v=\prod_ls_{j_l}$. 定义字
   $$
   \vec i=[-r,\ldots,-1, i_1,\ldots, i_{\ell(u)},-j_1,\ldots ,-j_{-\ell(v)}].
   $$
   为使得模型不过于简单, 此处不妨取 $u,v$ 为最长字 $w_0=s_1s_2s_1$. 即 $u=s_1s_2s_1$, $v=s_{-1}s_{-2}s_{-1}$, $r=2$, 得
   $$
   \vec i=[-r\cdots -1]\cdot u\cdot v=[-2,-1,1,2,1,-1,-2,-1].
   $$

3. 将 $\vec i$ 中字体标序为 $-2,-1,1,\ldots,6$. 定义 $k^+$ 使得 $|s_{k^+}|=|s_k|$ 的最小后继序数(若不存在, 则记作 $\ell(u)+\ell(v)+1=7$).  

4. 下复原丛代数对应的箭图 $Q$. 此处 $\vec i$ 的长度 $m=\ell(u)+\ell(v)+2$ 为箭图中的顶点总数, $u$ 与 $v$ 中包含的字元数(区分符号)为冻结顶点数. 此处 $|Q_0|=8$, 冻结顶点数为 $4$, 从而可迁顶点数为 $4$. 其中, 可迁顶点对应
   $$
   \{1\leq k\leq \ell(u)+\ell(v)\mid k^+\leq \ell(u)+\ell(v)\}.
   $$
   对 $\mathrm{SL}(3,\mathbb C)$ 而言, 可迁点为 $\{1,2,3,4\}$. 现定义 $k<l$ 的连边为(不考虑冻结点间的边)

   * 若 $k^+=l$, 则 $k$ 与 $l$ 间连横向边. 方向由 $s_l$ 符号决定, 即 $\underset k\circ\to \underset l\oplus$ 或 $\underset k\circ \leftarrow \underset l\ominus$.
   * 若同时有 (1) $l<k^+<l^+$; (2) $c_{|i_k|,|i_l|}\neq 0$, $i_l\cdot i_{k^+}>0$, 则连斜向边. 方向为 $\underset l\circ \to \underset {k^+}\ominus \quad\underset{l^+}\ominus$ 或 $\underset l\circ \leftarrow \underset{k^+}\oplus \quad \underset{l^+}\oplus$, 数量为 $\max(-c_{|i_k|,|i_l|},1)$.
   *  若同时有 (1) $l<l^+<k^+$; (2) $c_{|i_k|,|i_l|}\neq 0$, $i_l\cdot i_{l^+}<0$, 则连斜向边. 方向为 $\underset l\circ \to \underset {l^+}\ominus \quad\underset{k^+}\oplus$ 或 $\underset l\circ \leftarrow \underset{l^+}\oplus \quad \underset{k^+}\ominus$, 数量为 $\max(-c_{|i_k|,|i_l|},1)$.

   <img src="C:\Users\czhan\AppData\Roaming\Typora\typora-user-images\image-20230327215346501.png" alt="image-20230327215346501" style="zoom:25%;" />

   对应的转移矩阵为
   $$
   \begin{matrix}
   \\-2&\mid\\-1&\mid\\1&\mid\\2&\mid\\3&\mid\\4&\mid\\5&\mid\\6&\mid
   \end{matrix}
   \begin{matrix}
   \underline 1&\underline 2&\underline 3&\underline 4\\1&1\\1\\&\textcolor{red}-\textcolor{red}1&\textcolor{red}1\\\textcolor{red}1&&\textcolor{red}-\textcolor{red}1&\textcolor{red}1\\\textcolor{red}-\textcolor{red}1&\textcolor{red}1&&\textcolor{red}1\\&\textcolor{red}-\textcolor{red}1&\textcolor{red}1\\&1&&-1\\&&&1
   \end{matrix}
   $$
   对应的丛单项式即 $\{x_i(t)\}_{i=-2,-1,1,\ldots,6}$, 对应的行列式恒等式是自明的. 

**广义主子式** 一般性理论见 [[FZ03]](https://arxiv.org/pdf/math/0305434.pdf), [[FZ98]](https://arxiv.org/pdf/math/9802056.pdf) 等. 记基本权为 $\{\varpi_i\}_{i=1}^r\subseteq \mathfrak h^\ast$, 使得 $\langle \alpha_j^\vee,\varpi_i\rangle=\delta_{i,j}$. 对于 $A_r$ 型 Lie 群而言, 

* 对 $\mathrm{Hom}_{\mathbb C}(\mathfrak h,\mathbb C)\ni E_{i,j}:\mathfrak{sl}(r+1,\mathbb C)\to \mathbb C, (a_{p,q})_{(r+1)\times (r+1)}\mapsto a_{i,j}$, 有
  $$
  \mathrm{ad}(h)(X_{i,j})=[(E_{i,i}-E_{j,j})(h)](X_{i,j}).
  $$
  从而定义单根 $\alpha_i=E_{i,i}-E_{i+1,i+1}$. 

* 选择并形式地记余单根 $\alpha_i^\vee=X_{i,i}-X_{i+1,i+1}\in \mathbb C$, 从而 $\langle\alpha_i^\vee,\alpha_j\rangle =c_{i,j}$. 

* $\varpi_i$ 恰为 $\sum_{k=1}^i E_{k,k}$, 从而特征 $x^{\varpi_i}=[x]_0^{\varpi_i}$ 对应主子式 $\Delta_{\varpi_i,\varpi_i}=\Delta_{1\cdots i,1\cdots i}$.

* 取 $u,v\in W\simeq S_{r+1}$​, 则有主子式
  $$
  \Delta_{u\varpi_i,v\varpi_i}(x)=\Delta_{\varpi_i,\varpi_i}(u^{-1}xv).
  $$

对非 $A_r$ 型 Lie 群而言, 同样可采用基本权与 Weyl 群定义广义主子式. 

**例子** $G_2$ 型 Lie 群的丛代数结构(基本思路)

* 采用 [**引理 2.8**](https://arxiv.org/pdf/math/9802056.pdf) 给出的升次公式. 即, 对任意 $f\in \mathbb C[G]$, 总有
  $$
  E_i^k(f')=k!f,\quad \text{若 }f(x t^{h_i})=t^kf(x), k\geq 0.
  $$

* 从而对 $G_2$ 型量子群而言, 有 $E_1(\Delta_{\varpi_1,s_1\varpi_1})=\Delta_{\varpi_1,\varpi_1}$. 考虑逆变换 $\Delta_{\varpi_1,s_1\varpi_1}=F_i(\Delta_{\varpi_1,\varpi_1})$, 以及记 $[F_i]_s=\dfrac{F_i^s}{s!}$, 得
  $$
  \begin{align*}
  &\Delta_{\varpi_1,s_1\varpi_1}=[F_1]_1(\Delta_{\varpi_1,\varpi_1}),&&\Delta_{\varpi_1,s_2s_1s_2s_1\varpi_1}=[F_2]_1[F_1]_2[F_2]_1[F_1]_1(\Delta_{\varpi_1,\varpi_1}),\\ 
  &\Delta_{\varpi_1,s_2s_1\varpi_1}=[F_2]_1[F_1]_1(\Delta_{\varpi_1,\varpi_1}),&&\Delta_{\varpi_1,w_0\varpi_1}=[F_1]_1[F_2]_1[F_1]_2[F_2]_1[F_1]_1(\Delta_{\varpi_1,\varpi_1}).\\ 
  &\Delta_{\varpi_1,s_1s_2s_1\varpi_1}[F_1]_2[F_2]_1[F_1]_1(\Delta_{\varpi_1,\varpi_1}),
  \end{align*}
  $$

* 依照字 $\vec i=(-2,-1,1,2,1,2,1,2)$ 给出 Bruhat 双胞腔 $G^{e,w_0}$ 中的丛代数结构

  <img src="C:\Users\czhan\AppData\Roaming\Typora\typora-user-images\image-20230328161028406.png" alt="image-20230328161028406" style="zoom:25%;" />

  对应的丛变单项式如下

  ![image-20230328161845745](C:\Users\czhan\AppData\Roaming\Typora\typora-user-images\image-20230328161845745.png)



待补充. 