# Stability of a Linearized System

## Linearization of Dynamical System

Reference motion given by:
$$\bm{\dot{x}}_r= \bm{f}(\bm{x}_r,\bm{u}_r)$$

Noninear EOM:
$$\bm{\dot{x}} = \bm{f}(\bm{x},\bm{u})$$

Feedback control:
$$\delta\bm{u} = \bm{u} - \bm{u}_r$$

Departure motion:
$$\delta\bm{x} = \bm{x} - \bm{x}_r$$

> $\bm{u}_r$ Feedforward control

Performing a Taylor Series expansion of $\bm{x}$ about $(\bm{x}_r,\bm{u}_r)$ we obain

$$\delta \bm{\dot{x}} = \bm{f}(\bm{x}_r,\bm{u}_r) + \frac{\partial}{\partial \bm{x}} (\bm{x}_r,\bm{u}_r)\delta \bm{x} + \frac{\partial}{\partial \bm{u}} (\bm{x}_r,\bm{u}_r)\delta \bm{u} + H.O.T - \bm{f}(\bm{x}_r,\bm{u}_r)$$

$$
\delta \bm{\dot{x}} \simeq  \frac{\partial}{\partial \bm{x}} (\bm{x}_r,\bm{u}_r)\delta \bm{x} + \frac{\partial}{\partial \bm{u}} (\bm{x}_r,\bm{u}_r)\delta \bm{u}
$$

Defining
$$[\bm{A}] = \frac{\partial (\bm{x}_r,\bm{u}_r)}{\partial \bm{x}}$$
$$[\bm{B}] = \frac{\partial (\bm{x}_r,\bm{u}_r)}{\partial \bm{u}}$$

The linearized system is then written in standard form as:
$$\delta \dot{\bm{x}} \simeq [\bm{A}]\delta \bm{x} + [\bm{B}]\delta \bm{u}$$

If the nominal reference motion is an equitourn state xe,
then the linearized EOM simplify to:

$$\dot{\bm{x}} \simeq [\bm{A}] \bm{x} + [\bm{B}] \bm{u}$$
