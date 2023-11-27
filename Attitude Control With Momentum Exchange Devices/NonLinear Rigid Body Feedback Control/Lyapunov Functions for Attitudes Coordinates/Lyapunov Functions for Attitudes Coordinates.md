# Lyapunov Functions for Attitudes Coordinates

## Modified Rodrigues Parameters

Lyapunov Function:
$$V(\bm{\sigma}) = 2 \bm{K}(1+\bm{\sigma}^T\bm{\sigma})$$
> If you switch to the shadow MRP set on the $\sigma2=1$ surface, then this Lyapunov function is continous

Lyapunov Rate:
$$\dot{V} = \bm{\omega}^T(\bm{K}\bm{\sigma})$$
> This leads to elegant linear attitude feedback laws which are globally stabilizing by switching between the original and shadow MRP set.

## Euler Paramters

Ideal Attitude:
$$\hat{\bm{\beta}} = \begin{pmatrix}1&&0&&0&&0 \end{pmatrix}^T$$
Lyapunov Function:
$$V(\bm{\beta})=\bm{K}(\bm{\beta}-\hat{\bm{\beta}})^T(\bm{\beta}-\hat{\bm{\beta}})$$
Lyapunov Rate:
$$\dot{V}=\bm{K}\bm{\omega}^T[B(\bm{\beta})]^T(\bm{\beta}-\hat{\bm{\beta}})$$
Recall that
$$[B(\bm{\beta})]^T\bm{\beta}=0$$
This leads to:
$$\dot{V}=\bm{K}\bm{\omega}^T\begin{pmatrix}
\beta_1\\\beta_2\\\beta_3\\\beta_4\end{pmatrix}=\bm{\omega}^T(\bm{K}\bm{\epsilon})$$
> Note that will stabilize the atitude to $\beta_0 =\pm1$, which is the same attitude. However, no guarantee is made if the long or short rotational path is used.
