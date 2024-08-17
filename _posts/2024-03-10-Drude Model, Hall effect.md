---
layout: single
title: "2)Drude Model-Hall Effect"
typora-root-url: ../
categories : "Solid-State-Physics"
tag : [drude, hall]
#tag : [me, me2, me3]
toc : true
toc_sticky : true
author_profile : false
---
## Solid State Physics

전기장과 자기장 / 전하와 자기장의 관계가 있다는 것이 알려졌음.

전류와 자기장의 관계를 알고싶어 실험을 진행함.

<img src="/images/2. Hall effect from Drude/image-20240325135141851.png" alt="image-20240325135141851" style="zoom:67%;" />
$$
\begin{align}
&\text{Lorentz force} : F = q(\vec{v} \times \vec{B})
\\
&\text{1. q는 전자의 입장에서 -e이므로 전자는 -y축으로 힘을 받아 움직인다.}
\\
&\text{2. -y축으로 축적된 전자는 y축으로 향하는 전기장을 만들어 낸다.} 
\\
\\
&\text{이를 종합하여 나타내면 2의 전기장을 다음처럼 나타낼 수 있다.}
\\
&\vec{E} = -R_H (\vec{J} \times \vec{B}) ~~, R_H : \text{Hall coefficient}
\end{align}
$$

---

#### Electron momentum in Hall effect in D.C. Current

전자의 움직임을 다루기위해 운동량 방정식을 구성해야한다.
$$
\begin{align}
&\frac{dp(t)}{dt} = - \frac{p(t)}{\tau} + F(t) ~\cdot \cdot ~\cdot \text{Drude Model}
\\
& F = - e(\vec{E} + \vec{v} \times \vec{B}) = -e(\vec{E}+ \frac{1}{m}\vec{p} \times \vec{B})
\\
\\
&\text{In steady-state, y-axis에서 평형을 이루어야한다.}
\\
&\text{외적하면 다음과 같다.}
\\
&-\frac{m\vec{v}_y}{\tau} - e(\vec{E}_y - \vec{v}_x \vec{B}) = 0
\\
&\vec{v}_y = 0 , \vec{E}_y - \vec{v}_x \vec{B} = 0 \rightarrow \vec{E}_y  =  \vec{v}_x \vec{B}
\\
\\
&\text{이를 Hall coefficient와 결합하여 정리하여 나타내면 다음과 같다.}
\\
&R_H = \frac{\vec{E}_y}{\vec{J}_x \vec{B}} = \frac{\vec{v}_x \vec{B}}{- n e\vec{v}_x \vec{B}} = -\frac{1}{ne}
\end{align}
$$
결론 : 

- Hall coefficient는 $\vec{E} = -R_H (\vec{J} \times \vec{B})$ 에서 Input과 Output이 얼마나 비례하는지를 나타낸다. Hall coefficient는 Carrier 농도에 대해 반비례한다.

  이유 : Hall effect($\vec{E}$)는 $\vec{E}_y - \vec{v}_x \vec{B}$에 의해   $\vec{v}_x$에만 비례하기 때문에 Current Density($J$​​)에서 carrier 농도를 나누어 줘야한다.

- Hall coefficient는 Carrier의 속도와는 관련이 없다. 

  이유 : Carrier의 속도가 크다는 것은 'Input이 크다'라는 것이고, 'Input이 크면 Output도 크다'이므로 비례관계가 성립하는 상황이기 때문이다.



실제와 다른 점 :

- Hall coefficient는 자기장(B)와 온도(T)에 대해 dependent 성분을 갖는다.

---

#### Electron momentum in Hall effect in A.C. Current

$$
\begin{align}
&\frac{dp(t)}{dt} = - \frac{p(t)}{\tau} + F(t) ~\cdot \cdot ~\cdot \text{Drude Model}
\\
\\
&\text{A.C. Current는 다음과 같이 표현 가능하다.}
\\
&\vec{E}(t) = \text{Real}[\tilde{E}(\omega)e^{j \omega t}]
\\
& F = - e\vec{E}(t) = -e ~\text{Real}[\tilde{E}(\omega)e^{j\omega t}]
\\
\\
&\text{이를 종합하여 phasor notation으로 나타내면 다음과 같다.}
\\
& \tilde{p}(\omega) = - (\frac{e}{j \omega + \frac{1}{\tau}})\tilde{E}(\omega)
\\
\\
&\text{A.C. Current는 다음과 같다.}
\\
&J(t) = \text{Real}[\tilde{J}(\omega) e^{j\omega t}]
\\
&\tilde{J}(t)= - n e \tilde{v}(\omega) = -ne\frac{\tilde{p}(\omega)}{m}
\\
\\
&\text{이를}~\tilde{p}(\omega)\text{와}~\tilde{J}(t)\text{를 결합하여 나타내면 다음과 같다.}
\\
&\tilde{J}(\omega) = -\frac{ne}{m}\frac{e \tilde{E}(\omega)}{j\omega + \frac{1}{\tau}}
\\
&\text{따라서, Conductivity 정의를 통해 다음으로 나타낼 수 있다.}
\\
&\sigma(\omega) = \frac{\frac{ne^2\tau}{m}}{1+j\omega \tau} = \frac{\sigma _0}{1+j\omega\tau} : \text{Frequency-dependent AC conductivity}
\end{align}
$$

