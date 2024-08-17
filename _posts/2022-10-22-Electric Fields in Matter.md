---
layout: single
title: "3)Electric Fields in Matter"
typora-root-url: ../
categories : "Electromagnetic"
tag : field
#tag : [me, me2, me3]
toc : true
toc_sticky : true
author_profile : false
---
## Electromagnetic 

#### **헷갈릴때는 Figure 4.20 그림 및 문제를 살펴보자**

$$
\bold{ \triangledown \cdot E = \frac{\rho _{free} + \rho_{bounded}}{\epsilon _ 0}} \text{로 항상 생각하자.}
$$



#### Polarizability

$$
\begin{align}
p &= \alpha_{\perp}\bold{E} + \alpha_{\parallel}\bold{E}
\\
\alpha &= 4 \pi \epsilon_0 a^3 :\text{일반적으로 부피가 클수록 polarizablity가 크다.}
\end{align}
$$

Induced Dipole $\rightarrow$ 전기장을 상쇄시키는 방향으로 생성. physical dipole로 쉽게 계산할 수 있다.

Polar Dipole $\rightarrow$ 전기장에 대한 토크로 인해 회전하여 정렬된다.

#### Polarization

Dielectric에서 일어나는 Polarization을 알아보려고한다.
$$
p = \alpha E 
; \text{dipole moment는 전기장과 같은 방향}, \alpha : \text{atomic polarizability}
\\
\text{ p 는 physical dipole을 사용해도 된다.} 
\\ 
\text{1. 이유 : 어차피 dielectric 과 상당히 먼 곳에서 궁금한 것이므로}
\\
\text{2. 이유 : dielectric 내부를 구하더라도 macroscopic view를 볼 것이므로}
$$
**Polarized : a lot of little dipoles pointing along the direction of the field**  현상으로 인해 

Polarization($\bold{P}$ )룰  정의내릴 수 있다. 
$$
P \equiv \text{dipole moment per unit volume}
$$

---

#### Bound Charge : $\sigma_b , \rho_b$ 

Single dipole p 에 대해 다음을 알  수 있다. pure dipole로 계산하였다.
$$
V(\bold r) = \frac{1}{4 \pi \epsilon _0}\frac{\bold{p} \cdot \hat{\eta}}{\eta ^2}
$$

위의 식은 physical dipole에 관한 식이다. 원자1개에 대해 microscopic한 관점으로 바라보는 것

우리가 보통 관심있는 것은 원자 1개에 대한 microscopic 관점이므로 physical dipole에 대해 적분을 하여 구해도 괜찮다.

다음 그림의 Dielectric이 있고 pure dipole p가 존재한다고 하자.

