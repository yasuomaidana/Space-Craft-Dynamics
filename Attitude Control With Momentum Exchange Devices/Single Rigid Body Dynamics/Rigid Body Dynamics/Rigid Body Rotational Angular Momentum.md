# Rigid Body Rotational Angular Momentum

![fbd](./General%20Angular%20Momentum.jpg)

If we focused just in the body:
$$\bm{\dot{r}} = \frac{{}^Bd}{dt}\bm{r} + \bm{\omega}_{B/N} \times \bm{r} \rightarrow \\ = \bm{\omega}_{B/N} \times \bm{r}$$

Since the derivative of $\bm{r}$ is constant in the body reference frame.

## General Angular momentum

$$\bm{H}_O = \int_B\bm{R}\times\bm{\dot{R}}dm \\ = \bm{R}_C\times M\bm{\dot{R}}_C + \int_B \bm{r} \times \bm{\dot{r}}dm$$

Defining Momenum about CM as $\bm{H}_c $
$$\bm{H}_c = \int_B \bm{r} \times \bm{\dot{r}}dm$$

Since $\bm{\dot{r}} = \bm{\omega}_{B/N} \times \bm{r}$

$$\bm{H}_c = \int_B \bm{r} \times \bm{\omega}_{B/N} \times \bm{r} dm = \left(\int_B-[\tilde{r}][\tilde{r}]dm \right)\bm{\omega}$$

## Inertia Matrix Properties

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
