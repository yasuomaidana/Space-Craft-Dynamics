# Stability Definitions of Time Dependent Systems

## Non-Autonomous Stability Definitions

**Lyapunov Stable**: The motion $\bm{x}(t)$ is said to be Lyapunov stable (or stable) relative to $\bm{x}_r(t)$ if for each $\epsilon>0$ exists a $\delta(\epsilon,t_0)>0$ such that
$$\bm{x}({t_0})\in B_{\delta}(\bm{x_r}(t_0)) \Rightarrow \bm{x}(t)\in B_{\epsilon}(\bm{x}_r(t)) \\\forall t>t_0$$

**Asymptotic Stability**: The motion $\bm{x}(t)$ is said to be asymptotically stable relative to $\bm{x}_r(t)$ if $\bm{x}(t)$ is Lyapunov stable and there exists a $\delta(t_0)>0$ such that
$$\bm{x}({t_0})\in B_{\delta}(\bm{x}_r(t_0)) \Rightarrow \lim_{t\rightarrow \infin} \bm{x}(t) = \bm{x}_r(t)$$

**Uniformly Lyapunov Stable** The motion $\bm{x}(t)$ is said to be uniformly stable relative to $\bm{x}_r(t)$ if for each $\epsilon>0$ exists a $\delta(\epsilon)>0$ such that
$$\bm{x}({t_0})\in B_{\delta}(\bm{x_r}(t_0)) \Rightarrow \bm{x}(t)\in B_{\epsilon}(\bm{x}_r(t)) \\\forall t>t_0$$

**Uniformly Asymptotic Lyapunov Stability** The motion $\bm{x}(t)$ is said to be uniformly asymptotically stable relative to $\bm{x}_r(t)$ if $\bm{x}(t)$ is uniformly stable relative to $\bm{x}_r(t)$ and there exists a $\delta>0$ such that
$$\bm{x}({t_0})\in B_{\delta}(\bm{x}_r(t_0)) \Rightarrow \lim_{t\rightarrow \infin} \bm{x}(t) = \bm{x}_r(t)$$

## Positive definite functions

**Positive (Semi)-Definite Function**: A scalar continues function $V(\bm{x},t)$ is said to be locally positive (semi-)definite about $\bm{x}_r$, if
$$\forall\bm{x}\in\bm{B}_{\delta}(\bm{x}_r)\Rightarrow V(\bm{x},t) >(\ge)\bm{W}_1(\bm{x})$$

Where $\bm{W}_1$ is a positive definite about $\bm{x}_r$

### Positive definite functions-Example

* $V(t,\bm{x}) = \frac{x^2}{2}$ is positive definite
* $V(t,\bm{x}) = \frac{x^2}{2}e^{-t}$ is not positive definite

**Decrescent function**: A scalar continues function $V(\bm{x},t)$ is said to be locally decrescent about $\bm{x}_r$, if
$$\forall\bm{x}\in\bm{B}_{\delta}(\bm{x}_r)\Rightarrow V(\bm{x},t) \le\bm{W}_2(\bm{x})$$

Where $\bm{W}_2$ is a positive definite about $\bm{x}_r$

## Lyapunov's Direct Method

**Uniform Stability**: Assume a $\bm{\dot{x}} = \bm{f}(\bm{x},t)$. Let $V(\bm{x},t)$ be a continously differentiable possitive definite decrescent function with:
$$\bm{W}_1(\bm{x}) \le V(t,\bm{x}) \le \bm{W}_2(\bm{x})$$

and $\bm{W}_1(\bm{x})$ and $\bm{W}_2(\bm{x})$ being positive definite functions. If

$$\dot{V} = \frac{\partial{V}}{\partial t} + \frac{\partial{V}}{\partial \bm{x}} \bm{f}(\bm{x},t) \le 0$$
then $\bm{x}=0$ is uniformly stable

**Uniform Asymptotic Stability**: Assume a $\bm{\dot{x}} = \bm{f}(\bm{x},t)$. Let the dynamical system be uniformly stable and the Lyapunov rate satisfies

$$\dot{V} = \frac{\partial{V}}{\partial t} + \frac{\partial{V}}{\partial \bm{x}} \bm{f}(\bm{x},t)\le -\bm{W}_3$$

and $\bm{W}_3(\bm{x})$ is a positive definite function, then  $\bm{x}=0$ is uniformly asymptotically stable.

### Lyapunov's Direct Method Simple Example

Assume $\bm{\dot{x}} = \bm{f}(\bm{x})$. Stability for this non-autonomous system can proven trivially if you can find a Lyapunov function which satisfies.

$$V=V(\bm{x}) \quad \dot{V}=\dot{V}(\bm{x})$$

#### Time varying feedback gain Example

Let $\ddot{x} + kx = u$ wth $k > 0$.

The feedback control chosen to be $u = -c(t)\bm{x}$ wich leads to the followinng non-autonomous closed loop dynamics:
$$\ddot{x}+c(t)\dot{x}+kx = 0$$

To study the stability of this time dependent differential equation. we chose the Lyapunov function
$$V=V(x,\dot{x})=\frac{\dot{x}^2}{2}+\frac{k}{2}x^2$$

Differentiating this V function and substituiting the system equation of motion leads to
$$\dot{V}=\bm{\dot{x}}u=-c(t)\dot{x}^2$$
If $c(t)>0$, then the system is uniformly stable (condition does not depend initial condition).
