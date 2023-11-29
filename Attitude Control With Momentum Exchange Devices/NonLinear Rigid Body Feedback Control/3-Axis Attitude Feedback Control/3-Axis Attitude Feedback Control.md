# 3-Axis Attitude Feedback Control

## Unconstrained Control

First let us assume that the external control (thrusters) is unconstrained in magnitude, and that the thruster can point in any direction.

EOM:
$$[\bm{I}]\bm{\dot{\omega}} = -[\bm{\tilde{\omega}}][\bm{I}]+\bm{u}+\bm{L}$$

> Where:
>
>* $\bm{u}$ is the control vector (thrusters)
>* $\bm{L}$ is the external torque (atmospheric torque)

Goal:
$$\delta\bm{\omega} = \bm{\omega} - \bm{\omega}_r\rightarrow0 \quad \bm{\sigma}\rightarrow0$$

> Where:
>
>* $\delta\bm{\omega}$ is the angular velocity error
>* $\bm{\omega}$ is the body angular velocity
>* $\bm{\omega}_r$ is the reference angular velocity
>* $\bm{\sigma} \rightarrow0$: Represents the attitude error between body frame $\mathcal{B}$ and the reference frame $\mathcal{R}$ using MRPs.

Exact attitude tracking error kinematic
differential equations:
$$\dot{\bm{\sigma}}=\frac{1}{4}\left[
    (1-\bm{\sigma}^2)\bm{I}+2[\tilde{\bm{\sigma}} + 2 \bm{\sigma}\bm{\sigma}^T]
    \right]\delta\bm{\omega}$$
