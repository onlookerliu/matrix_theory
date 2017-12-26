
## 习题五

### 1.

设 $\Vert \cdot \Vert$ 是酉空间 $\mathbb{C}^n$ 的向量范数，证明向量范数的下列基本性质：

(1) 零向量的范数为零

由向量范数正定性 $\Vert x \Vert = 0 \iff x = 0$

(2) 当 $x$ 是非零向量时: $\big\lVert \dfrac{x}{\Vert x \Vert} \big\rVert = 1$

由齐次性
$$
\big\lVert \frac{x}{\Vert x \Vert} \big\rVert = \big\vert \frac{1}{\Vert x \Vert} \big\vert \cdot \Vert x \Vert = 1
$$

(3) $\Vert -x \Vert = \Vert x \Vert$

同上，齐次性；

(4) $\big| \Vert x \Vert - \Vert y \Vert \big| \leq \Vert x - y\Vert$

$$
\begin{align*}
&\Vert x \Vert = \Vert x+y-y \Vert y \leq \Vert x-y \Vert + \Vert y \Vert &\implies \Vert x \Vert- \Vert y \Vert\leq\Vert x-y\Vert \\
&\Vert y \Vert = \Vert y+x-x \Vert x \leq \Vert y-x \Vert + \Vert y \Vert &\implies \Vert y \Vert- \Vert x \Vert\leq\Vert x-y\Vert
\end{align*}
$$

综上 $\big\vert \Vert x\Vert - \Vert y\Vert \big\vert \leq \Vert x-y \Vert$

### 2.

证明: 若 $x\in\mathbb{C}^n$, 则

(1) $\Vert x\Vert_2 \leq \Vert x\Vert_1 \leq \sqrt{n}\Vert x\Vert_2$

$$
\begin{align*}
&\Vert x\Vert_2 = \left( \sum_{i=1}^n x_i^2 \right)^{1/2} \leq \sum_{i=1}^n (x_i^2)^{1/2} = \sum_{i=1}^n\vert x_i\vert = \Vert x\Vert_1 \\
&(1+1+\cdots+1)(x_1^2+x_2^2+\cdots+x_n^2) = n\Vert x \Vert \geq (x_1+x_2+\cdots+x_n)^2 = \Vert x\Vert_1^2
\end{align*}
$$

(2) $\Vert x\Vert_{\infty} \leq \Vert x\Vert_1 \leq n\Vert x\Vert_{\infty}$

$$
\max_{1\leq i\leq n}|x_i| \leq \sum_{i=1}^n|x_i| \leq \sum_{i=1}^n\max|x_i| = n\max_{1\leq i\leq n}|x_i|
$$

(3) $\Vert x\Vert_{\infty} \leq \Vert x\Vert_2 \leq \sqrt{n}\Vert x\Vert_{\infty}$

$$
\max_{1\leq i\leq n}|x_i| \leq \left( \sum_{i=1}^n (\max_{1\leq i\leq n} x_i)^2 \right)^{1/2} = \sqrt{n}\max_{1\leq i\leq n}|x_i|
$$

### 12.

设矩阵 $A$ 的F-范数等于 $a$，$U$ 是酉矩阵，问 $AU$ 与 $UA$ 的F-范数各是多少？请总结你的计算

$$
\begin{align*}
&\Vert A\Vert_{F} = \left( \sum_{i=1}^n a_{ij}^2 \right)^2 = \left( \tr(AA^*) \right) \\
&\Vert UA\Vert_{F} = = [\tr(UA\cdot A^*U^*)]^{1/2} = \tr(AA^*)^{1/2} \\
&\Vert AU\Vert_{F} = = [\tr(AU\cdot U^*A^*)]^{1/2} = \tr(A^*A)^{1/2} \\
\end{align*}
$$

由上可知，酉矩阵保持范数不变

### 16.

证明矩阵的1-范数、2-范数和$\infty$-范数分别是向量的1-范数、2-范数和$\infty$-范数的诱导范数

分别依照范数定义证明

$$
\Vert A \Vert_{p} \leq \max_{x\neq 0} \frac{\Vert Ax\Vert_{p}}{\Vert x\Vert_{p}} \quad p = 1,2,\infty
$$

并且说明等号可以取到即可。

### 21.

设 $T$ 为正交矩阵，又 $A\in\mathbb{R}^{n\times n}$. 证明:

(1) $\Vert T \Vert_2 = 1$

$$
T'T=I_n \quad \rho(T^*T)=\rho(I_n)=1 \quad \Vert T \Vert_2 = \sqrt{\rho(T^*T)} = 1
$$

(2) $\Vert A \Vert_2 = \Vert TA \Vert_2$

$$
\Vert TA \Vert_2 = \sqrt{\rho(A^*T^*TA)} = \sqrt{\rho(A^*A)} = \Vert A \Vert_2
$$

(3) 试解释上面的两个结果.

- 正交变换为等距变换
- 正交变换保持矩阵2-范数不变

### 22.

设 $A$, $B$ 为 $n$ 阶矩阵，，其中 $A$ 可逆而 $B$ 不可逆，设 $\Vert \cdot \Vert$ 是任何一种矩阵范数.
定义 $A$ 的条件数 $\Cond(A) = \Vert A\Vert \Vert A^{-1}\Vert$.
证明: $\Vert A-B \Vert \geq 1/\Vert A^{-1}\Vert$. 解释这个结果

因 $B$ 不可逆，故必有0奇异值，从而 $I - A^{-1}B$ 有特征值1

