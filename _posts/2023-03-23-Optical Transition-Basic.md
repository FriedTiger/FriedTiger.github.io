---
layout: single
title: "4)Optical transition - Basic"
typora-root-url: ../
categories : "OLED"
tag : exciton
#tag : [me, me2, me3]
toc : true
toc_sticky : true
author_profile : false
---
## OLED

Optical Transition이란 transition between two molecular states involving EM wave

Optical Transition은 Light-matter interaction이며 transient한 개념이다.

- H-field는 spin과 같은 electron's magnetic moment에 영향을 준다. 
- E-field는 electric charge(electron&nuclei)에 영향을 주고 이는 optical transition을 일으킨다.
- Optical Transition의 결과는 분자내의 electron configuration의 redistribution 및 molecule의 dipole moment 변화를 일으킨다.

---

#### Electric Dipole

$\mu$ (dipole moment of a molecule) = q $\cdot$ $\bold{r}$ 
$$
\tau = \mu \times E
$$
<img src="/images/figure/image-20230406123025465.png" alt="image-20230406123025465" />


Electric Potential Energy를 계산하기 위해 $\theta = \frac{\pi}{2}$ 일 때를  $U = 0$ 로 계산하자.
$$
U = \int ^{\theta } _{\frac{\pi}{2}} \tau d \theta^{'} = \mu E \int ^{\theta } _{\frac{\pi}{2}}sin\theta ^{'}d \theta{'} = - \mu Ecos\theta = - \mu \cdot E
\\
\text{ U = Light(E) - matter(}{\mu}\text{) interaction energy로 여기 단원에서는 표기한다.}
$$

---

#### Permanent dipole moment

Molecule이 
$$
\langle U \rangle = \langle \Psi_n \vert \hat{U} \vert \Psi_n\rangle = \int \Psi^*_n (\hat U)\Psi_n d^3 \bold{r} = \int \Psi^*_n(-\hat{\mu}\cdot \hat{E}) \Psi^*_n d^3 \bold{r}
\\
\text{molecule의 길이는 ~1nm 정도 되니 전기장이 이 구간에서 일정하다고 가정하자.}
\\
\therefore \langle U \rangle \approx - E \cdot \langle \mu \rangle ~~~ (\ast ~  \langle \mu \rangle = q \langle r \rangle)
$$

#### Transition dipole moment

transition dipole moment : dipole moment of the molecule ' during transition' --> transient의 의미를 갖는다.
$$
\langle U \rangle = \langle \Psi_f \vert \hat{U} \vert \Psi_i \rangle = \int \Psi^* _f (\hat{U})\Psi_i d^3\bold{r} = \int \Psi^*_f ( - \hat{\mu} \cdot \hat{E}) \Psi^*_i d^3 r \approx -E \cdot \langle \mu \rangle _T
\\
\text{Probability of a transition} = \langle \mu \rangle ^*_T \langle \mu \rangle _T = \vert \langle \mu \rangle _T \vert ^2
\\
\vert \langle \mu \rangle _T \vert ^2 = 0 : \text{No transition}
\\
\vert \langle \mu \rangle _T \vert ^2 \gg 0 : \text{Strong transition}
$$
만약, 1차원에서 transition dipole moment 문제를 푼다음 다음처럼 풀 수 있다.
$$
\langle \mu \rangle _T = q \int \Psi ^*_n (\hat{x}) \Psi _m dx = \int x ( \psi^*_n exp (i\frac{E_n}{\hbar}t))(\psi_m exp(-i \frac{E_m}{\hbar}t))dx
\\
= \underline{(\int x \psi^*_m \psi_n dx)} \cdot  \underline {exp(-i \frac{E_m-E_n}{\hbar}t)}
\\
= \text{ Exchange integral  } \times \text{Oscillating term}
$$
Exchange integral : Intensity $\propto \int x \psi ^*_m \psi_n dx$ (spatial overlap) 을 의미한다.

Oscillating term : $E_m 과 E_n$ 전자가 왔다갔다 하다가, $\frac{E_m - E_n}{\hbar}$ 의 진동수를 갖는 빛을 방출한다.

---

#### Molecular Wavefunction to Born-oppenhiem approximation

$$
\Psi = \cdot \psi _{electron} \psi_{nuclei} \Phi_{spin}
\\
\text { Fermi's golden rule : a formula for transition rate at two states} 
\\
k_{if} = \alpha \vert \langle \mu \rangle _T \vert ^2 = \alpha \cdot \langle \psi_f \vert \hat{x} \vert \psi_i \rangle \times \vert \langle \psi_{nf} \vert \psi_{ni} \rangle \vert \times \vert \langle \phi_f \vert \phi_i \rangle \vert  : \text{Born-oppenhiem approximation}
$$

#### 1. Electronic state

- Electron configuration & total spin angular momentum 에 의해 결정된다  

- $$
  \langle \psi_{ef}\vert \hat{r}\vert \psi_{ei}\rangle
  $$



#### 2. Vibrational state : Frank-Condon Principle

- vibrational motion of constituting atoms. (energy interval : 0.1 ~ 0.3 eV) 
  $$
  \langle \psi_{nf} \vert \psi_{ni}\rangle
  $$
  $\psi_{ni}$ 와 $\psi_{nf}$ 사이의 nuclei oscillate configuration resonance가 있어야 값이 크다.  

|              | Harmonic Oscillator                              | Morse approximation                                          |
| ------------ | ------------------------------------------------ | ------------------------------------------------------------ |
| Potential    | $V = -D_e + \underline{\frac{1}{2} k (r-r_e)^2}$ | $V = -D_e + \underline{D_e ( 1- e^{-a(r-r_e)})^2} \\ = D_e (\underline{e^{-2a{(r-r_e)}}} - \underline{2e^{-a(r-r_e)})}$ |
| Eigen-energy | $E_n = h v_0 (n+\frac{1}{2})$                    | $E_n = h v_0 (n+\frac{1}{2}) - \frac{1}{4D_e}[hv_0 (n+\frac{1}{2})]^2$ |

harmonic oscillator는 equilibrium state에 대해 좌우 대칭이었지만. morse approximation 에서는 좌우 damping force가 다르므로 ( nuclei가 가까워질수록 nonlinear 하게 반발력이 커짐) short-range repulsion과 long-range attratction차이의 항으로 나타낼 수 있음.

<img src="/images/figure/image-20230408173302253.png" alt="image-20230408173302253" style="zoom:80%;" />

#### 3. Total spin

total spin은 단어와 맞지 않게 $\vert \uparrow \rangle$ 와 $\vert \downarrow \rangle $ 의 spin state들이 cancel되므로, two electrons만 고려해도 된다.
$$
\vert \langle \phi_f \vert \phi _i \rangle \vert 
$$
$\vert \phi_f \rangle$ 과 $\vert \phi_i \rangle$ 이 orthogonal 하면 0 이다.

즉, triplet  - triplet 이라면 1 , singlet - singlet 이라면 1, singlet - triplet 이라면 0 이다.

---

#### Stokes Shift 

Absorption peak와 Emission peak의 값이 차이가 있는 상황이고, molecular 끼리 약한 결합 or 배열 상태일 때 차이가 크다. 

관측 방법 : 아주 낮은 온도 (10k) 에서 관측 가능하다. 

<img src="/images/figure/image-20230408173633825.png" alt="image-20230408173633825" />

born-oppenheim approximation에 따라 $S_0 $ --> $S_1$ 로 이동할 때 transient 순간에는 nuclei distance가 같은 곳에서 electron configuration이 overlap 되고 spin이 orthogonal 하지 않을 때 전이 확률 이 높다.

---

#### Kasha's rule

Emission alway occurs at lowest level of exicted state.

<img src="/images/figure/image-20230511175316935.png" alt="image-20230511175316935" style="zoom:80%;" />

빛을 흡수하여 $S_2 (v_m)$ 에 전자가 exicted state를 형성하면 어떻게 전자의 에너지 준위가 바뀔까. 

Kasha's rule에 의해 설명 가능하다.

1. exicted state의 가장 낮은 곳에서만 방출될 수 있다. 따라서 direct emission : $S_n (v_m) \rightarrow S_0 (v_l)$보다  Internal conversion 확률이 높아진다. 
2. 따라서, $S_n(v_m) \rightarrow S_1(v_0)$ 으로 전이가 된다.
3. $S_1(v_0) \rightarrow S_0(v_l)$ 로 전이되면서 빛을 radiative 하게 된다.

** Anti - Kasha'srule : IC(Internal conversion)이 일어날정도로 vibrational energy가 크지 않으면 $S_2(v_0) \rightarrow S_0(v_l)$ 가 일어날 수 있다. **

<img src="/images/figure/image-20230511185049639.png" alt="image-20230511185049639" style="zoom:80%;" />

---

#### Jablonski Diagram

위에서 종합한 것들을 그린 것을 Jablonski Diagram이라 한다.

<img src="/images/figure/image-20230516125300133.png" alt="image-20230516125300133" />

**Singlet과 Triplet은 다름 System으로 나누어서 그리고, System 사이를 넘어가는 것을 ISC(Intersystem Crossing)이라 한다.** 

<img src="/images/figure/image-20230516125755846.png" alt="image-20230516125755846" />

대략적인 residual time은 위 그림과 같다.
