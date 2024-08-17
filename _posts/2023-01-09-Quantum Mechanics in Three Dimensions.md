---
layout: single
title: "4)Quantum Mechanics in Three Dimensions"
typora-root-url: ../
categories : "Quantum-Mechanics"
tag : Quantum
#tag : [me, me2, me3]
toc : true
toc_sticky : true
author_profile : false
---
## Quantum Mechanics 

#### 슈레딩거 방정식

슈레딩거 방정식은 다음과 같다.
$$
\\i\hbar \frac{\delta \Psi }{\delta t } = \hat{H}\Psi
$$

Hamilton operator를 고전역학에서의 운동에너지 + 위치에너지로 나타내어 대입하면 다음과 같다.
$$
i\hbar \frac{\delta \Psi}{\delta t} = -\frac{\hbar^2}{2m}\triangledown ^2 \Psi +V\Psi
$$
이를 time-independent Schrodinger Equation으로 표현하면 다음과 같다.
$$
-\frac{\hbar ^2}{2m}\triangledown^2\psi +V\psi = E\psi
$$
이를 time-dependent Schrodinger Equation으로 표현하면 다음과 같다.
$$
\Psi(\bold{r},t) = \sum c_n \psi_n(\bold{r})e^{-iE_nt/\hbar}
$$

---

#### Spherical Coorindates

대부분의 상황은 **Central Potentials** 이므로 구형좌표계로 생각하는 것이 자연스럽다.

변수분리를 통하면 다음과 같다.
$$
\psi(r, \theta, \phi) = R(r)Y(\theta, \phi)
$$
이를 time-dependent Schrodinger Equation에 대입하면 다음과 같다.
$$
\underline{\left\{\frac{1}{R}\frac{d}{dr}\left(r^2\frac{dR}{dr}\right) - \frac{2mr^2}{\hbar^2}\left[V(r) - E\right]\right\}} + \underline{\frac{1}{Y}\left\{\frac{1}{\sin\theta}\frac{\partial}{\partial \theta}\left(\sin \theta \frac{\partial Y}{\partial \theta}\right) + \frac{1}{\sin^2 \theta}\frac{\partial^2 Y}{\partial \phi^2}\right\}} = 0
$$
밑줄 친 부분은 서로 상수여야만 변수 관점에서 말이 된다. 

따라서, 다음과 같이 표기할 수 있다.
$$
\frac{1}{R}\frac{d}{dr}(r^2 \frac{dR}{dr}) -\frac{2mr^2}{\hbar^2}[V(r)-E]=l(l+1)
\\
\frac{1}{Y} \{\frac{1}{sin\theta}\frac{\delta}{\delta \theta}(\sin \theta \frac{\delta Y}{\delta \theta})+\frac{1}{sin^2 \theta}\frac{\delta ^2 Y}{\delta \phi ^2} = -l(l+1)
$$

---

#### The Angular Equation

아래 식에서 Y는 V(r)과 관계가 없으므로 **어떠한 상황과 관계없이 항상 성립하는 식**이다.

이를 풀기위해 변수분리를 통하면 다음과 같다.
$$
Y(\theta, \phi) = \Theta(\theta)\Phi(\phi)
$$
이를 대입하면 다음과 같다.
$$
\underline{\{ \frac{1}{\Theta}[sin\theta \frac{d}{d\theta}(sin \theta \frac{d\Theta}{d\theta})]+l(l+1)sin^2 \theta\}}+\underline{\frac{1}{\Phi}\frac{d^2 \Phi}{d \phi ^2}} = 0
$$
따라서, 다음과 같이 표기할 수 있다.
$$
\{ \frac{1}{\Theta}[sin\theta \frac{d}{d\theta}(sin \theta \frac{d\Theta}{d\theta})]+l(l+1)sin^2 \theta\} = m^2
\\
\frac{1}{\Phi}\frac{d^2 \Phi}{d \phi ^2} = -m^2
$$
이를 최종적으로 정리하면 다음과 같다.
$$
\Phi(\phi) = e^{im\phi}
\\
\Phi(\phi + 2\pi) = \Phi(\phi) 
\text{이므로, ~~~따라서~ m은 정수다 }
$$

$$
\Theta(\theta) = A P^m_l (cos\theta) \text{로 나누어 나타낼 수 있다 : associated Legendre function}
\\
P^m_l \text{는 2개의 이름표를 갖고 있는 것을 알 수 있다.}
$$



다음 상황에서 Nomarlize를 찾을 수 있다.
$$
\int{\mid \psi \mid}^2 r^2 sin\theta ~dr~ d\theta~ d\phi = \underline{\int\mid R \mid ^2 r^2~dr}~~\underline{\int\mid Y \mid ^2 d \ohm}=1
\\
\ohm \text{은 Solid angle}
$$
이를 모두 정리하면 다음과 같다.
$$
Y^m_l(\theta, \phi) = \sqrt{\frac{(2l+1)}{4 \pi}\frac{(l-m)!}{(l+m)!}}e^{im\phi} P^m_l(cos\theta)
$$

---

#### The Radial Equation