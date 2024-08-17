---
layout: single
title: "7)Small signal admittance"
typora-root-url: ../
categories : "Fundamental-of-Semicondutor"
tag : diode
#tag : [me, me2, me3]
toc : true
toc_sticky : true
author_profile : false
---
## Fundamental of semiconductor

기본 개념을 먼저 정리해야한다. 

#### Phasor

Sinusoidal driving force 에 의해 움직이는 harmonic oscillator를 생각해볼 수 있다.
$$
X_{SS}(t) = X_0 cos(wt + \delta ) = Re\left\{X_0 e^{-i(wt + \delta)} \right\} = Re\left\{\tilde X_{SS}~e^{-iwt}\right\}
$$
본래의 $X_{SS}(t)$는 변수 $X_0$, $w$ , $\delta$ 로 이루어져있다. 그러나, Phasor의 개념을 도입하면 변수 $\tilde{X}_{SS}$ 와 w의 변수로 나눌 수 있다.

따라서 Phasor는 시간변수를 독립변수로 만들기 위해 도입해졌다.

#### Linear System

<img src="/images/figure/image-20221226152503091.png" alt="image-20221226152503091" style="zoom:150%;" />
$$
\frac{\tilde{V}}{\tilde{I}} = Z : \text{Impedence  / Resistance}
\\
\frac{\tilde{I}}{\tilde{V}} = Y : \text{Admittance  / Conductance}
$$
이러한 Input-Out System 에서 $V_1 + V_2$ --> $I_1+I_2$ 에 대응되면 이는 Linear System이다.

Linear system이란?

--> input을 a+b를 넣으면 output이 c+d가 나오는 것

---

#### Small Signal 분석

DC Voltage에 small signal인 V를 미소량 AC로 가해주어 Capacitance를 측정한다. 

미소량 AC를 가해주어 측정하는 이유는 이에 대해서만 Linear System이 작동하고, DC와 AC에 대해서는 Linear System이 작동하지 않기 때문이다. 

$Y= jwC + G$ 로 표현이 가능하다. minority carrier가 capacitance 역할을 하기 때문이다.

다이오드를 이에 따라 그림으로 나타내면 다음과 같다.

<img src="/images/figure/image-20221226153314183.png" alt="image-20221226153314183" style="zoom:80%;" />

* Capacitance와 Conductance에 화살표는 '가변'을 의미한다. $C = C(V_A)$, $G = G(V_A)$
* 다이오드에 대한 Reverse Bias에서 다음과 같이 모델을 만들 수 있다. ( 전류의 관점에서 $C + G$ )

#### Reverse - Bias C-V measurement

$V_A > 0$이면 depletion width가 줄어든다. $V_A < 0$ 이면 depletion width가 커진다.

1) ***$V_A < 0$인 상황에서 살펴보자.***



<img src="/images/figure/image-20221226154015726.png" alt="image-20221226154015726" style="zoom:80%;" />

 따라서 다음의 그림에서 $C = \frac{dQ}{dV}$ 를 구해야 하는데, 흔히 알고 있는 parallel capacitor model을 사용하여 C를 구할 수 있다.
$$
C = K \epsilon_0 \frac{A}{W} 
\\
\text{이 때, 7단원에서 depletion width에 관한 식을 구했었다.}
\\
\text{Step Junction : } W = \left[\frac{2K_s \epsilon _0}{qN_B}(V_{Bi}-V_{A})\right]^{1/2}
\\
\text{Linearly graded Junction : } W = \left[\frac{12K_s \epsilon _0}{qa}(V_{Bi}-V_{A})\right]^{1/3}
$$
따라서, 이를 C에 대입하면 다음과 같다.
$$
N_B(x) = bx^m \text{일 때}
\\
C_J = \frac{K_S \epsilon _0 A}{\left[ \frac{(m+2)K_S \epsilon _ 0}{qb} (V_{Bi}- V_A)\right]^{1/(m+2)}}
$$
C-V measurement를 통해 Doping Profile을 알 수 있다.
$$
N_B(x) = \frac{2}{qK_S \epsilon _0 A^2 \vert d(1/C^2_j)/dV_A \vert}
\\
x = \frac{K_s \epsilon _ 0 A}{C_j}
\\
\text{(4)식을 통해서} d(1/C^2 _j)/dV_A \text{의 기울기를 구할 수 있다. 이때 x 에 대해} ~N_B, C_j\text{를 구할 수 있다.}
\\
\text{즉 x에 대한 Doping Profile을 구할 수 있다.}
$$


