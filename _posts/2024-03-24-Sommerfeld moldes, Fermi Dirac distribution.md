---
layout: single
title: "4)Sommerfeld Models-Fermi Dirac Distribution"
typora-root-url: ../
categories : "Solid State Physics"
tag : sommerfeld
#tag : [me, me2, me3]
toc : true
toc_sticky : true
author_profile : false
---
## Solid State Physics

Bosons은 Bose-Einstein distribution

Fermions는 Fermi-Dirac distribution을 갖는다.



앞서 배운 electron gas의 model을 통해 Fermi Dirac distribution을 증명해보자.

---

#### Fermi Dirac distribution 증명

가정 : 

- spin은 고려하지 않는다.
- 전자 1개는 1개의 state를 차지한다.

전제 : 

볼츠만 분포(Boltzmann distribution)에 따라 system이 Energy $E_i$ 에 대해 state $i$ 가 차지할 확률은 다음과 같다.
$$
\begin{align}
&p_N (E_i) \propto e^{-\frac{E_i}{k_B T}}
\\
&p_N (E_i) = \frac{1}{Q}e^{-\frac{E_i}{k_B T}}, ~~ \text{where}~~ Q = \sum_i e^{- \frac{E_i}{k_B T}}
\\
&\text{Q는 가능한 상태들의 확률의 총합을 의미한다. 즉, Q는 1을 나타내는게 아님.}
\end{align}
$$
열역학 개념 (Helmholtz free energy)의 개념으로 Q를 다음과 같이 나타낼 수 있다.

$F_N = U - TS$ (Helmholtz free energy) : 온도 T에서 생성할 수 있는 에너지 총 양
$$
\begin{align}
&Q = \sum_{i=1} e^{-\frac{E_i}{k_B T}} = e^{-\frac{F_N}{k_B T}}, ~~ F_N = U-TS 
\\
&\text{따라서,} ~p_N\text{을 위 식에 따라 나타내면 다음과 같다.}
\\
&p_N(E_i) = e^{-\frac{E_i - F_N}{k_B T}}
\end{align}
$$
정의 : 

<img src="/images/4. Sommerfeld moldes-Fermi Dirac distribution/image-20240403120533990.png" alt="image-20240403120533990" style="zoom:67%;" />

N개의 전자에 대해 $i$th state에 전자가 있을 확률은 다음과 같다.
$$
f_{i,N} = \sum_{\alpha} p_N(E_{\alpha, N}) ~~ \text{i번째 전자가 존재하여 있는  상태로 } \alpha\text{가 1부터 N까지 각 state에 차있는 확률의 합}
$$
N개의 전자에 대해 $i$th state에 전자가 있을 확률은 다음처럼도 표현 가능하다.
$$
f_{i,N} = 1 - \sum_{\beta} p_N(E_{\beta, N}) ~~ \text{i번째 전자가 존재하여 않는  상태로 1에서 } \beta\text{가 1부터 N까지 각 state에 차있는 확률의 합을 뺀 것}
$$

---

증명 시작 :  

CASE 1 : N+1개의 전자들에서 $i$th state를 전자가 채우고 있는 상황 : 에너지를 다음처럼 표현 가능 ($E_{\alpha, N+1}$ )

CASE 2 : N+1개의 전자들에서 $i$th state를 전자가 채우고 있지 않은 상황 : 에너지를 다음처럼 표현 가능 ($E_{\alpha, N+1} - \epsilon_i$)



