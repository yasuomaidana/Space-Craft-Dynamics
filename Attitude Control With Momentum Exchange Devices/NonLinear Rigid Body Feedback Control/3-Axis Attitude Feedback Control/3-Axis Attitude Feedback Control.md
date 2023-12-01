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

Lyapunov fincton definition:
$$V(\bm{\omega,\bm{\sigma}})=\frac{1}{2}\delta\bm{\omega}^T\bm[I]\delta\bm{\omega}+2K\ln{\left(1+\bm{\sigma}^T\bm{\sigma}\right)}$$
> * $\frac{1}{2}\delta\bm{\omega}^T\bm[I]\delta\bm{\omega}$ is the kinetic energy like p.d. function
> * $2K\ln{\left(1+\bm{\sigma}^T\bm{\sigma}\right)}$ p.d. MRP attitude error function
</br>
</br>
> Note that the angular rate and inertia components are taken with respect to the body frame.
> $$[\bm{\dot{I}}] \Rightarrow \frac{{}^\mathcal{B}d}{dt}\left([\bm{I}]\right) = 0 \quad\quad \delta\dot{\bm{\omega}}\Rightarrow \frac{{}^\mathcal{B}d}{dt}\left(\delta\bm{\omega}\right)$$

To guarantee stability, we force $\dot{V}$ to be negative semi-deinte by setting it equal to
$$\dot{V}=-\delta\bm{\omega}^T[\bm{P}]\delta\bm{\omega}\\ [\bm{P}]=[\bm{P}]^T>0$$

Then we derive the closed-loop dynamics:
$$[\bm{I}]\frac{{}^\mathcal{B}d}{dt}(\delta\bm{\omega})+[\bm{P}]\delta\bm{\omega}+\bm{K}\bm{\sigma}=0$$

Using transponse theorem $\frac{{}^\mathcal{B}d}{dt}(\delta\bm{\omega})=\dot{\bm{\omega}}-\dot{\bm{\omega}}_r+\bm{\omega}\times\bm{\omega}_r$ yields
$$[\bm{I}]\left(\dot{\bm{\omega}}-\dot{\bm{\omega}}_r+\bm{\omega}\times\bm{\omega}_r \right)+[\bm{P}]\left(\bm{\omega}-\bm{\omega}_r\right)+\bm{K}\bm{\sigma}=0$$

Substitute EOM: $[\bm{I}]\bm{\dot{\omega}} = -[\bm{\tilde{\omega}}][\bm{I}]+\bm{u}+\bm{L}$
Then:
$$\bm{u}= -\bm{K}\bm{\sigma}-[\bm{P}]\delta\bm{\omega}+[\bm{I}] \left(\dot{\bm{\omega}}_r-[\tilde{\bm{\omega}}]\bm{\omega}_r\right)+[\tilde{\bm{\omega}}][\bm{I}]\bm{\omega}-\bm{L}$$

$${}^{\mathcal{B}}\bm{\omega}_r=[BR]{}^{\mathcal{R}}\bm{\omega}_r \quad\quad
{}^{\mathcal{B}}\bm{\dot\omega}_r=[BR]{}^{\mathcal{R}}\bm{\dot\omega}_r$$