<img src="/images/figure/image-20230504155018846.png" alt="image-20230504155018846" style="zoom:67%;" />
$$
V(r) = \frac{1}{4 \pi \epsilon _0} \int _V \frac{\bold{P(r')}\cdot \hat{\eta} }{\eta ^2} d\tau' = \frac{1}{4 \pi \epsilon _0} \int _V \bold{P}\cdot \triangledown' (\frac{1}{\eta}) d\tau'
\\
= \frac{1}{4 \pi \epsilon _0}[\oint \frac{1}{\eta}P \cdot d\bold{a}' - \int \frac{1}{\eta}(\triangledown ' \cdot P)d\tau ']
$$
**First Term** : $\sigma _b \equiv \bold{P} \cdot \hat{n}$ 

**Second Term** : $\rho _b \equiv - \triangledown \cdot \bold{P}$ 

**물리적 의미 1 : $\sigma _b $ 와 $\rho _b$ 는 가상의 charge가 아니라 perfectly genuine accumulations of charge 이다. ** 
$$
\int _V \rho _b d\tau = - \oint_S P \cdot da = - \int _V (\triangledown \cdot \bold{P})d\tau 
\\
\text{물리적 의미 : 내부 축전 전하 + 외부 축전 전하 = 0}
\\
\therefore \rho_b = - \triangledown \cdot P (\text{true for any volume})
$$
 **물리적 의미 2 :problem(3.47d) dielectric 물질 내부의 볼륨 V에 대해, 총 전하량은 0이므로 내부 축전 전하량과 외부 축전 전하량은 같다.**

결론 --> $\bold{P}$로 물질 내부의 Field를 단순 계산하면 된다.

정리 : 

<img src="/images/figure/image-20230504165651654.png" alt="image-20230504165651654" style="zoom:80%;" />
$$
\rho _b - - \triangledown \cdot P = 0 ~~\text{P가 일정하므로}
\\
\sigma_b = P \cdot \hat{n}
\\
\\
\text{즉, P를 통해 계산해주면 된다.}
$$

---

#### Gauss Law in Dielectric

|          | Vaccum                                            | Dielectric                                                   |
| -------- | ------------------------------------------------- | ------------------------------------------------------------ |
| Equation | $\triangledown \cdot E = \frac{\rho}{\epsilon_0}$ | $\triangledown \cdot E = \frac{\rho_f + \rho_b}{\epsilon_0}$ |
| Meaning  | Microscopic & Macroscopic                         | Macroscopic ( $\rho_b$ 가 macroscopic 의미이므로)            |

$$
\triangledown \cdot (\epsilon _0 E) = \rho_f + \rho_b = \rho_f - \triangledown \cdot {P}
\\
\triangledown(\epsilon_0E + {P}) = \rho_f 
\\
\triangledown D = \rho_f ~~~\text { D : Electric Displacement}
$$

**주의 : D에 대해서는 쿨롱의 법칙과 중첩의 원리가 적용되지 않는다. **

#### Electric susceptibility

$$
P = \epsilon _0 \chi_e E
\\
$$

E에 대해 P가 어떻게 생성되는지의 관계를 나타내었다.

**Input** : E $\rightarrow$ **System** : $\chi_e$ $\rightarrow$ **Output** : P 의 형식을 갖는다.
$$
D = \epsilon_0 E + P = \epsilon_0 (1+\chi_e)E = \epsilon_0\epsilon_rE = \epsilon E
$$

Relative permittivity = $\epsilon _r $ = Dielectric constant

Si 반도체 : 전자들이 delocalized 되어있음. $\rightarrow$ dielectric constant가 큼. 

유기반도체: 전자들이 localized 되어있음. $\rightarrow$ dilelectric constant가 작다.

예제 1) 가운데 metal, 겉 dielectric

<img src="/images/figure/image-20230504172354086.png" alt="image-20230504172354086" style="zoom:80%;" />
$$
D = \frac{Q}{4 \pi r^2}\hat{r}
\\
E = \frac{Q}{4 \pi \epsilon r^2}\hat{r}~~ : a<r<b
\\
E= \frac{Q}{4 \pi \epsilon_0 r^2} \hat{r}~~ : r>b
$$

1) P를 구한다.
   $$
   P = \epsilon_0 \chi_e E = \frac{\epsilon_0 \chi_e Q}{4 \pi \epsilon r^2}\hat{r}
   \\
   \therefore \rho_b = - \triangledown \cdot \text{P = 0 이므로, 아래 그림처럼 bound charge 를 생각하자}
   $$
   <img src="/images/figure/image-20230504173036791.png" alt="image-20230504173036791" style="zoom:80%;" />

   <img src="/images/figure/image-20230504173242608.png" alt="image-20230504173242608" />

따라서, 각 interface 사이에 전기장의 불연속이 생긴다.

2. $\sigma_b = \bold{P}\cdot \hat{n}$ 을 구한다.
   $$
   \rho_b = \bold{P \cdot \hat{n}} = \frac{\epsilon _0 \chi_e Q}{4 \pi \epsilon b^2} \text{at the outer surface}
   \\
   \rho_b = \bold{P \cdot \hat{n}} = \frac{\epsilon _0 \chi_e Q}{4 \pi \epsilon a^2} \text{at the innter surface}
   \\
   \text{확인 : 각 각}~ 4\pi b^2 or 4\pi a^2 \text{을 곱하면 두개 더하고 0이 되는 것을 확인 할 수 있다.}
   $$

---

#### Boundary Value Problems with Linear Dilectrics

$$
\rho_b = - \triangledown \cdot P = -(\frac{\chi _e}{1 + \chi _e})\rho _{free}
\\
\text{만약} ~\rho _{free} \text{가 0이라면} ~\rho _ b \text{도 0이다.}
\\
\text{따라서 Linear homogeneous(거리무관) dielectric에서 Laplace'equation을 적용해도 된다.}
$$



에제 2)

<img src="/images/figure/image-20230504174536392.png" alt="image-20230504174536392" style="zoom:80%;" />
$$
\rho _b = -\triangledown \cdot P = -(\frac{\chi_e}{1+\chi_e})\rho _f
\\
\rho_f \text{가 0이므로, } \rho_b\text{도 0이다.}
$$
  경계조건 : 
$$
1. V_{in} = V_{out} ~~\text{당연히 연속}
\\
2. \epsilon \frac{\partial V_{in}}{\partial r} = \epsilon_r \frac{\partial V_{out}}{\partial r} ~~ \text{D가 연속인 조건}
\\
3. V_{out} \rightarrow -E_0 r cos\theta ~~\text{Legendre polynomial}
$$

---

#### 에너지 

**W = W(q, V) 의 함수이다. **
$$
\alpha : \text{0에서 1까지 charge를 모은다고 생각해보자.}
\\
dW = dW(\alpha q, \alpha V) = \int_{\text{all space}} (\alpha V)(\rho _F d \alpha) d\tau 
\\
\therefore \text{아무것도 없는 공간에서 Final까지 모든 Energy를 계산하면 다음과 같다.}
\\
\begin{align}
W &= \int ^{1}_{0}\alpha ~ d\alpha  \int _{\text{all space}} V\rho_F~ d\tau = \frac{1}{2}\int _{\text{all space}} V\rho_F~ d\tau
\\
W &= \frac{1}{2} \int_{\text{all space}}V(\triangledown \cdot \vec{D}) d\tau = \int _{\text{all space}}(\triangledown \cdot(V \vec{D}) - \vec{D}\cdot\triangledown V )d\tau
\\
W &= \frac{1}{2}\int_{\text{S at} \infty} V \vec{D}\cdot da + \frac{1}{2}\int_{\text{all space}} \vec{D} \cdot \vec{E}~d\tau
\\
W &= \frac{1}{2}\int_{\text{all space}} \vec{D} \cdot \vec{E} ~d\tau
\end{align}
$$
<img src="/images/figure/image-20230619135124479.png" alt="image-20230619135124479" />

(1)은 spring이 고려가 안되어있고, (2)는 간접적으로 고려되어있다.

이는 (1)의 전기장이 Macrosopic의 charge를 source로 생각하였기 때문이다.

---

#### 힘

$$
F = -F_{me} = - \frac{\delta W(Q, x)}{\delta x}\mid _{Q}  : \text{energy}
\\
F = -F_{me} = - \frac{\delta W(V, x)}{\delta x}\mid _{V} : \text{coenergy}
$$

