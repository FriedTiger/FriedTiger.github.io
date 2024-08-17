---
layout: single
title: "3)Sommerfeld Models-Electron Gas"
typora-root-url: ../
categories : "Solid-State-Physics"
tag : sommerfeld
#tag : [me, me2, me3]
toc : true
toc_sticky : true
author_profile : false
---
## Solid State Physics

Specific heat($C_v$), Mean-square electronic velocity($v^2$​), thermopower(Q) 등에서 Drude model이 맞지 않은 모습을 보여줌.

이유 - Drude model은 Maxwell- boltzmann distribution을 따른다고 가정함(표준편차를 갖는.)

실제 - Fermi- Dirac Distribution을 갖음



**Sommerfeld model = Drude's free electron model + Fermi-Dirac Distribution**

---

#### 전자들을 양자역학적으로 표현(electron gas model), 온도가 포함되어있지 않음.

$$
\begin{align}
&-\frac{\hbar ^2}{2m}\triangledown ^2 \psi(\vec{r}) = E \psi (\vec{r})
\\
&\text{Free electron model : no potential term}
\end{align}
$$

 boundary condition

<img src="/images/3. Sommerfeld models/image-20240326132036720.png" alt="image-20240326132036720" style="zoom:67%;" />

계산결과 다음의 wavefunction을 갖는다.
$$
\begin{align}
&\psi_k (r) = \frac{1}{\sqrt{V}}e^{i \vec{k}\cdot \vec{r}}
\\
&E(k) = \frac{\hbar ^2 \vert k \vert ^2}{2m}
\\
&k_x = \frac{2 \pi n_x}{L}, k_y = \frac{2 \pi n_y}{L}, k_z = \frac{2 \pi n_z}{L}
\end{align}
$$
Fermi sphere

<img src="/images/3. Sommerfeld models/image-20240329115938442.png" alt="image-20240329115938442" style="zoom:50%;" />
$$
\begin{align}
&\text{Unit volume in k-space}
\\
&\frac{1}{(2\pi/L)^3} = \frac{L^3}{8 \pi ^3} = \frac{V}{8 \pi ^3}
\\
\\
&\text{Fermi sphere} : k_F
\\
&-\text{N개의 전자들로 채워준 energy level을 의미한다.}
\\
&-\text{Outside the sphere, energy levels are not occupied.}
\\
&\text{이를 계산하면 다음과 같다.}
\\
&n_F = (\frac{4}{3}\pi k_F ^3)\times (\frac{V}{8\pi^3})
\\
&\therefore \frac{N}{V} = \frac{k^3_F}{3 \pi ^2}
\\
\\
&\text{용어 정리 : }
\\
&\text{Fermi velocity : the velocity of the electron in the highest occupied state at the Fermi surface}
\\
&\text{Fermi Energy : the kinetic energy of the electron in the highest occupied state}
\\
&\text{Fermi temperature : }T_F\text{미만 에서는 Fermi-dirac distribution}, T_F\text{이상에서는 Maxwell-Boltzman distribution}
\end{align}
$$


고체 물리수업 학생의 질문 : Voltage를 0이라고 하고 슈레딩거 방정식을 진행하였는데, 그렇다면 전자 particle 1개를 가지고 하는게 아닌 전체 wavefunction을 구해야하는게 아닌가?

교수님 답변 - 그게 현실적으로 맞지만 컴퓨터를 통해서 구해야한다. 실제로 구해보았을 때 크게 차이 없다.

---

#### 이를 통한 결론 vs Drude model

$$
\begin{align}
&\text{In real space}
\\
&\frac{V}{N} = \frac{1}{n} = \frac{4\pi r_s ^3}{3} 
\\
&\text{In Fermi sphere}
\\
&n = \frac{N}{V} = \frac{k_F ^3}{3\pi ^2}
\\
\\
&\text{이를 연립하면 다음의 사실을 알 수 있다.}
\\
&r_s / a_0 = 2 \sim 6 
\end{align}
$$

1) Fermi Velocity

$$
\begin{align}
&\text{- Sommerfeld model}
\\
&v_F = \frac{\hbar k_F}{m} = \frac{4.20}{r_s / a_0} \times 10^6 = \frac{4.20}{4 \sim 6} \times 10^6 (m/s)
\\
\\
&\text{- Drude model}
\\
& v_{th} = \sqrt{\frac{3k_B T}{m}} = 10^{2 \sim 3} (m/s) ~\text{at} ~T= 298K, ~ 0(m/s) ~\text{at} ~T= 0K
\end{align}
$$

2. Fermi Energy(가장 높은 상태의 전자 E)

$$
\begin{align}
&E_F = \frac{\hbar^2 k_F ^2}{2m} = (\frac{e^2}{2a_0})(k_F a_0)^2 = \frac{50.1}{(r_s/a_0)^2} (eV) = 1.5 \sim 15 (eV) \text{for metals} 
\\
\end{align}
$$

3. T = 0K일 때, Ground state Energy

$$
\begin{align}
& \text{- Sommerfeld model}
\\
&E = 2 \sum_{\vert k ~\vert< ~\vert k_F \vert} \frac{\hbar ^2 \vert k \vert ^2}{2m} : \text{within the Fermi sphere}
\\
\\
&\triangle k' = \frac{8 \pi ^3}{V} \text{로 정의하자.} : \text{1 state당 단위 부피}
\\
& v \rightarrow \infty , \triangle k' \rightarrow 0 \text{이라 가정하면 다음과 같이 표현할 수 있다.}
\\
\\
&E = 2 \sum_{\vert k ~\vert< ~\vert k_F \vert} \frac{\hbar ^2 \vert k \vert ^2}{2m} = V \times 2 \times \frac{1}{8\pi ^3} \int_{k < k_F} \frac{\hbar^2 k^2}{2m} dk' = \frac{V}{4 \pi ^3} \int_{k < k_F} \frac{\hbar^2k^2}{2m} ( 4\pi k^2 dk) = \frac{V}{\pi ^2}\frac{\hbar ^2 k_F ^5}{10m}
\\
\\
&\text{이를 Fermi Sphere식과 연립하면 다음을 알 수 있다.}
\\
&\frac{E}{N} = \frac{3\hbar ^2 k_F ^2}{10m} = \frac{3}{5}E_F
\\
\\
&\therefore \text{Ground state energy} = \frac{3}{5}E_F = \frac{3}{5} \times \frac{\hbar ^2 k_F ^2}{2m} = 0.9 \sim 9 (eV)
\\
\\
& \text{- Drude model}
\\
& E_{th} = \frac{3}{2}k_B T = 0 (eV)
\end{align}
$$



