# Equations of Motion

Euler's equation:
$$\bm{\dot{H}}_C = {}^{\mathcal{B}}\frac{d}{dt}(\bm{H}_C) + \bm{\omega} \times \bm{H}_C = \bm{L}_C\$$

$${}^{\mathcal{B}}\frac{d}{dt}(\bm{H}_C) =
{}^{\mathcal{B}}\frac{d}{dt}([\bm{I}])\bm{\omega}+
[\bm{I}]{}^{\mathcal{B}}\frac{d}{dt}(\bm{\omega})=
[\bm{I}]\bm{\dot{\omega}}
$$

Euler's rotational equations of motion:
$$[\bm{I}]\bm{\dot{\omega}} =
-[\tilde{\omega}][\bm{I}]\bm{\omega}+\bm{L}_C$$

Principal axis version of rotational EOM:
$$I_{11}\dot{\omega}_1 = - (I_{33} - I_{22})\omega_2\omega_3 + L_1 \\
I_{22}\dot{\omega}_2 = - (I_{11} - I_{33})\omega_3\omega_1 + L_2 \\
I_{33}\dot{\omega}_1 = - (I_{22} - I_{11})\omega_1\omega_2 + L_3 \\$$

## Additional Definitions

State Vector $$\bm{x} = (x_1\dots x_N)^T$$
EOM:
$$\bm{\dot{x}} = \bm{f}(x,t) \text{ Non-autonomous System} \\
\bm{\dot{x}} = \bm{f}(x) \text{ Autonomous System} \\$$

Control Vector:
$$\bm{u} = \bm{g}(\bm{x})$$

Closed-Loop System:
$$\bm{\dot{x}}=\bm{f}(\bm{x},\bm{u},t)$$

Equilibrium State: A state vector point $\bm{x}_e$ is said
to be an equilibrium state (or equilibrium point) of
a dynamical system described by
$\bm{\dot{x}} = \bm{f}(\bm{x},t)$ at time $t_0$ if $$\bm{f}(\bm{x}_c,t)=0 \ \forall t>t_0$$
$$\bm{\dot{x}}_c = 0 \space \bm{x}_c=\text{constant}$$

![neighborhood and stabilities](./neighborhood%20and%20stabilities.jpg)
