# Stability Definitions

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
![asymptotic stability](./Asymptotic%20stability.jpg)
