---
layout: single
title: "5)Magnetic Fields in Matter"
typora-root-url: ../
categories : "Electromagnetic"
tag : field
#tag : [me, me2, me3]
toc : true
toc_sticky : true
author_profile : false
---
## Electromagnetic 

전자는 Spin을 가지고 있다. 따라서 물질에서 자기장의 근원은 전자의 움직임이다.

그렇다면 왜 전기장의 dipole 과는 다르게 모든 magnetic dipole 들이 한방향으로 정렬하지는 않는걸까? 

--> 모든 전자들의 spin을 고려하는 것이 아닌  홀전자의 spin만을 고려하게 되니까. 약해서(?)



Magnetic Dipole은 어떻게 생각해야될까?

<img src="/images/figure/image-20230622115856348.png" alt="image-20230622115856348" style="zoom:80%;" />

Magnetic Dipole은 Electric Dipole과는 다르게 Monopole이라는 것을 상상할 수 없다. 

따라서, Electric dipole의 model을 따라서 Gilbert model을 쓰는 것보다

Ampere model인 전자의 loop를 상상하는 것이 좋다. 그러나 직관성을 위해서는 Gilbert model을 사용하는 것도 좋다.

---

#### Effect of a Magnetic Field on Atomic Orbits

자기장이 존재하는 상황에서 전자의 궤도 운동은 어떻게 바뀔 수 있을까?

<img src="/images/figure/image-20230622131858677.png" alt="image-20230622131858677" style="zoom:67%;" />
$$
\begin{align}
\text{쿨롱 힘} &= \text{구심력 이므로}
\\
\frac{1}{4 \pi \epsilon _0} \frac{e^2}{R^2} &= m_e \frac{v^2}{R}
\\
 \text{If, 자기장이 z축 방향으로 } &\text{존재하고 있는 상황을 가정해보자.}
\\
\text{전자가 Loop에 중심}&\text{방향으로 힘을 받으므로}
\\
\text{쿨롱의 힘이 더 쎄져} &\text{manetic moment의 값은 더 커진다.}
\end{align}
$$
즉, 자기장과 반대방향으로 magnetic moment가 더 커질 수 있다. --> Dielectric이 존재할 수 있는 간접적인 이유가 된다.

---

#### Magnetization

polarization과 마찬가지로 단위 부피에 대한 magnetic dipole로 구할 수 있다.
$$
M \equiv \text{Magnetic dipole moment per unit volume}
$$
이를 수식적으로 살펴보자
$$
\begin{align}
\vec{A}(r) &= \frac{\mu _0}{4 \pi}\frac{\vec{m}\times \hat{\eta}}{\eta ^2} \text{in field with single dipole}
\\
\vec{A}(r) &= \frac{\mu_0}{4 \pi}\int \frac{\vec{M}(r^{'}) \times \hat{\eta}}{\eta ^2} d\tau^{'} \text{in magnetized object}
\\
&= \frac{\mu_0}{4 \pi}\int \frac{1}{\eta}[\triangledown ^{'} \times \vec{M}(r^{'})]d\tau^{'} + \frac{\mu _0}{4 \pi}\oint \frac{1}{\eta}[\vec{M}(r^{'})\times d\vec{a}^{'}]
\end{align}
$$
따라서, polarization과 마찬가지로 다음처럼 생각할 수 있다.
$$
\vec{J_b}= \triangledown \times \vec{M}
\\
\vec{K_b} = \vec{M} \times \hat{n}
$$
만약 $\triangledown \cdot P = -\rho_b = 0$ 처럼 $\triangledown \times \vec{M} = \vec{J_b}=0$ 이라면 다음처럼 겉 표면에 current loop로 생각해볼 수 있다.

​                                     <img src="/images/figure/image-20230622142355640.png" alt="image-20230622142355640" style="zoom:80%;" /> <img src="/images/figure/image-20230622142404114.png" alt="image-20230622142404114" style="zoom:80%;" />



그렇다면 $\triangledown \times \vec{M} = \vec{J_b}\neq 0$ 은 어떤 상황일까?

다음처럼, 전류를 생각한 방향(x축)과 수직으로 $\vec{M}$ (y축 or z축)이 non-uniform 하게 있을 때를 생각해볼 수 있다.

<img src="/images/figure/image-20230622143437447.png" alt="image-20230622143437447" style="zoom:67%;" />

---

#### The Auxiliary field H

위의 식을 통해 source를 $\vec{J} = \vec{J_b} + \vec{J_f}$ 로 나누어 생각할 수 있다.
$$
\begin{align}
\triangledown \times B &= \mu_0 J
\\
&=\mu_0(J_f + J_b)
\\
&=\mu_0(J_f + \triangledown \times \vec{M})
\\
\\
&\triangledown\times (\frac{1}{\mu _0}B - M) = J_f
\\
\therefore ~~& H \equiv \frac{1}{\mu _0}B - \vec{M}
\end{align}
$$
$\vec{H}$ 는 $\vec{D}$ 와 마찬가지로 물질 내에서의 free source로 인해 서술하는 field로 해석할 수 있다.

예시)

<img src="/images/figure/image-20230622144214591.png" alt="image-20230622144214591" style="zoom:50%;" />

diamagnetic 물질인 Cu에서 아래에서 위로 전류가 흐르는 모습을 상상해보자. 자기장이 어떻게 작아지는지 상상해봐야 한다.

<img src="/images/figure/image-20230622144409793.png" alt="image-20230622144409793" style="zoom:67%;" />

다음처럼 생각할 수 있다.

1. 내부에서 r에 따라 자기장의 세기가 다름
2. 자기장의 세기가 다르고, diamagnetism이므로 $\vec{M}$이 바깥쪽에서 크다는 사실을 알 수 있음. 즉, $\triangledown \times \vec{M} = J_b$이 존재하는 것을 알 수 있다.
3. $J_b$를 해석하면 r이 커질수록 $J_b$가 커지는 상황을 생각해 볼 수 있다.

---

#### Magnetic Susceptibility

전기장에서 $\vec{P} = \chi _e \vec{E}$ 의 관계를 가졌다. by LTI system 

자기장에서 $\vec{M} = \chi_m \vec{B}$ 의 관계를 똑같이 생각할 수 있지 않을까? $\rightarrow$ X
$$
\begin{align}
\\
D = \epsilon_0 E + P &\rightarrow P = \chi_e E
\\
B = \mu_0H +M &\rightarrow M = \chi_m H
\\
\text{의 개념으로 } &\text{이해할 수 있다.}
\end{align}
$$
예시)

상황 : infinite solenoid. susceptibility : $\chi_m$

<img src="/images/figure/image-20230623001302477.png" alt="image-20230623001302477" style="zoom:67%;" />
$$
\begin{align}
&1. M = \chi_m H \text{을 자연스럽게 머릿속에 그림이 그려저야한다.}
\\
&2. H = nI \hat{z} \text{: Ampere's law에 의하여}
\\
&3. B=\mu_0H + M = \mu_0 nI\hat{z} + \chi_mnI\hat{z} = \mu_0(1+\chi_m)nI\hat{z} \text{: 내부 } J_b\text{은 상쇄된다.}
\end{align}
$$


