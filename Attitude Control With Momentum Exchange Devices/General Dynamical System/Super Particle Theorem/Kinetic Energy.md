# Kinetic Energy

![Free Body Diagram](./3D%20free%20body%20diagram.jpg)

Definition: $$T = \frac{1}{2}\int_B\bm{\dot{R}}\cdot\bm{\dot{R}}dm$$

$$\bm{\dot{R}} = \bm{\dot{R}}_C + \bm{\dot{r}}$$

$$T = \frac{1}{2}\left(\int_B dm \right) \bm{\dot{R}}_C \cdot\bm{\dot{R}}_C + \bm{\dot{R}}_C \cdot\int_B\bm{\dot{r}}dm + \frac{1}{2}\int_B\bm{\dot{r}}\cdot\bm{\dot{r}}dm \rightarrow $$
$$T = \frac{1}{2}M\bm{\dot{R}}\cdot\bm{\dot{R}} + \frac{1}{2}\int_B\bm{\dot{r}}\cdot\bm{\dot{r}}dm$$

Where:

* $\frac{1}{2}M\bm{\dot{R}}\cdot\bm{\dot{R}} = $  Energy of CM
* $\frac{1}{2}\int_B\bm{\dot{r}}\cdot\bm{\dot{r}}dm =$ Energey **about** CM

Differentiate Energy:
$$\frac{dT}{dt} = M \bm{\ddot{R}}_C\cdot\bm{\dot{R}}_c + \int_B\bm{\dot{r}}\cdot\bm{\dot{r}}dm$$
Where:

* $M\bm{\ddot{R}} = \bm{F}$ and $\bm{\ddot{r}} = \bm{\ddot{R}}-\bm{\ddot{R}}_c$

Then:
$$\frac{dT}{dt} = \bm{F}\cdot\bm{\dot{R}}_c + \int_Bd\bm{F}\cdot\bm{\dot{r}} \rightarrow$$
$$T(t_2) - T(t_1) = \int_{t_1}^{t_2}\bm{F}\cdot\bm{\dot{R}}_cdt+ \int_{t_1}^{t_2}\int_Bd\bm{F}\cdot\bm{\dot{r}}dt$$
