# Definite Definitions

**Positive (Negative) Definite Function**: A scalar continues function $V(\bm{x})$ is said to be locally positive (negative) definite about $\bm{x}_r$, if
$$\bm{x} = \bm{x}_r \Rightarrow V(\bm{x}) = 0$$
and there exists a $\delta>0$ such that:
$$\forall\bm{x}\in\bm{B}_{\delta}(\bm{x}_r)\Rightarrow V(\bm{x}) > 0 \quad\quad (V(\bm{x}) < 0)$$

**Positive (Negative) Semi-Definite Function**: A scalar continues function $V(\bm{x})$ is said to be locally positive (negative) semi-definite about $\bm{x}_r$, if
$$\bm{x} = \bm{x}_r \Rightarrow V(\bm{x}) = 0$$
and there exists a $\delta>0$ such that:
$$\forall\bm{x}\in\bm{B}_{\delta}(\bm{x}_r)\Rightarrow V(\bm{x}) \ge 0 \quad\quad (V(\bm{x}) \le 0)$$

A matrix $[\bm{K}]$ is said to be positive of (negative) semi-definite if for every state vector $\bm{x}$:

$$
\bm{x}^T[\bm{K}]\bm{x}
\begin{cases}
>0 \Rightarrow \text{positive definite}\\
\ge 0 \Rightarrow \text{positive semi-definite}\\
<0 \Rightarrow \text{negative definite}\\
\le 0 \Rightarrow \text{negative semi-definite}
\end{cases}
$$
