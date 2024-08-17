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

momentum을 나타내기 위해 전자 1개의 운동량, 평균적인 속도를 이용해 나타내보자.

가정 - 전자가 이온과 충돌하면 운동량을 잃는다.

가정- [t, t+dt]동안, 충돌할 확률은 $\frac{dt}{\tau}$ , 충돌하지 않을 확률은 $1-\frac{dt}{\tau}$​

가정 - 외부 힘은 E(t)로, F(t)를 가하고 있음.

<img src="/images/1. Drude Model/image-20240319212902812.png" alt="image-20240319212902812" style="zoom:67%;" />

1) 충돌하지 않았을 시
   $$
   \begin{align}
   &p (t + dt) = \text{기존 운동량 + 외부 힘으로 인한 운동량}
   \\
   &p (t + dt) = p(t) + F(t)dt
   \end{align}
   $$
   

2. 충동하였을 시

$$
p(t+dt) \leq F(t)dt
$$

1과 2를 확률을 고려하여 더하면 다음과 같다.
$$
\begin{align}
&p(t+dt) = (1-\frac{dt}{\tau}) \times 1 + \frac{dt}{\tau} \times 2
\\
&p(t+dt) = (1-\frac{dt}{\tau}) \times (p(t)+F(t)dt) + \frac{dt}{\tau} \times (F(t)dt)
\\
&p(t+dt) = p(t)+F(t)dt - \frac{dt}{\tau}p(t)
\\
&p(t+dt) - p(t) = F(t)dt - \frac{dt}{\tau}p(t)
\\
&\frac{p(t+dt) - p(t)}{dt} = F(t) - \frac{p(t)}{\tau}
\\
&\therefore \frac{dp(t)}{dt} = -\frac{p(t)}{\tau}+F(t)
\end{align}
$$
만약 $p(t)$를 $m \dot x$로 생각한다면 이를 harmonic oscillator의 관점으로 생각할 수 있다.

따라서, $-\frac{p(t)}{\tau}$는 Damping term임을 알 수 있다.
