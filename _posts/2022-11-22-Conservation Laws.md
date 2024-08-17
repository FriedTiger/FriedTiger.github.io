---
layout: single
title: "8-1)Conservation Laws"
typora-root-url: ../
categories : "Electromagnetic"
tag : electrodynamics
#tag : [me, me2, me3]
toc : true
toc_sticky : true
author_profile : false
---
## Electromagnetic 

이번 챕터에서는 에너지, 운동량, 각운동량 법칙에 대해서 배운다.

1. #### Conservation of Charge

$$
\frac{\partial \rho}{\partial t} = - \triangledown \cdot J : \text{Continuity equation}
$$

전하량 보존 법칙은 Continuity equation으로 나타낼 수 있고, 이는 맥스웰 방정식과 독립적이다.



2. #### Conservation of Energy

아래와 같은 상황을 상상해보자.

<img src="/images/8. Conservation Laws/image-20240628113121895.png" alt="image-20240628113121895" style="zoom:67%;" />

전자기파가 사각형으로 들어오는 상황을 생각해보자.

dt만큼 시간이 지나면, 전하들이 살짝 움직일 것이다. 전기장과 자기장을 만들 것이다.

이럴 때, $d\tau$가 받는 Electromagnetic forces는 어떻게 될까?

이를 Lorentz force law로 부터 구할 수 있다. 비보존력이 아닌 그냥 알짜힘이라고 생각하자.
$$
\begin{align}
&\text{일과 운동에너지 정리}
\\
\\
&d\tau \text{에 해당하는 전하에 대해 다음을 알 수 있다.}
\\
&F \cdot dl = q(\vec{E}+ \vec{v} \times \vec{B})\cdot \vec{v} dt = q\vec{E} \cdot \vec{v}~dt
\\
&q \rightarrow \rho ~d\tau, ~~ \rho ~\vec{v} \rightarrow \vec{J}
\\
\\
&\text{이를 정리하면 일(알짜힘)과 운동에너지 식으로 나타낼 수 있다.}
\\
&\int_{\text{Volume}}(\vec{E}\cdot \vec{J})d\tau = \frac{dW}{dt}
\end{align}
$$

---

#### Poynting Vector

위에서 나타낸 일(알짜힘)과 운동에너지 식을 $d\tau$에 해당하는 입자의 성격이 아닌 Field 관점에서 생각해보자.

에너지 보존 관점에서 이를 생각해야 한다. (들어간 에너지) = (운동 에너지) + (위치 에너지)
$$
\begin{align}
&\vec{E} \cdot \vec{J} &&= \frac{1}{\mu _o}\vec{E} \cdot (\triangledown \times \vec{B}) - \epsilon _0 \vec{E} \cdot \frac{\partial \vec{E}}{\partial t} ~~~~~~~~~\because \triangledown \times \vec{B} = \vec{J} + \epsilon _0 \frac{\partial \vec{E}}{\partial t} 
\\
& ~ &&= \frac{1}{\mu _0}[\vec{B}\cdot ( \triangledown \times \vec{E})-\triangledown \cdot (\vec{E}\times \vec{B})] - \epsilon _0 \vec{E} \cdot \frac{\partial \vec{E}}{\partial t} ~~~~~~~~~\because \text{product rule 6}
\\
& ~ &&= \frac{1}{\mu _0}[\vec{B}\cdot -\frac{\partial \vec{B}}{\partial t}-\triangledown \cdot (\vec{E}\times \vec{B})] - \epsilon _0 \vec{E} \cdot \frac{\partial \vec{E}}{\partial t} ~~~~~~~~~\because \text{Faraday's law}
\\
& ~ &&= -\frac{1}{2}\frac{\partial}{\partial t}(\epsilon _0 E^2 + \frac{1}{\mu_0}E^2) - \frac{1}{\mu _0}\triangledown \cdot (\vec{E} \times \vec{B}) ~~~~~~~~~\because \text{이차미분 성질}
\\
\end{align}
$$

또한 다음 아래의 내용을 안다.
$$
\begin{align}
&W_e = \frac{\epsilon _0}{2}\int E^2 d\tau : \text{Electric energy}
\\
&W_m \frac{1}{2 \mu _ 0} \int B^2 d\tau : \text{Magnetic energy}
\\
&u = \frac{1}{2}(\epsilon_0 E^2 + \frac{1}{\mu _0}B^2) : \text{Energy density}
\end{align}
$$
이를 통해서 일과 운동에너지 식에 관해 다음처럼 생각할 수 있다.
$$
\begin{align}
& &&\text{에너지 보존 법칙에 대해}
\\
&\frac{dW}{dt} &&= - \frac{d}{dt} \int_{\text{Volume}} \frac{1}{2}(\epsilon _0 E^2 + \frac{1}{\mu _0}B^2) - \oint_{\text{surface}} \frac{1}{\mu _0}\triangledown \cdot ( \vec{E} \times \vec{B}) \cdot d\vec{a}~~~~~~~~~ : \text{Poynting Theorem(Work-energy theorem of 전자기학)}
\\
& &&= -\frac{d}{dt}\int _{\text{Volume}}u ~d\tau - \oint_{\text{surface}} \frac{1}{\mu _0}\triangledown \cdot ( \vec{E} \times \vec{B}) \cdot d\vec{a}
\\
\\
&\text{들어간 에너지} &&= \text{운동 에너지} + \text{위치에너지}
\\
&- \oint_{\text{surface}} \frac{1}{\mu _0}\triangledown \cdot ( \vec{E} \times \vec{B}) \cdot d\vec{a} &&=\frac{dW}{dt}+\frac{d}{dt}\int _{\text{Volume}}u ~d\tau
\\\\
&\text{Poynting Vector는 다음으로 기술된다.}
\\
&S \equiv \frac{1}{\mu_0}(\vec{E}\times \vec{B})
\\
\\
&\therefore -\oint \vec{S} \cdot d \vec{a} &&=\frac{dW}{dt}+\frac{d}{dt}\int _{\text{Volume}}u ~d\tau 
\\
&\text{이를 정리하면 일반적인 식으로 나타낼 수 있다.}
\\
&-\triangledown \cdot \vec{S} = \frac{\partial w}{\partial t} + \frac{\partial u}{\partial t}
\end{align}
$$
전자기파의 에너지는 전하에 대해 앞 뒤로 막 여러방면으로 복합적으로 영향을 미친다. 전자기파의 에너지는 보존력이어서 역학적 에너지 손실은 없는 듯.

이를 최종적으로 생각할 때, 전자기파 에너지를 넣어준 만큼 운동에너지 + 위치에너지로 작용을 하고. 운동에너지는 Work의 시간 변화, 위치에너지는 Energy density의 시간변화를 통해 나타낼 수 있다.