1) A.C. Current로 인한 전자기파 중 H-field에 의한 영향을 F에 무시할 수 있는 이유

- 전자기파 이론에 따르면 전기장의 에너지와 자기장의 에너지는 같다. 

이를 통해 계산하면, $\vec{B} = \frac{\vec{E}}{c}$ 이므로 자기장은 전기장보다 $10^8$ 만큼 작다. 따라서 무시할 수 있다. 

만약, 빛의 속도가 아닌 전자의 속도를 고려해도 자기장의 크기는 많이 작다.

2. A.C. Current를 Harmonic Oscillator로 고려할 때, 위치에 대한 성분을 고려하지 않아도 되는 이유

- A.C Current의 파장(가시광선)이 Drude model mean free path(평균 이동거리)보다 한참 길다. 

따라서, Drude model mean free path를 생략해서 고려해도 된다. 

따라서, 전자가 특정 r position에 있을 때 $\vec{E}(r,t)$​를 생각하면 된다. 



Complex permittivity를 보는 관점 2가지

<img src="/images/2. Hall effect from Drude/image-20240326113049174.png" alt="image-20240326113049174" style="zoom:50%;" />

<img src="/images/2. Hall effect from Drude/image-20240326112537922.png" alt="image-20240326112537922" style="zoom:50%;" />

1)  Frequency가 작은 microwave 등에서는 자유전자가 금속에서 $\omega$에 반응하는 것으로 생각할 수 있고 이는 $\sigma$로 정의할 수 있다.
2) Frequency가 큰 optical wave 등에서는 전자가 금속 원자핵에 속박되어있다고 생각할 수 있고(polarization) 이는 $\epsilon^{''}$ 로 정의할 수 있다. 



자유전자로 생각하고 식을 이어나가보자.
$$
\begin{align}
&\triangledown \times \tilde{H} = \tilde{J} + j \omega \epsilon \tilde{E} = ( \sigma + j \omega \epsilon)\tilde{E} = j \omega (\epsilon + \frac{\sigma}{j \omega})\tilde{E} \equiv j \omega \epsilon _c \tilde{E}
\\
&\therefore \epsilon _c = \epsilon + \frac{\sigma}{j \omega}
\\
&\text{위 식에 의하여} ~\sigma(\omega) = \frac{\sigma _ 0}{1+j\omega \tau}
\\
\\
&\text{대부분 상황에서 high frequency로 가정하자.}~\omega \tau ~\rangle\rangle 1
\\
& \epsilon _c = \epsilon + \frac{\sigma}{j \omega} =\epsilon + \frac{\sigma _0/j\omega\tau}{j\omega} = \epsilon - \frac{\sigma _0 }{\omega^2 \tau} = \epsilon (1 - \frac{\sigma _0}{\omega ^2 \epsilon\tau })
\\
&\omega _p^2 = \frac{\sigma _0}{\epsilon \tau}\text{라고 정의하면 다음으로 나타낼 수 있다.}
\\
&\epsilon _c = \epsilon (1-\frac{\omega _p ^2}{\omega^2})
\\
&\text{위 식에 의하여}
\\
&\omega_p ^2 = \frac{\sigma _ 0}{\epsilon \tau} = \frac{ne^2 \tau /m}{\epsilon \tau} = \frac{n e^2}{m \epsilon}
\end{align}
$$
전자기파에서 다음이 성립한다는 것을 알 수 있다.
$$
k_c = \omega \sqrt{\mu \epsilon _c}
$$
따라서, 다음을 정의내릴 수 있다.
$$
\begin{align}
&\text{Case 1 : }\omega ~\langle ~\omega_p
\\
&\epsilon_c = \epsilon (1-\frac{\omega _p ^2}{\omega^2}) <0
\\
&\therefore k_c \text{는 imaginary}
\\
&\text{Plasma frequency보다 에너지가 낮은 전자기파는 흡수된다.}
\\
\\
&\text{Case 2 : } \omega ~\rangle ~\omega_p
\\
&\epsilon_c = \epsilon (1-\frac{\omega _p ^2}{\omega^2}) > 0
\\
&\therefore k_c \text{는 실수}
\\
&\text{Plasma frequency보다 에너지가 낮은 전자기파는 통과된다.}
\\
\\
&\text{이러한 가정들이 Alkali metal에는 잘 적용됨.}
\end{align}
$$
