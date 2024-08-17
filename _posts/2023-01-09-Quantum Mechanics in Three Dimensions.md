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
\underline{\{{\frac{1}{R}\frac{d}{dr}(r^2\frac{dR}{dr})-\frac{2mr^2}{\hbar^2}[V(r)-E]}\}}+\underline{\frac{1}{Y}\{{\frac{1}{\sin\theta}\frac{\delta}{\delta \theta}(\sin \theta\frac{\delta Y}{\delta \theta})+\frac{1}{sin^2 \theta}\frac{\delta ^2 Y}{\delta \phi^2}}\}} =0
$$
밑줄 친 부분은 서로 상수여야만 변수 관점에서 말이 된다. 

따라서, 다음과 같이 표기할 수 있다.
$$
\frac{1}{R}\frac{d}{dr}(r^2 \frac{dR}{dr}) -\frac{2mr^2}{\hbar^2}[V(r)-E]=l(l+1)
\\
\frac{1}{Y} \{\frac{1}{sin\theta}\frac{\delta}{\delta \theta}(\sin \theta \frac{\delta Y}{\delta \theta})+\frac{1}{sin^2 \theta}\frac{\delta ^2 Y}{\delta \phi ^2} = -l(l+1)
$$

---