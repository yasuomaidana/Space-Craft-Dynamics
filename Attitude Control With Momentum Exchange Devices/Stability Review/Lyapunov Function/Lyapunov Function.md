# Lyapunov Function

**Lyapunov Function**:

The scalar function $V(\bm{x})$ is a Lyapunov Function for the dynamical system $\bm{\dot{x}}=\bm{f}(\bm{x})$ if it is continous and there exists a $\delta>0$ such that for any $\bm{x} \in B_{\delta}(\bm{x}_r)$

1. $V(\bm{x})$ is a positive definite function about $\bm{x}_r$
2. $V(\bm{x})$ has continous partial derivatives
3. $\dot{V}(\bm{x})$ is negative semi-definite

## Lyapunov Stability

If a Lyapunov function $V(\bm{x})$ exists for the dynamical system $\dot{\bm{x}} = \bm{f}(\bm{x})$, then this system is stable about the origin.

### Example

Consider the spring-mass system:

$$m\ddot{x}+kx=0$$

Let us use the total system energy as a candidate Lyapunov function

$$V(x,\dot{x}) = \frac{1}{2}m\dot{x}^2+\frac{1}{2}kx^2$$

The Lyapunov rate is then expressed as

$$\dot{V}(x,\dot{x}) = (m\ddot{x}+kx)\dot{x}=0\le0$$

$$\dot{V} = \frac{\partial V}{\partial\bm{x}}^T \quad \dot{x}=\frac{\partial V}{\partial{\bm{x}}}^T \quad \bm{f}(\bm{x})\le 0$$

All projections of the dynamical motion on the Lyapunov function surface must point toward the reference state $\bm{x}_r$

## Asymptotic Stability

Assume $V(\bm{x})$ is a Lyapunov function about $\bm{x}_r(t)$ for the dynamical system $\dot{\bm{x}} = \bm{f}(\bm{x})$, then this system is asymptitically stable if:

1. the system is stable about $x_r$
2. $\dot{V}(x)$ is negative definite about $x_r$

**Theorem**
Assume there exists a Lyapunov function $V(\bm{x})$ of the dynamical system $\bm{\dot{x}} = \bm{f}(\bm{x})$. Let $\Omega$ be the non empty set of state vectors such that
$$\bm{x}\in \bm{\Omega} \Rightarrow \bm{\dot{V}}(\bm{x}) = 0$$

If the first $k-1$ derivatives of $V(\bm{x})$, evaluated on the set $\Omega$, are zero
$$\frac{\bm{d^iV(x)}}{\bm{dt^i}} = 0 \quad \forall \bm{x} \in \bm{\Omega} \quad i=1,2, \dots, k-1$$

and the $k^{th}$ derivative is negative definite on the set $\Omega$

$$\frac{\bm{d^kV(x)}}{\bm{dt^k}} < 0 \quad \forall \bm{x} \in \Omega$$

Then the system $\bm{x}(f)$ is asymptotically stable if $k$ is an odd number.

### Asymptotic Stability example

Consider the spring mass damper system
$$m\ddot{x} + c\dot{x} + kx =0$$

With the lyapunov function:

$$V(x,\dot{x}) = \frac{1}{2}m\dot{x}^2+\frac{1}{2}kx^2$$

Taking the derivative we only determine stability:

$$\dot{V}(x,\dot{x}) = (m\ddot{x}+kx)\dot{x}=-c\dot{x}^2\le0$$

Evaluating the higher derivativs on the set $x=0$ yields:

$$\ddot{V}(\dot{x}=0) = -2c\ddot{x}\dot{x}= 2\frac{c}{m}(c\dot{x} + kx)\dot{x} = 0$$
$$\overset{\dots}{V} = -2\frac{c}{m^2} \left((c\dot{x} + kx)^2 + c^2\dot{x}^2 + ckx\dot{x}  - k\dot{x}^2\right)\$$

$$\overset{\dots}{V}(\dot{x}=0) = -2\frac{ck^2}{m^2} x^2<0\$$

## Lyapunov Stability of Linear System

Assume that the dynamical system is of the linear form:
$$\bm{\dot{x}} = [\bm{A}][\bm{x}]$$
Let be $[P]>0$ be a symmetric, p.d. matrix, then we define

$$V(\bm{x}) = \frac{1}{2}\bm{x}^T[\bm{P}]\bm{x}$$
$$\dot{V}(\bm{x}) = \bm{\dot{x}}^T[\bm{P}]\bm{x} + \bm{x}^T[\bm{P}]\bm{\dot{x}}$$
$$\dot{V}(\bm{x}) = \bm{x}^T\left[[\bm{A}]^T[\bm{P}]+ [\bm{A}][\bm{A}]\right]\bm{]x} < 0$$

**Theorem**: An autonomous linear system $\bm{\dot{x}} = [A]\bm{x}$ is stable if and only if for any symmetric possitive definite $[R]$ there exists a corresponding symmetric, positive $[P]$ such that
$$[\bm{A}]^T[\bm{P}] + [\bm{P}][\bm{A}] = -[\bm{R}]$$
