---
layout: single
title: "17)MOSFET Essentials"
typora-root-url: ../
categories : "Fundamental-of-Semicondutor"
tag : [diode, MOSFET]
#tag : [me, me2, me3]
toc : true
toc_sticky : true
author_profile : false
---
## Fundamental of semiconductor

MOSFETs은 다음 그림처럼 p-Si에 minority Carrier인 전자가 channel을 형성하여 스위치를 조절하는 장치이다.

<img src="/images/figure/image-20221227100733611.png" alt="image-20221227100733611" style="zoom:80%;" />

전극으로 $N^+$ 를 사용하고 channel로 minority carrier 전자를 사용하는 이유는 ohmic contact를 위해서이다.

Mosfet은 2차원에서 나타내는 상황이므로 에너지밴드 다이어그림을 2차원에 대한 에너지 밴드 다이어그램으로 나타내야한다.

---

이를 다음의 그림으로 나타낼 수 있다.

1) $V_G = 0, V_D = 0$

<img src="/images/17. MOSFETs-The Essentials/image-20240110154753322.png" alt="image-20240110154753322" style="zoom: 80%;" /><img src="/images/17. MOSFETs-The Essentials/image-20240110154805506.png" alt="image-20240110154805506" style="zoom:80%;" />

점선은 Fermi Level을 의미한다.

2. $V_G  \geq   V_T, V_D = 0$

<img src="/images/17. MOSFETs-The Essentials/image-20240110155650261.png" alt="image-20240110155650261" /><img src="/images/17. MOSFETs-The Essentials/image-20240110155550932.png" alt="image-20240110155550932" style="zoom:80%;" />

3. $V_G \geq V_T, V_D > 0$

<img src="/images/17. MOSFETs-The Essentials/image-20240110161547894.png" alt="image-20240110161547894" style="zoom:80%;" />

4. $V_G \geq V_T, V_D >> 0$

<img src="/images/17. MOSFETs-The Essentials/image-20240110161727430.png" alt="image-20240110161727430" style="zoom:80%;" /><img src="/images/17. MOSFETs-The Essentials/image-20240110161742967.png" alt="image-20240110161742967" style="zoom:80%;" />

$V_D$를 많이 가했을 경우, Fermi Level이 아래쪽으로 많이 내려가 있게 되어 delpletion region이 형성된다.

점선 3개중에 아래 쪽 점선이 $F_n$을 나타낸다.

Depletion region이 형성되었다는 것은 Pinch-off voltage가 필요하다는 것을 의미한다. 

따라서 다음을 알 수 있다.
$$
V_G = V_{channel} + V_{Dsat}
$$


따라서 이를 종합하여 $V_G$에 따른 $V_D$를 나타내면 다음과 같은 그래프를 나타낸다는 것을 알 수 있다.

<img src="/images/17. MOSFETs-The Essentials/image-20240110170904148.png" alt="image-20240110170904148" style="zoom:60%;" />

---

#### Quantitative Relationships

MOSFET은 Electrical Energy의 기울기에 영향을 받는 소자이므로 $J_{Diff}$는 무시할 수 있다.  $\therefore$ $J = \rho  v_d=nq\mu E $

1. $n \text{은 } V_G \text{에 의해 결정된다.} E \text{는 } V_{SD} \text{에 의해 결정된다.}$

2. Source, Drain 전극 사이에 p-Si Substrate와 Depletion region이 생긴다. 따라서, $V_{SD}$ 가 커짐에 따라 Drain과 p-Si Substrate 사이에 depletion region이 커지고 이에 따라 channel에 길이가 짧아진다. 그러나 짧아지더라도 전기장으로 인해 $I_{sat}$ 로 흐른다.

3. $V_G$ 에 $V_T$ 이상을 가해줘야 전류가 흐른다.  16단원의 (7)식을 통해 다음을 알 수 있다.

$$
V_T = \phi_{semi}+ \phi_{oxi}=\phi_F + \frac{K_S}{K_O}t_o \sqrt{\frac{4qN_A}{K_S \epsilon _0}\phi_F}
$$
**MOSFET Mobility**

<img src="/images/figure/image-20221227102838295.png" alt="image-20221227102838295" style="zoom:80%;" />

Channel 에서의 전자는 surface 쪽으로 많은 drift current(힘)을 받는다.

