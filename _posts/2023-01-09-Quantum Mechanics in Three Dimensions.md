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