$$
1\leq \Vert I-A^{-1}B \Vert = \Vert A^{-1}(A-B) \Vert \leq \Vert A^{-1}\Vert \cdot\Vert A-B\Vert
$$

则有 $\Vert A-B\Vert \geq \frac{1}{\Vert A^{-1}\Vert}$

因 $\Vert A \Vert \neq 0$, $\Vert A^{-1} \Vert = \frac{\Cond(A)}{\Vert A\Vert}$, 于是

$$
\Vert A-B \Vert \leq \frac{\Cond(A)}{\Vert A\Vert} \quad \Cond(A)=\Vert A\Vert\cdot\Vert A^{-1}\Vert=1
$$

以上结果表明存在奇异矩阵 $B$ 与可逆矩阵 $A$ 在范数意义上最接近

### 23.

设 $A\in\mathbb{C}^{m\times n}$, $\sigma_1, \sigma_2, \cdots, \sigma_n$ 是 $A$ 的全部奇异值. 证明

(1) $\Cond(A) = \sigma_1(A)/\sigma_n(A)$, 其中 $\sigma_1(A)$ 与 $\sigma_n(A)$ 分别是 $A$ 的最大和最小奇异值

$\sigma_1, \sigma_2, \cdots, \sigma_n$ 是 $A$ 的全部奇异值, 则 $1/\sigma_1, 1/\sigma_2, \cdots, 1/\sigma_n$ 是 $A^{-1}$ 的全部奇异值, 容易得知

$$
\Vert A\Vert_2 = \sigma_1 \quad \Vert A^{-1} \Vert_2 = \frac{1}{\sigma_n}
$$

从而$\Cond(A) = \sigma_1(A)/\sigma_n(A)$

(2) $\Vert A \Vert_F = \Big( \sum_{i=1}^r \sigma_i^2 \Big)^{1/2} = [\tr(A^*A)]^{1/2}$

$$
\Vert A \Vert_F = \Big( \sum_{i=1}^n \sigma_i^2 \Big)^{1/2} = \Big( \sum_{i=1}^r \sigma_i^2 \Big)^{1/2} = [\tr(A^*A)]^{1/2}
$$

(3) $\Vert A \Vert_2 = \sigma_{\max}(A)$

$$
\Vert A \Vert_2 = \sqrt{\rho(A^*A)} = \sigma_1(A)
$$

### 26.

设 $A_k = \begin{pmatrix} \frac{1}{k^2} & \frac{k^2+k}{k^2+1} \\ 2 & (1-\frac{2}{k})^k \end{pmatrix}$，求 $\lim_{k\to\infty}A_k$

逐项求导即可 $\lim_{k\to\infty}A_k = \begin{pmatrix} 0&1 \\ 2&e^{-2} \end{pmatrix}$

### 27.

设 $\lim_{k\to\infty} A_k = A$

(1) 如果 $A_k$ 均为正定矩阵，问 $A$ 有何特点

$$
\forall x\in\mathbb{C}^n (A_k x, x) > 0 \iff x'A_k x > 0
$$

若 $A\neq 0$, 则 $(Ax, x) > 0$; 反之 $A=0$, $(Ax, x)=0$. 于是 $(Ax, x) \geq 0$, $A$ 半正定

(2) 如果 $A_k$ 均为正规矩阵，问 $A$ 有何特点

$A$ 为正规矩阵，则 $\forall k, A_kA_k^* = A_k^*A_k$, 两边取极限可以得到 $AA^* = A^*A$

(3) 如果 $A_k$ 均为可逆矩阵，问 $A$ 有何特点

$A$ 不一定可逆，可取 $A_k = \begin{pmatrix} \frac{1}{k}&0 \\ 0&\frac{1}{k} \end{pmatrix}$ 说明问题

### 30.

设 $A = \begin{pmatrix} 2&-\frac{1}{2} \\ 2&0 \end{pmatrix}$, 求 $\sum_{k=0}^{\infty} \frac{A^K}{2^k}$

根据求和公式

$$
\sum_{k=0}^{\infty} \frac{A^K}{2^k} = (I-\frac{A}{2})^{-1}
$$

容易解得 $\begin{pmatrix} 4&-1 \\ 4&0 \end{pmatrix}$

### 31.

设 $A = \begin{pmatrix} -0.6&1&0.8 \\ 0&0.2&0 \\ -0.6&1&0.8 \end{pmatrix}$. 试判断 $A$ 是否幂收敛.

$$
|\lambda I - A| = \begin{vmatrix}
\lambda+0.6 & -1 & -0.8 \\
0 & \lambda-0.2 & 0 \\
0.6 & -1 & \lambda-0.8
\end{vmatrix} = (\lambda-0.2)\times\begin{vmatrix}
\lambda+0.6 & -0.8 \\
0.6 & \lambda-0.8
\end{vmatrix} = (\lambda-0.2)\lambda(\lambda-0.2)
$$

不难发现特征值均小于1，从而幂收敛

### 32.

(1) 设 $A = \begin{pmatrix} 0&0 \\ 1&-2 \end{pmatrix}$，求 $e^A, \sin(A), \cos(A)$

此类矩阵函数问题均可按照课本三种方法来解答，根据实际情况采用简洁高效的算法即可。注意：要多利用最小多项式和 Jordan 标准型的信息

下面利用符号计算软件[Mathematica](https://www.wolfram.com/mathematica/) 来给出计算结果，后面相似问题可同样处理。