#### Reverse-Bias Conductance

conductance는 정의에 의해 다음과 같이 나타낸다.
$$
G = \frac{dI}{dV_A}
\\
\text{DC이므로 Voltage 변화가 없지만 I-V 그래프에서 기울기를 나타내는 것이다.}
$$
따라서, $I = I_0\left[e^{(qV_A /kT)} -1\right]$이므로 이를 미분해주면 다음을 얻을 수 있다.
$$
G_0 = \frac{q}{kT}I_0 e^{qV_A /kT} = \frac{q}{kT}(I + I_0) \text{ in Ideal diode}
\\
G_0 = \frac{d}{dV_A}\left(-\frac{qAn_i}{2\tau _0}W\right) = \frac{qAn_i W/2 \tau _0}{(m+2)(V_{Bi} - V_A)} \text{~in~} I_{R-G}\text{ dominant}
$$

#### Forward-Bias Diffusion Capacitance & Admittance

 majority carrier의 경우 (4)식에 대입하면 된다. 그러나, Reverse-Bias와는 다르게 minority carrier도 고려를 해야한다.

<img src="/images/figure/image-20221226173229656.png" alt="image-20221226173229656" style="zoom:70%;" />

steady-state일 때는 기울기가 직선을 갖는다. 그러나, AC에서는 minority carrier의 lifetime보다 AC에 걸리는 시간이 짧으면 minority carrier가 oscillate 한다.

minority carrier가 oscillate 한다는 것은 $\triangle V$가 $\triangle Q$와 out-of-phase 라는 것이고, $\triangle Q$ 는 $I$와 Out-of-phase 관계 이므로 결과론적으로 Admittance를 증가시킨다. 따라서, 이러한 사실들을 다음 그림으로 modeling 할 수 있다.



<img src="/images/figure/image-20221226173557173.png" alt="image-20221226173557173" />
$$
C_J : \text{junction Capacitor} \rightarrow \text{In Phase : majority carrier}
\\
C_D : \text{Diffusion Capacitor} \rightarrow \text{In Phase : minority carrier}
\\
G_D : \text{Diffusion Admittance} \rightarrow \text{Out of Phase : minority carrier}
$$


---

#### Quantitative analysis

$p^+ n $ junction을 생각해보자.

상황 : n-side minority carrier가 $V_a +v_a$ 에 의해 영향을 받고 있다.
$$
\delta p_n(x,t) = \bar{p_n}(x) + p_{n,ac}(x,t)
$$
$\delta p_n(x,t)$ 는 continuity equation을 만족시켜야한다.
$$
\frac{\partial \delta p_n(x,t)}{\partial  t} = D_n \frac{\partial ^2 ~\delta p_n(x,t)}{\partial x^2}-\frac{\delta p_n(x,t)}{\tau}
$$
생각해야되는 것 

1. 지금 우리가 보고 있는 것은 Steady-state가 아닌 General한 식을 보고 있다.
2. Diffusion current가 Drift current보다 훨씬 많은 상황을 여기고 있다.

(9)를 (10)에 대입하고 DC current와 AC current를 분리하면 다음을 알 수 있다.
$$
\begin{align}
\\
&0 = D_n\frac{\partial ^2 \bar{p_n} (x)}{\partial x^2}- \frac{\bar{p_n}(x)}{\tau_p}
\\
&\frac{\partial p_{n,ac}(x,t)}{\partial t} =  D_n \frac{\partial ^2  p_{n,ac}(x,t)}{\partial x^2}-\frac{p_{n,ac}(x,t)}{\tau}
\end{align}
$$
(17)식을 Phasor로 나타내어 보자.

편미분 방정식의 형태이므로, phasor는 공간에 대한 함수로 나타난다. 

<img src="../friedtiger/friedtiger.github.io/images/7. pn Junction Diode Small-Signal Admittance/image-20231218230151693.png" alt="image-20231218230151693" style="zoom: 80%;" />