따라서 scattering이 많이 발생하므로, effective mobility를 새로 정의해야한다.
$$
\bar{\mu}_n ~\text{or}~ \bar{\mu}_p = \text{effective mobility} = \text{average mobility of the inversion layer carriers}
$$

<img src="/images/figure/image-20221227103234903.png" alt="image-20221227103234903" style="zoom:67%;" />
$$
\begin{align}
&\text{Channel까지} ~x = 0~ ~ x =~ x_c\text{까지의 가중치를 통한 평균 mobility를 의미한다.}
\\
&\bar{\mu}_n = \frac{\int ^{x_e(y)} _0 \mu _n (x,y) n (x,y) dx}{\int ^ {x_e(y)} _0 n(x,y) dx}= - \frac{q}{Q_N(y)}\int ^{x_e(y)} _0 \mu _n (x,y) n (x,y) dx : \text{y에 대한 함수로 mobility가 나온다.}
\\
\end{align}
$$

**Quantitative Relationship**
$$
\begin{align}
&\text{가정}
\\
&\text{1. channel은 drift에 의한 것이 많다고 생각할 수 있다.}
\\
&\text{2. Channel이 길면 y에 대한 dependency를 없앨 수 있다.}
\\
&\text{3. x = 0+ 에서 current가 많이 흐를 것이다.} \to \text{x dependency를 없앨 수 있다.}
\\
&J_N \approx J_{N,y} \approx q \mu _n n E_y = -q \mu _n n\frac{d \phi}{dy}
\end{align}
$$

$$
\therefore I_D = - \int \int J_{Ny} dx dz = \left(-Z\frac{d\phi}{dy}\right) \left(-q \int ^{x_c(y)} _{0} \mu _n(x,y) n(x,y) dx\right)
$$

