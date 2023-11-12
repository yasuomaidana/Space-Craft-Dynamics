# Momentum of a General System

## Linear momentum

$$d\bm{p} = \bm{\dot{R}}dm$$
$$p = \int_Bd\bm{p} = \int_B\bm{\dot{R}}dm =
\int_B\left(\bm{\dot{R}}_C  + \dot{r}\right)dm
= \left(\int_Bdm\right)\bm{\dot{R}}_C + \int_B\dot{r}dm \rightarrow
$$
$$\bm{p} = M \bm{\dot{R}}_C$$

Linear Momentum Rate:
$$\bm{\dot{p}} = \int_B\bm{\ddot{R}}dm = \int_Bd\bm{F} = \bm{F}$$
$$\bm{F} = \frac{{}^Nd}{dt}(\bm{p})$$

## Angular Momentum

![fbd](../3D%20free%20body%20diagram.jpg)

Angular momentum around P:
$$\bm{H}_p = \int_B\bm{\sigma}\times\bm{\dot{\sigma}}dm$$
$$\bm{\sigma} = \bm{R} - \bm{R}_p$$
Inertial time derivate:
$$\bm{\dot{H}}_p = \int_B\bm{\sigma}\times\bm{\ddot{R}}dm - \left(\int_B\bm{\sigma}dm\right) \times \bm{\ddot{R}}_P$$
$$\int_B\bm{\sigma}dm = \int_B\bm{R}dm - \left(\int_Bdm\right)\bm{R}_P = M(\bm{R}_C - \bm{R}_P)$$
Torque about P:
$$\bm{L}_P = \int_B\bm{\sigma}\times\bm{\ddot{R}}dm  = \int_B\bm{\sigma}\times d \bm{F}$$
$$\bm{\dot{H}}_p = \bm{L}_P + M \bm{\ddot{R}}_P \times (\bm{R}_C - \bm{R}_P)$$
If $\bm{P}$ is CM or inertial:
$$\bm{\dot{H}}_P = \bm{L}_p$$