각 점마다의 phasor가 있다고 생각하면 편하다.
$$
j \omega \tilde{p}_{n,ac}(x,t) = D_n \frac{\partial ^2 \tilde{p}_{n, ac}(x,t)}{\partial x^2} - \frac{\tilde{p}_{n,ac}(x,t)}{\tau}
$$
(14)를 통해 정리하면 (12), (13)식을 다시 다음과 같이 나타낼 수 있다.
$$
\begin{align}
\\
&0 = D_n\frac{\partial ^2 \bar{p_n} (x)}{\partial x^2}- \frac{\bar{p_n}(x)}{\tau_p}
\\
&0=  D_n \frac{\partial ^2  p_{n,ac}(x,t)}{\partial x^2}-\frac{p_{n,ac}(x,t)}{\tau_p/(1+j\omega \tau _p )}
\end{align}
$$
(17)에 대해 Boundary condition은 다음과 같다.
$$
\begin{align}
\\
&x_{\infty} \rightarrow \bar{\delta p_n}(\infty) = \tilde{p}_{n,ac}(\infty) = 0
\\
&x = x_n \rightarrow \delta p_n(x,t) = \bar{\delta p_n}(x_n) + p_{n,ac}(x_n,t) = \frac{n^2 _i}{N_d}(e^{q(V_a+v_a)/kT}-1) : \text{junction의 법칙}
\end{align}
$$
$V_a$ 와 $v_a$의 식을 구별해야하므로 (23)의 식을 linearize해야 한다.

따라서, $v_a << V_a$ 의 상황을 가정하고 Taylor series를 전개해야한다.
$$
\begin{align}
\\
&\text{Let's } ~ x = \frac{v_a}{V_a}
\\
&f(x) = \frac{n^2 _i}{N_d}(e^{q(V_a+v_a)/kT}-1) = \frac{n^2 _i}{N_d}(e^{qV_a(1+\frac{v_a}{V_a})/kT}-1) = \frac{n^2 _i}{N_d}(e^{qV_a(1+x)/kT}-1)
\\
&f(x) = f(0) + f'(0)x
\\
&f(x) = \frac{n^2 _i}{N_d}(e^{q{V_a}/kT}-1) + \frac{qv_a}{kT}e^{qV_a/kT}
\\
&\therefore \delta p_n(x,t) =  \bar{\delta p_n}(x_n) + p_{n,ac}(x_n,t) = \frac{n^2 _i}{N_d}(e^{q{V_a}/kT}-1) + \frac{qv_a}{kT}e^{qV_a/kT}
\end{align}
$$
Bundary condition, 미분 방정식을 모두 구했으므로 풀면 다음과 같다.
$$
\begin{align}
\\
&\text{DC current : } I = -qAD_p\frac{\partial \bar{\delta p_n}(x)}{\partial x}\vert_{x_n}= qA \sqrt{\frac{D_p}{\tau _p}}\frac{n_i ^2}{N_d}(e^{qV_a/kT}-1) 
\\
&\text{AC current : } \tilde{I} = -qAD_p\frac{\partial \tilde{\delta p_n}(x)}{\partial x}\vert_{x_n}= qA \sqrt{\frac{D_p}{\tau _p}}\frac{n_i ^2 q v_a}{N_d k T}(e^{qV_a/kT})\sqrt{1+j\omega\tau _p}
\end{align}
$$
이를 Admittance로 표현하면 다음과 같다.
$$
Y = \frac{\tilde{I}}{\tilde{v_a}} = qA \sqrt{\frac{D_p}{\tau _p}}\frac{n_i ^2 q}{N_d k T}(e^{qV_a/kT})\sqrt{1+j\omega\tau _p} = I_0\frac{q}{kT}e^{qV_a/kT}\sqrt{1+j\omega\tau _p} = G_0\sqrt{1+j\omega\tau _p}
$$
이를 그래프로 나타내면 다음과 같다,

<img src="../friedtiger/friedtiger.github.io/images/7. pn Junction Diode Small-Signal Admittance/image-20231219000305822.png" alt="image-20231219000305822" style="zoom:80%;" />