N개의 전자들에서 $i$th state를 전자가 채우고 있는 상황을 위 식에 따라 나타내면 다음과 같다.
$$
f_{i, N} = 1 - \sum_{\beta} p_N(E_{\beta, N}) = 1 - \sum_{\alpha}p_N(E_{\alpha,N+1}- \epsilon_i)
$$
정리 : $E_{\alpha, N+1} - \epsilon_i$는  N개의 전자에서 $i$th state를 채우고 있지 않는 것을 의미한다.
$$
\begin{align}
&p_N(E_{\alpha, N+1} - \epsilon _i ) &&= exp(- \frac{(E_{\alpha, N+1} - \epsilon _i) - F_N}{k_B T})
\\
& &&=exp(- \frac{E_{\alpha, N+1}- F_{N+1}}{k_B T}) \cdot exp(- \frac{\epsilon _i- (F_{N+1}-F_N)}{k_B T})
\\
& &&=p_{N+1}(E_{\alpha, N+1}) \cdot exp(\frac{\epsilon_i - \mu}{k_B T}), \text{where}~ F_{N+1} - F_N = \mu  : \text{chemical potential}
\\
\\
& \therefore f_{i,N} &&= 1 - exp(\frac{\epsilon_i - \mu}{k_B T})\sum_{\alpha}p_{N+1}(E_{\alpha,N+1}) = 1-exp(\frac{\epsilon _i - \mu}{k_B T})f_{i,N+1}
\\
\\
& && N >> 10^{22} cm^{-3}\text{에서, extra electron은 무시 가능하다.}
\\
&f_{i,N} = 1 - exp(\frac{\epsilon_i - \mu}{k_B T})f_{i,N+1} &&\rightarrow f_{i,N} \approx 1 - exp(\frac{\epsilon_i - \mu}{k_B T})f_{i,N}
\\
&\therefore f_i = \frac{1}{exp(\frac{\epsilon_i - \mu}{k_B T})+1}
\end{align}
$$
따라서 정리하면 다음과 같다.
$$
\begin{align}
&\text{Fermi-Dirac distribution : N개의 전자가 i번째 level에 전자가 차있을 확률}
\\
&f_i = \frac{1}{exp(\frac{\epsilon_i - \mu}{k_B T})+1}
\end{align}
$$

---

#### Fermi-Dirac statistics - Chemical potential ($\mu$)

$$
f_i = \frac{1}{exp(\frac{\epsilon_i - \mu}{k_B T})+1}
$$

의미 : single-Fermion level($\epsilon_i$)이 차여있을 확률
$$
\begin{align}
&\text{Chemical potential}(\mu) ~\text{정의 내리기}
\\
\\
&\text{온도가 0 인상황을 생각해보자.}
\\
&f_i = 1 ( \epsilon_i \langle \mu) ~\text{or} ~0  ( \epsilon_i \rangle \mu)
\\
&\text{따라서, }\mu \text{기준으로 생각할 수 있다.}
\\
\\
&\text{Fermi Energy : } \epsilon_F = \frac{\hbar ^2 k_F ^2}{2m} : \text{the highest occupied eneregy in T = 0K}
\\
&\therefore \lim_{T \rightarrow 0} \mu(T) = \epsilon _F
\end{align}
$$
이를 그래프로 나타내면 다음과 같다.

<img src="/images/4. Sommerfeld moldes-Fermi Dirac distribution/image-20240409113819479.png" alt="image-20240409113819479" style="zoom:67%;" />

상온에서 Step function이라고 봐도 무방하다. 

**Temperature-dependent Chemical potential**
$$
\begin{align}
& \text{(전자의 수) = (Fermi-Dirac distribution) * (Energy state 수)} 
\\
& n_i = f_i \cdot g_i
\\
&\text{가정: Energy state 수가 상수라고 가정하자.}
\\
& N = \sum_i n_i \simeq \int ^ {\infty} _0 g f(\epsilon) d\epsilon = \int ^{\infty} _0 \frac{g~d\epsilon}{exp[\frac{\epsilon - \mu}{k_B T}]+1}
\\
&\text{이를풀면 다음과 같다.}
\\
&\mu(T) = k_B T ~ln(exp(\frac{N}{g k_B T})-1) 

\end{align}
$$
이를 그래프로 나타내면 다음과 같다.

<img src="/images/4. Sommerfeld moldes-Fermi Dirac distribution/image-20240412150856664.png" alt="image-20240412150856664" style="zoom:67%;" />

온도 $T$가 $T_F$가 될 때까지 0.3$T_F$ 가 될 때 까지 $\mu$는 $\epsilon_F$으로 생각할 수 있다. 

---

#### Fermi-Dirac statistics - total energy of electron gas

지금까지 우리는 양자역학 관점에서의 electron gas model과 Fermi-Dirac statistics를 유도하였다.

