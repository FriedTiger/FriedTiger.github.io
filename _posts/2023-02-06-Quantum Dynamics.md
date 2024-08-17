---
layout: single
title: "11)Quantum Dynamics"
typora-root-url: ../
categories : "Quantum-Mechanics"
tag : Quantum
#tag : [me, me2, me3]
toc : true
toc_sticky : true
author_profile : false
---
## Quantum Mechanics 

time- independent purturbation theory는 다음과 같다.
$$
\Psi (\bold{r}, t) = \psi (\bold{r}) e^{\frac{- i E t}{\hbar}}
$$
**Transitions (quantum jumps)** 를 고려하고 싶다면 Quantum Dynamics(Time - Dependent Purturbation Theroy)를 알아야 한다.
$$
\text{example)} 
\\
\text{빛의 흡수가 없을 때 : } \hat{H} = H_0
\\
\text{빛의 흡수가 있을 때 : } \hat{H} = H_0 + H^{'}
$$

---

#### Two-Level Systems

$$
\hat {H^0} \psi_a = E_a \psi_a ~~ and ~~ \hat {H^0} \psi_b = E_b \psi_b, ~~~ \langle \psi_a \vert \psi_b \rangle = 0
\\
\text{따라서 Two-Level Systems에서 두 } \psi \text{에 대한 선형 조합으로 나타낼 수 있다.}
\\
\\
\psi(0) = c_a \psi_a + c_b \psi_b
\\

\psi(t) = c_a(t) \psi_a e^{-i \hbar t / \hbar} + c_b(t) \psi_b e^{- i \hbar t / \hbar}, ~~~~ \vert c_a \vert ^2 + \vert c_b \vert ^2 = 1
$$

#### The Perturbed System

$$
H = H_0 + H^{'}(t) = H_0 + \lambda W(t)
\\
\\

\vert \phi \rangle : \text{perturbed state라 정의하자}
\\
\vert \phi \rangle = \sum _n c_n(t) \vert n \rangle e^{-i {E_n t}/{\hbar}}
\\
i \hbar \frac{\delta \vert \phi \rangle}{\delta t} = \left\{H_0 + H^{'}\right\} \vert \phi \rangle
$$

이를 대입하고 미분 및정리하면 다음과 같다.
$$
\sum _n \frac{dc_n}{dt} \vert n \rangle e^{-iE_nt/ \hbar}= \frac{1}{i \hbar}\sum_n c_n(t) \lambda W(t)\vert n \rangle e^{-iE_nt/ \hbar}
\\
\\
\text{위 식에 } \langle m \vert \text{를 곱하고 정리하면 다음과 같다.}
\\
\frac{dc_m}{dt} = \frac{1}{i \hbar} \sum_n \lambda c_n(t)\langle m \vert W \vert n \rangle e^{i(E_m - E_n)t/ \hbar}
\\ \langle m \vert W \vert n \rangle \equiv W_{mn}, \text{~and} ~~E_m - E_n \equiv \hbar w_{mn}\text{라 하자} \\
\frac{dc_m}{dt} = \frac{1}{i \hbar} \sum \lambda c_n (t) W_{mn}e^{iw_{mn}t}
$$
이 때 power series를 통해 정의를 하자.
$$
c_m(t) = c^0 _m (t) + \lambda c^1 _m (t) + \lambda ^2 c^2 _m (t) + \cdot\cdot\cdot
$$
이를 대입하고 정리하면 다음과 같다.
$$
\frac{dC^0_m}{dt} + \lambda \frac{dC^1_m}{dt} + \lambda ^2 \frac{dC^2_m}{dt} + \cdot\cdot\cdot
\\
= \frac{1}{i \hbar} \sum_n \lambda(c^0_n + \lambda c^1_n+ \lambda^2 c^2_n+ \lambda^3 c^3_n+ \cdot\cdot\cdot)W_{mn}e^{iw_{mn}t}
$$

$$
0th ~ order : \frac{dC^0 _m}{dt} = 0
\\
1st ~ order : \frac{dC^1_m}{dt} = \frac{1}{i \hbar} \sum _n W_{mn} c^0_ne^{iw_{mn} t}
$$

시간에 대한 식이므로 Initial Conditon i은 다음과 같다.
$$
c_m (0) = \delta _ {mi} =c_m^0 (0) +\lambda c_m^1 (0)+\lambda c_m^2 (0)+\lambda c_m^3 (0) + \cdot\cdot\cdot
\\
\text{ 시간 0에서~} \lambda = 0 이므로 ~c^0_m (0) = \delta_{mi},~ c^N_m (0) = 0 ~ for N\neq 0
$$
이를 통해 정리하면 다음과 같다.
$$
1st ~order : c^1_m(t) = \frac{1}{i \hbar} \int^t _0 dt' W_{mi}(t')e^{iw_{mi} t'}
$$

---

#### Transition Probability

$$
P_{i \rightarrow n} = \vert c_n (t) \vert ^2
\\
c_n(t) = c^0_n(t) + \lambda c^1_n(t) + \lambda c^2_n(t)+ \cdot\cdot\cdot
\\
\\
\text{If} ~ n \neq i , c^0 _n (t) = 0
\\
P_{i \rightarrow n} = \vert \lambda c^1_n (t)\vert^2
\\
=\vert \frac{\lambda}{i \hbar} \int ^t _0 dt' W_{ni}(t')e^{iw_{ni}t'}\vert^2
\\
=\frac{1}{\hbar ^2}\vert \int^t _0 dt' H^{'}_{ni}(t')e^{iw_{ni}t'}\vert^2
$$

따라서 확률을 구하는 방법은 다음과 같다.

1. $H^{'}_{ni} = \langle n \vert \hat{H} \vert i \rangle$을 계산한다.
2. $E_m - E_i = \hbar w_{mi}$를 계산한다. 
3. 이를 적분한다.


$$
\frac{dc_m}{dt} = \frac{1}{i \hbar} \sum \lambda c_n (t) W_{mn}e^{iw_{mn}t}
$$
(12)와 (11)을 연결하여 생각하면, perturbation이 크지 않은 상황에서 성립한다. 즉, t가 크지 않을 떄 성립한다.

---

#### Electromagnetic Waves

전자기파와 같은 싸인파를 perturbation으로 생각하면 전자기파의 주기에 맞게 작동한다.

책과 보충자료를 통해 정리하면 다음과 같다.

#### Absorption & Stimulated Emission

$$
\text{ lower state : } \psi_a, ~~~ \text{upper state : }\psi_b
\\
P_{a \rightarrow b}(t) = \left(\frac{\vert \wp \vert E_0}{\hbar}\right)^2 \frac{sin^2 \left[(w_0 - w)t/2\right]}{(w_0 - w)^2}\\
P_{b \rightarrow a}(t) = \left(\frac{\vert \wp \vert E_0}{\hbar}\right)^2 \frac{sin^2 \left[(w_0 - w)t/2\right]}{(w_0 - w)^2}
$$

Quantum dot도 레이저 같은 원리일까 OLED와 같은 원리일까?

디스플레이 소자는 OLED와 같은 Spontaneous Emission이다.



#### Spontaneous Emission

진공 filed가 stimulated Emission을 통해 Spontaneous Emission를 나타낸다.

---

#### Incoherent Perturbations

12/01 강의 및 Valeur, Molecular Fluorescence : Principles and Applications 책 읽어보자.



#### Fermi Golden Rule

