# Rigid Body Detumbling

State Vector : $\bm{\omega}$

Goal: $\omega \rightarrow 0$

EOM: $[\bm{I}]\bm{\dot{\omega}} = -[\bm{\tilde{\omega}}][\bm{I}]+\bm{Q}$

Lyapunov Function:$V(\bm{\omega}) = T = \frac{1}{2}\bm{\omega}^T[\bm{I}]\bm{\omega}$

Where:

* $\bm{Q}$ is the external control torque
* $\bm{I}$ is constant in Body frame components

Lyapunov rate:
$$\dot{V} = \bm{\omega}^T([\bm{I}]\bm{\dot{\omega}})=\bm{\omega}^T\left(-[\bm{\tilde{\omega}}][\bm{I}]+\bm{Q} \right)\\=\bm{\omega}^T\bm{Q} $$

Control:
$$\bm{Q} = -[\bm{P}]\bm{\omega} \quad\text{with} \quad [\bm{P}]=[\bm{P}]^T>0$$
$$\dot{V}(\bm{\omega})=-\bm{\omega}^T[\bm{P}]\bm{\omega}<0$$
Which ensures that $V$ is globally asymptotically stabilizing

## Using reference $\bm{\omega}_r$

Reference: $\bm{\omega}_r$
Goal: $\delta\omega = \omega -\bm{\omega}_r \rightarrow 0$

Note: ${}^\mathcal{B}\delta\bm{\omega} = {}^\mathcal{B}\bm{\omega} -[BR]{}^\mathcal{R}\bm{\omega}_r$

Lyapunov Function:$V(\delta\bm{\omega}) = T = \frac{1}{2}\delta\bm{\omega}^T[\bm{I}]\delta\bm{\omega}$

Lyapunov rate:
$$\dot{V} = \delta\bm{\omega}^T[\bm{I}]\frac{{}^\mathcal{B}d}{dt}(\delta\bm{\omega})$$

>Note: $\frac{{}^\mathcal{B}d}{dt}(\delta\bm\omega)=\bm{\dot\omega}-\bm{\dot\omega}_r + \bm{\dot\omega}\times\bm{\dot\omega}_r$
$$\dot{V} = \delta\bm{\omega}^T\left(-[\bm{\tilde{\omega}}][\bm{I}]\bm{\omega} + [\bm{I}]\bm{\omega}\times\bm{\omega}_r - [\bm{I}]\dot{\bm{\omega}}_r+\bm{Q} \right)$$

Control:
$$\bm{Q} = [\bm{\tilde{\omega}}][\bm{I}]\bm{\omega} - [\bm{I}]\bm{\omega}\times\bm{\omega}_r + [\bm{I}]\dot{\bm{\omega}}_r-[\bm{P}]\delta\bm{\omega}$$
Then:
$$\dot{V}(\bm{\omega})=-\delta\bm{\omega}^T[\bm{P}]\delta\bm{\omega}<0$$
Which ensures that $V$ is globally asymptotically stabilizing

> **Note**: These controls do not require any knowledge of the inertia matrix. It is very robust to inertia modeling errors.