따라서, 이를 통해 electron gas의 전체 에너지를 구해보자.
$$
\begin{align}
&\text{전자 1개에 대해 다음의 에너지를 갖는다. :} ~\epsilon(\vec{k})  = \frac{\hbar^2 k ^2}{2m}
\\
&\vec{k}\text{는 Volume에 대한 k wave vector를 의미한다.}
&N  = 2 \sum_k f(\epsilon(\vec{k}))
\\
&U = 2\sum_k \epsilon(\vec{k})f(\epsilon(\vec{k}))
\\
&\text{이를 적분형태로 나타내면 다음과 같다.}
\\
&\frac{N}{V} = n = \int \frac{d\vec{k}}{4\pi ^3}f(\epsilon(k)) = \int^{\infty}_0 \frac{4\pi k^2 dk}{4\pi^3}f(\epsilon(\vec{k}))
\\
&k^2 = \frac{2m\epsilon}{\hbar ^2}, ~ 2kdk = \frac{2m}{\hbar^2}d\epsilon \rightarrow kdk = \frac{m}{\hbar ^2}d\epsilon \text{를 대입하면 다음과 같다.}
\\
&\text{준식} = \int ^{\infty} _ 0 \frac{\sqrt{2}}{\pi ^2} (\frac{m}{\hbar ^2})^{\frac{3}{2}} \sqrt{\epsilon}f(\epsilon )d\epsilon
\\
&\text{준식} = \int ^{\infty} _ 0 g(\epsilon)f(\epsilon)d\epsilon, ~ g(\epsilon) = \frac{\sqrt{2}}{\pi ^2} (\frac{m}{\hbar ^2})^{\frac{3}{2}} \sqrt{\epsilon}
\\
&\text{Density of state는 } \sqrt{\epsilon}\text{에 비례한다.}
\\
\\
&\therefore
\\
&u = \int ^{\infty} _ 0 \epsilon g(\epsilon)f(\epsilon)d\epsilon
\\
&n = \int ^{\infty}_0 g(\epsilon)f(\epsilon)d\epsilon
\end{align}
$$
이를 통해서 Total energy of electron gas를 구하면 다음과 같다.
$$
u =\int ^{\infty} _0 \epsilon g(\epsilon)f(\epsilon) \simeq \frac{3}{5}n \epsilon _F [ 1 + \frac{5\pi^2}{12}(\frac{T}{T_F})^2] =U_0 + \triangle U (\text{Ground state E(T=0K) + Excited state E(T>0K)})
$$
이를 통한 $C_V$를 구하면 다음과 같다.
$$
C_V = \frac{1}{V}(\frac{\partial U}{\partial T})_V = (\frac{\partial u}{\partial T})_V = \frac{\pi ^2}{2}n k_B \frac{T}{T_F} = \frac{3}{2}nk_B (\frac{\pi ^2}{3}\frac{k_B T}{\epsilon _F})
$$
이를 통해 silver의 $C_V$를 구해보면 다음과 같다.
$$
\begin{align}
&C_V = 1.74(J/kg \cdot K)
\\
&C_V \approx 235(J/kg \cdot K) ~\text{measured}
\\
&\text{차이가 발생하는 이유 : Heat capacity는 ion의 관여가 많은 영향을 미친다.}
\end{align}
$$
지금까지 모든 것을 정리하면 다음과 같다.

<img src="/images/4. Sommerfeld moldes-Fermi Dirac distribution/image-20240413173727807.png" alt="image-20240413173727807" style="zoom:80%;" />

1) Mean-free path

<img src="/images/4. Sommerfeld moldes-Fermi Dirac distribution/image-20240413173840450.png" alt="image-20240413173840450" style="zoom:80%;" />

2. Thermal conductivity

<img src="/images/4. Sommerfeld moldes-Fermi Dirac distribution/image-20240413173927870.png" alt="image-20240413173927870" style="zoom:80%;" />

3. Thermopower

<img src="/images/4. Sommerfeld moldes-Fermi Dirac distribution/image-20240413174010769.png" alt="image-20240413174010769" style="zoom:80%;" />

두 모델에 관한 큰 문제 

1) Free-electron approximation : No electron - ion interaction(except collisions)
2) Independent approximation : No electron - electron interaction
3) Relaxation time approximation : $\tau$ independent of electron's position and velocity



이 중에서 1. Free-electron approximation이 가장 큰 문제를 일으킨다.



따라서 이를 다음의 두가지 방향으로 나아가 생각해야한다.

1. **Nearly-free electron model** : Electrons move in the presence of a static potential
2. Consideration of the effects of **ionic vibration**( + Crystalline structure)
