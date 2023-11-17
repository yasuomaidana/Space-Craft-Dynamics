# Inertia Matrix Properties

Definition
$${}^B[\bm{I}_C] = \int_B -[\tilde{r}][\tilde{r}]dm = \int_B {}^B
\begin{bmatrix}
r_2^2 + r_3^2 && -r_1r_2 && -r_1r_3 \\
-r_1r_2 && r_1^2 + r_3^2 && -r_2r_3 \\
-r_1r_3 && -r_2r_3 &&  r_1^2 + r_2^2
\end{bmatrix} dm
$$
Angular momentum Expression
$$\bm{H}_C =
{}^B\begin{pmatrix}
\bm{H}_{c_1} \\ \bm{H}_{c_2} \\ \bm{H}_{c_3} \end{pmatrix} = \int_B {}^B
\begin{bmatrix}
r_2^2 + r_3^2 && -r_1r_2 && -r_1r_3 \\
-r_1r_2 && r_1^2 + r_3^2 && -r_2r_3 \\
-r_1r_3 && -r_2r_3 &&  r_1^2 + r_2^2
\end{bmatrix} dm \ {}^B\begin{pmatrix}
\bm{\omega}_{1} \\ \bm{\omega}_{2} \\ \bm{\omega}_{3} \end{pmatrix} dm = [\bm{I}_C]\bm{\omega}$$

## Parallel Axis Theorem

![Parallel axis fbd](./Parallel%20axis%20fbd.jpg)
$$[\bm{I}_O] = [\bm{I}_C] + M [\bm{\tilde{R}}_C][\bm{\tilde{R}}_C]^T$$

Intertia about CM: $[\bm{I}_O]$

Total mass: $M$

CM offset: $[\bm{\tilde{R}}_C]$

## Coordinate Transformation

$${}^{\mathcal{F}}[\bm{I}] = [\bm{FB}]\ {}^{\mathcal{B}}[\bm{I}][\bm{FB}]^T$$

Body frame: $\mathcal{B}$

$2^{nd}$ Coordinate Frame: $\mathcal{F}$

![coordinate transformation](./coordinate%20transformation.jpg)
