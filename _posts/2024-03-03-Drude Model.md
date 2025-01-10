---
layout: single
title: "1)Drude Model"
typora-root-url: ../
categories : "Solid-State-Physics"
tag : drude
#tag : [me, me2, me3]
toc : true
toc_sticky : true
author_profile : false
---
## Solid State Physics

<img src="/images/1. Drude Model/image-20240310175340416.png" alt="image-20240310175340416" />

가정

1. 충돌전에 여러 힘들은 무시된다.

- Independent electron approximation : 전자-전자 상호작용은 일어나지 않는다.

- Free electron approximation : 전자-이온 상호작용은 일어나지 않는다. (No binding Force)

2. Electron scattering : 전자 - 이온 충돌이 순간적으로 일어난다.

<img src="/images/1. Drude Model/image-20240310175736660.png" alt="image-20240310175736660" />

- 전자들이 충돌하고나서 속도는 온도에 의해 결정된다. : 열역학 법칙을 따른다.(따라서, electron gas model)
- 전자들의 충돌시간은 1/시간 의 확률로 나타낼 수 있다. :  $1 / \tau [s^{-1}]$

---

#### Current Density

Current density는 charge의 flux이므로 
$$
\bold{J} = - n e \langle v \rangle
$$
전기장이 존재하는 상황에서 평균 속도는 다음과 같이 나타낼 수 있다.
$$
\langle v \rangle = \langle v_0 \rangle - \frac{eE \langle t \rangle}{m} = - \frac{eE \tau}{m}
$$
따라서 이를 종합하면 다음과 같다.
$$
\bold{J} = - n e \langle v \rangle = ( \frac{n e^2 \tau}{m})E \equiv \sigma E
\\
\sigma = \frac{1}{\rho} = \frac{ne^2 \tau}{m}
$$

- 금속의 전자 농도는 대략 $10^{22}$ [electrons/$cm^3$]
- 전자 1개가 차지하는 볼륨을 '구'로서 표현하면 반지름을 $a_0 \approx 0.53 [ \dot{A} ]$. 이를 Bohr radius라 한다.

#### Collision time

collision time을 정의할 수 있어야 conductivtiy를 나타낼 수 있다.
$$
\begin{align}
&\sigma = \frac{1}{\rho} = \frac{ne^2 \tau}{m}
\\
&\tau = \frac{m}{\rho n e^2}
\end{align}
$$
mean free path를 통해 최대한 collision time을 이해해보자.
$$
\begin{align}
& l = v_o \tau
\\
& V_0 \text{를 Average electronic speed. From classical thermodyanmics로 나타낼 수 있다.}
\\
& \frac{1}{2}m v_o ^2 = \frac{3}{2}k_B T  
\\
\\
& v \approx 10^5[m/s]
\\
& l = 1 \sim 10 [ \dot{A}]
\end{align}
$$
**Collision time : 충돌하는데 걸리는 시간**

Drude model의 한계 :

- 실제로 v는 온도에서 따라서 크게 안바뀜 (temperature independent)
- $\tau$​ (collision time)은 온도에 따라서 크게 바뀜(temperature dependent)

---

#### Electron momentum 방정식

책을 읽으면서 느낀 중요한 Concept

: 전자 각 각의 운동량을 아는 것은 미친 짓이다. ''전자들의 묶음'' Macroscopic 관점에서 생각을 해보자.

momentum을 나타내기 위해 전자들의 운동량, 평균적인 속도를 이용해 나타내보자.

가정 - 전자가 이온과 충돌하면 운동량을 잃는다.

가정- [t, t+dt]동안, 충돌할 확률은 $\frac{dt}{\tau}$ , 충돌하지 않을 확률은 $1-\frac{dt}{\tau}$​

가정 - 외부 힘은 E(t)로, F(t)를 가하고 있음.

<img src="/images/1. Drude Model/image-20240319212902812.png" alt="image-20240319212902812" style="zoom:67%;" />

''전자가 이온과 충돌하면 운동량을 잃는다.' 라는 가정을 잘 생각해보면 전자는 평균시간 $\tau$ 에서 운동량을 잃게 된다.

그러나, 정말 운동량을 잃나?라고 생각하면 많이 의문이 든다. 

따라서 전자의 운동량을 잃는다. 라고 생각할 때, "Average the final momentum" 이 0이다라고 생각하는 게 좋다.

이를 통해 다음의 식을 생각할 수 있다.
$$
p(t) : \text{운동량}, F(t) : \text{전기장, 자기장에 의한 외부힘}
\\
\langle p(t+dt) \rangle = (1 - \frac{dt}{\tau})( \langle p(t) \rangle  + F dt ) +  \frac{dt}{\tau} ~0
$$
다음의 식을 통해 전개해보자.
$$
\begin{align}
&\langle p(t+dt) \rangle = (1 - \frac{dt}{\tau})( \langle p(t) \rangle  + F dt ) +  \frac{dt}{\tau} ~0
\\
&\langle p(t+dt) \rangle = \langle p(t) \rangle  - \frac{dt}{\tau} \langle p(t) \rangle + F dt - \frac{dt}{\tau}F dt-  \frac{dt}{\tau} ~0
\\
&\langle p(t+dt) \rangle - \langle p(t) \rangle  = - \frac{dt}{\tau} \langle p(t) \rangle + F dt - \frac{dt}{\tau}F dt
\\
&\frac{\langle p(t+dt) \rangle - \langle p(t) \rangle}{dt}  = - \frac{\langle p(t) \rangle}{\tau}  + F - \frac{F dt}{\tau}
\\
&\lim_{dt \rightarrow 0}\frac{\langle p(t+dt) \rangle - \langle p(t) \rangle}{dt}  = \lim_{dt \rightarrow 0}(- \frac{\langle p(t) \rangle}{\tau}  + F - \frac{F dt}{\tau})
\\
&\frac{d\langle p(t) \rangle}{dt} = - \frac{\langle p(t) \rangle}{\tau}  + F
\\
\\
&\langle p(t) \rangle\text{을 } p(t)\text{물리적으로는 같다는 것을 의미한다고 가정하자.}
\\
&\text{particle 1개에 대한 분석을 할 수 없으므로.}
\\
&\frac{p(t)}{dt} = - \frac{p(t)}{\tau}  + F
\\
\\
&\text{Electric field가 없을 때는 다음과 같다.}
\\
&p(t) = p_{\text{initial}} e^{-t/\tau}
\\
\\
&\text{해석할 때 모든 것을 '평균적인'의 의미를 반드시 부여하자.}
\end{align}
$$


1) 만약 $p(t)$를 $m \dot x$로 생각한다면 이를 harmonic oscillator의 관점으로 생각할 수 있다.

따라서, $-\frac{p(t)}{\tau}$는 Damping term임을 알 수 있다.