가정 3을 통하여 다음을 얻을 수 있다.
$$
\begin{align}
&I_D = -Z\bar{\mu}_n Q_N\frac{d\phi}{dy}
\\
&\text{양변을 z에 대해 적분하면 다음과 같다.}
\\
&\int^{L}_0 I_D ~dy = \int^{L}_0 -Z\bar{\mu}_n Q_N\frac{d\phi}{dy} dy
\\
&I_D L = \int^{V_D}_{V_S} -Z\bar{\mu}_n Q_N d\phi
\\
&I_D = - \frac{Z \bar{\mu}_n}{L}\int^{V_D}_{V_S}Q_n d\phi
\\
&\therefore Q_n\text{이 channel에 얼마나 있는지를 구하면 된다.}
\end{align}
$$
Charge에 대해 구하기 위해 생각해보면 Mos 에서 배운 식 + Source, Drain에서의 상황을 이용하면 된다.
$$
\begin{align}
&V_G = \phi_S(y) + \phi_{oxi}=\phi_S(y)+ \frac{Q_G}{C_0} = \phi_S(y) - \frac{Q_N + Q_{depl}}{C_0}
\\
&\therefore Q_N = -C_0[V_G - \phi_S(y)] - Q_{depl}
\\
\\
&\text{1) At the onset inversion}
\\
&\text{MOS에서} \phi_S = 2 \phi_F
\\
&\text{MOSFET에서는 Source, Drain 영향으로} ~\phi_S (y) = 2\phi_F + V(y)
\\
&2) ~Q_{depl} = -qN_AW_T(y) = -QN_A\sqrt{\frac{2k_S \epsilon _0\{2\phi_F + V(y\}}{qN_A}} = -\sqrt{2k_S\epsilon _0 qN_A\{2\phi_F+V(y\}}
\\
\\
&\text{이를 대입하면 다음과 같다.}
\\
&Q_N = -C_0\{V_G - 2\phi_F - V(y) \} + \sqrt{2k_s \epsilon_0q N_A\{2\phi_F+V(y\}}
\end{align}
$$
**Sqaure-Law Theory**

위의 식을 다시 쓰면 다음과 같다.
$$
\begin{align}
&Q_N = - C_0\{V_G - 2\phi_F - V(y) + \frac{Q^0_{depl}}{C_0}\}
\\
&Q^{0}_{depl} = \sqrt{2k_S\epsilon_0 q N_A \{2\phi_F \}}\text{의 형태로 y dependency가 없다고 정의하자. : Square-Law Theory}
\\
\\
&V_T = 2\phi_F - \frac{Q^0_{depl}}{C_0}
\\
&\therefore Q_N = -C_0\{V_G -V_T - V(y)\}
\\
\\
&I_D = - \frac{Z \bar{\mu}_n}{L}\int^{V_D}_{V_S}Q_n d\phi_S
\\
&\phi_S(y) = 2\phi_F+V(y)\text{에서} ~~d\phi_s(y) = dV(y)
\\
&\therefore I_D = - \frac{Z \bar{\mu}_n}{L}\int^{V_D}_{V_S}Q_n dV
\\
&\therefore I_D = - \frac{Z \bar{\mu}_n C_0}{L} \{(V_G-V_T)V_D - \frac{V_D ^2}{2}\}
\end{align}
$$
따라서, 다음의 그래프에 대해 다음과 같이 해석할 수 있다.

<img src="/images/17. MOSFETs-The Essentials/image-20240110170904148.png" alt="image-20240110170904148" style="zoom:60%;" />

For small drain voltages
$$
\begin{align}
&I_D = - \frac{Z \bar{\mu}_n C_0}{L} (V_G-V_T)V_D
\\
&\text{conductance} = \frac{\partial I_D}{\partial V_D} = - \frac{Z \bar{\mu}_n C_0}{L} (V_G-V_T) = \text{constant}
\\
&\text{의미 :}~ V_G - V_T : \text{charge density}
\\
&\text{의미 :}~ V_D : \text{Volatge 조절}
\\
\\
&\therefore V_G\text{가 클수록 기울기가 가파르다.}
\\
&
\end{align}
$$
For large drain voltages
$$
\begin{align}
&\therefore I_D = - \frac{Z \bar{\mu}_n C_0}{L} \{(V_G-V_T)V_D - \frac{V_D ^2}{2}\}
\\
&\text{conductance} = \frac{\partial I_D}{\partial V_D} = - \frac{Z \bar{\mu}_n C_0}{L} (V_G-V_T - V_D) = \text{constant}
\\
&V_D = V_G - V_T\text{가 되는} ~V_D\text{값이}~ V_G\text{값이 증가함에 따라 커진다.}
\\
\\
&V_D\text{가} ~\text{Saturated}\text{되었을 때}
\\
&Q_N(L) = -C_0\{V_G - V_T- V_{Dsat} \} = 0 ~ L = V_{Dsat}
\\
&V_{Dsat} = V_G - V_T
\\
&I_{Dsat} = \frac{Z \bar{\mu}_n C_0}{2L} (V_G-V_T)^2
\\
&\text{이 식에서 mobility 값을 추출할 수 있다.}
\end{align}
$$
따라서, MOSFET에서 그림을 그리는 방법이 총 3가지이다.

1) $I_D$ - $V_D$ : Transistor 작동에 대해, mobility를 구하기 위해
2) $\sqrt{I_D}$ - $V_G$ : $V_T$ 값을 구하기 위해, on-off ratio를 구하기 위해
3) $logI_D$ - $logV_G$ : mobility를 구하기 위해

**Bulk Charge Theory**

Square-Law theory와 다르게 $V(y)$ 를 그대로 사용하는 것
$$
\begin{align}
&I_D = - \frac{Z \bar{\mu}_n}{L}\int^{V_D}_{V_S}Q_n d\phi
\\
&I_D = \frac{Z \bar{\mu}_n C_0}{L} \int^{V_D}_{V_S}\{(V_G - 2\phi_F-V)- \frac{\sqrt{2k_s\epsilon_0qN_A(2\phi_F+V)}}{C_0}\}dV
\\
&I_D = \frac{Z \bar{\mu}_n C_0}{L}\{(V_G - 2\phi_F -\frac{V_D}{2})V_D-\frac{2}{3}\frac{\sqrt{2k_s\epsilon_0qN_A}}{C_0}[(V_D+2\phi_F)^{3/2}-(2\phi_F)^{3/2}] \}
\\
&\text{이를 Taylor series 전개하면 된다.}
\end{align}
$$

---

#### Small-Signal Characteristics

At low frequency

-1) Minority Carrier detect X

-2) Majority Carrier detect O

<img src="/images/17. MOSFETs-The Essentials/image-20240112102637197.png" alt="image-20240112102637197" style="zoom:80%;" />

At high frequency

-1) Minority Carrier detect X

-2) Majority Carrier detect O

<img src="/images/17. MOSFETs-The Essentials/image-20240112102718161.png" alt="image-20240112102718161" style="zoom:80%;" />

