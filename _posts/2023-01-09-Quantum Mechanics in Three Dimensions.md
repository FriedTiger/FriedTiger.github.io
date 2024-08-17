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

$$
\frac{1}{R}\frac{d}{dr}(r^2 \frac{dR}{dr}) -\frac{2mr^2}{\hbar^2}[V(r)-E]=l(l+1)
\\
u(r) \equiv r R(r) \text{로 나타낼 수 있다.}
$$

이를 정리하면 다음과 같다.
$$
-\frac{\hbar ^2}{2m}\frac{d^2 u }{dr^2}+[V+ \frac{\hbar^2}{2m}\frac{l(l+1)}{r^2}]u = Eu
\\
V_{eff} = V + \frac{\hbar^2}{2m}\frac{l(l+1)}{r^2} \text{로 설정할 수 있다.(원심력과 비슷한 느낌)}
$$
다음 상황에서 Nomarlize를 찾을 수 있다.
$$
\int^\infty _0 \mid u\mid ^2 dr = 1 
$$

---

---

#### Ex) The Hydrogen Atom

$$
V(r) = -\frac{e^2}{4\pi \epsilon_0}\frac{1}{r}
\\
\kappa \equiv \frac{\sqrt{-2m_e E}}{\hbar} \text{ : Scaling}
\\
\rho \equiv \kappa r \text{ : 단위 없애기}, \rho_0 \equiv \frac{m_e e^2}{2\pi \epsilon_0 \hbar ^2 \kappa}
$$

를 The Radial Equation에 대입하면 다음과 같다.
$$
\frac{d^2 u}{d \rho ^2} = [1-\frac{\rho_0}{\rho}+\frac{l(l+1)}{\rho ^2}]u
$$

1. $$
   \rho \rightarrow \infty \text{일 때}
   \\
   u(\rho) \approx A e^{-p}
   $$

2. $$
   \rho \rightarrow 0 \text{일 때}
   \\
   u(\rho) \approx C\rho ^{l+1}
   $$

따라서 이를 조합하면 다음과 같다.
$$
u(\rho) = \rho^{l+1} e^{-p} \times v(\rho)
$$
이를 Power Series로 나타내어 B.C를 rho가 굉장히 클 때의 상황으로 제약하면 다음과 같다.
$$
v(\rho) = c_0\sum^\infty _{j=0} \frac{2^j}{j!} \rho ^j = c_0 e^{2\rho}
$$
 따라서, 다음과 같다.
$$
u(\rho) = c_0 \rho ^{l+1} e^{\rho}
$$
다음 상황에서 Normalize를 찾을 수 있다.
$$
\text{Power Series로 나타낼 때 } C_{N-1} \neq 0 , ~ C_N = 0 \text{을 설정할 수 있다.}
\\
c_{j+1} = \{\frac{2(j+l+1) - \rho_0}{(j+1)(j+2l+2)}\} c_j \text{에서}
\\
2(j+l+1)-\rho_0 = 0 \rightarrow 2(N+l) - \rho_0 = 0
\\
n \equiv N + l \text{로 설정하면}
\\
\rho_0 = 2n
$$
따라서 Bohr fomula는 다음과 같다.
$$
E \sim \kappa \sim \rho_0 \text{의 관계에 의해}
\\
E_n = -[\frac{m_e}{2\hbar ^2}(\frac{e^2}{4\pi\epsilon_0})^2]\frac{1}{n^2} \text{이 성립한다.}
$$
 이를 통해서 각 상태에 대한 psi를 구할 수 있다.
$$
\psi_{nlm}(r, \theta, \phi) = R_{nl}(r)Y^m_l (\theta, \phi)
$$

$$
l\text{은~}N+l\text{에서} ~0\sim n-1\text{의 ~degeneracy를 ~갖는다.}
\\
\text{m은} ~l\text{에}~ \text{대해서} 2l+1\text{의 ~degeneracy를~갖는다.}
\\
\text{따라서,~n에~대하여 ~} 
d(n) = ~ \sum^{n-1}_{l=0} (2l+1) = n^2 \text{이다.}
$$

---

#### Angular Momentum

고전역학에서 각 운동량이란 다음과 같다.
$$
\bold{L} = \bold{r} \times \bold{p}
\\
L_x = yp_z - zp_y,~ L_y = zp_x-xp_z,~ L_z = xp_y - yp_x\\ \text{(in position representation)}
$$
각각의 운동량에 operator를 대입하고 commute한지 여부를 조사하면 다음과 같다.
$$
[L_x, L_y] = i\hbar L_z, ~ [L_y, L_z] = i\hbar L_x, ~ [L_z, L_x] = i\hbar L_y
$$
각 운동량에 대해 언제나 성립한다.

<img src="/images/2023-01-09-Quantum Mechanics in Three Dimensions/KakaoTalk_20221213_203743407-1723885249899-2.jpg" alt="KakaoTalk_20221213_203743407" style="zoom:50%;" />

L^2 에 대해서는 다음이 성립한다.
$$
[L^2, L_x] = [L^2, L_y]=[L^2, L_z]=0
$$

#### Ladder operator

Harmonic oscillator와 같은 방식으로 각 운동량이 commute하지 않기 때문에 ladder operator를 만들 생각을 해야한다.
$$
L_{\pm} \equiv L_x \pm iL_y
\\
[L_z, L_{\pm}] = \pm \hbar L_{\pm}
\\
[L^2, L_{\pm}] = 0
$$
L^2와 L_z는 commute하기 때문에 공통된 eigenfunction f를 갖는 상황을 생각할 수 있다. 

이 때,
$$
L^2 f = \lambda f, ~ L_zf = \mu f
\\
L^2(L_\pm f) = \lambda (L_{\pm} f) ~~\text{(B.C. 로 생각할 수 있다.)}
\\
L_z(L_{\pm}f)=(\mu\pm \hbar)(L_{\pm}f) ~~\text{(ladder operator에 따른 eigenvalue)}
$$
B.C. 설정을 하기 위해서 다음과 같이 가정하자.
$$
L_z f_t = \hbar l f_t
$$
주의해야할 것은 f는 L_z와 L^2에 대한 공통된 eigenfunction이라는 것을 잊지 말자.
$$
L^2 = L_{\pm}L_{\mp} + L^2 _z \mp \hbar L_z \text{를 대입하면 다음을 알 수 있다.}
\\
L^2f_t = \lambda f_t = \hbar^2l(l+1)f_t
\\
L^2f_b = \lambda f_b = \hbar ^2 \bar{l}(\bar{l}-1)f_b
$$
이를 정리하면 다음과 같다. 

L^2에 의해 사다리가 결정된다.

<img src="/images/2023-01-09-Quantum Mechanics in Three Dimensions/KakaoTalk_20221213_222349561-1723885249899-4.png" alt="KakaoTalk_20221213_222349561" style="zoom:50%;" />

#### Eigenfunctions

Angular Momentum에 대한 del 연산자를 spherical coordinate로 기술하면 다음을 알 수 있다.
$$
L^2 = -\hbar ^2[\frac{1}{sin \theta}\frac{\delta}{\delta \theta}(sin \theta \frac{\delta}{\delta \theta})+\frac{1}{\sin^2 \theta}\frac{\delta ^2}{\delta\phi ^2}] = \hbar^2 l(l+1)
$$

| 이름표 (Labe)l      | Operator | Eigenvlaue     | function |
| ------------------- | -------- | -------------- | -------- |
| n                   | H        | E              | phi      |
| l                   | L^2      | hbar^2 *l(l+1) | phi      |
| m = l, l-1, ..., -l | L_z      | hbar * m       | phi      |

** Angular Momentum으로 풀었을 시 l은 0, 1/2, 1, 3/2를 갖는다. 그러나 전자의 수소 원자는 0, 1, 2, 3궤도를  가졌 다.

---

---

#### Spin

**저자 왈"양자역학이  헷갈릴 때는 spin chapter로 와서 다시 읽어보아라 chapter 4.4**

위의 정리를 통해
$$
l = 0, \frac{1}{2}, ~1, ~\frac{3}{2}, ~2, \cdot \cdot \cdot
\\
\text{을 알 수 있다.}
$$
Hydrogen atom in spherical coordination과 Angular equation in orthogonal coordiation에서 l의 의미는 각운동량으로 모두 궤도를 나타내었다.

ordinary matters(protons, neutrons, and electrons)같은 경우 
$$
Spin ( \text{S}= I w)
$$
으로 지구의 자전과 유사한 Intrinsic angular momentum(S)의 값을 나타낸다. 즉, 고유한 성질을 갖고있는 것이므로 (위치, 운동량, 에너지)와 같은 좌표계로 나타낼 수 없다.

Spin의 전개는 l의 값을 구하는 것과 비슷하므로 결과를 나타내면 다음과 같다.
$$
S^2 \mid sm \rangle = \hbar ^2 l(l+1) \mid s m \rangle
\\
S_z \mid sm \rangle = \hbar m \mid s m \rangle
\\
S_{\pm} = \hbar \sqrt{s(s+1) - m(m\pm 1)} ~\mid s(m\pm1)\rangle
\\
S_{\pm} \equiv S_x \pm i S_y
$$
또한 다음의 사실을 알고 있다.
$$
m = -s, -s + 1, \cdot \cdot \cdot, s-1, s
$$
전자는 s = 1/2이기 때문에 m은 -1/2, 1/2 값을 갖는다.

다음과 같이 정의하자.
$$
\chi_+ = \mid \frac{1}{2} \frac{1}{2} \rangle \rightarrow \mid \uparrow \rangle \rightarrow \left(\begin{array}{}1\\ 0\end{array}\right)
\\
\chi_- = \mid \frac{1}{2} -\frac{1}{2} \rangle \rightarrow \mid \downarrow \rangle \rightarrow \left(\begin{array}{}0\\ 1\end{array}\right) 
\\
\text{각각 base이므로, 따라서 다음과 같이 나타낼 수 있다.}
\\
\chi = \left(\begin{array}{}a\\b\end{array}\right) = a\chi _ + +b\chi_-
$$
또한 다음의 중요한 개념을 확인할 수 있다.
$$
\text{S}^2 = \left(\begin{array}{}c~~d \\ e~~f\end{array}\right)
\\
c = \langle \uparrow \mid \text{S}^2 \mid \uparrow \rangle
\\
d = \langle \uparrow \mid \text{S}^2 \mid \downarrow \rangle
\\
e = \langle \downarrow \mid \text{S}^2 \mid \uparrow \rangle
\\
f = \langle \downarrow \mid \text{S}^2 \mid \downarrow \rangle
$$
따라서 다음과 같이 나타낼 수 있다.
$$
\text{S}_z \chi_+ = \frac{\hbar}{2}\chi_+, ~S_z\chi_- = -\frac{\hbar}{2}\chi_-
\\
\therefore \text{S}_z = \frac{\hbar}{2} \left(\begin{array}{} 1~~~~~0 \\ 0~-1\end{array}\right)
\\
\text{S}_+ = \hbar \left(\begin{array}{} 0~~1 \\ 0~~0\end{array}\right), ~\text{S}_- = \hbar \left(\begin{array}{} 0~~0 \\ 1 ~~0\end{array}\right)
\\
\text{S}_x = \frac{\hbar }{2} \left(\begin{array}{} 0~~1 \\ 1 ~~0\end{array}\right), \text{S}_y = \frac{\hbar }{2} \left(\begin{array}{} 0~-i \\ i~~~~~0\end{array}\right)
$$
따라서,  두번째의 식을 첫번째의 식을 통해 나타낼 수 있다.
$$
\chi = a \chi^{(z)}_+ +b \chi^{(z)}_- 
\\
\chi = (\frac{a+b}{\sqrt{2}})\chi^{(x)}_+ + (\frac{a-b}{\sqrt{2}})\chi^{(x)}_ -
$$
** 궁금한점 

만약, a와 b가 임의의 z축에서 결정될 때, x축에서 각 base로 어떻게 되어있는지 알 수 없네.. --> 

base를 공유하지 않네 그러나 eigenvlaue는 같다.--> commute하지 않다의 정의같다.

#### Electron in a Magnetic Field

magnetic dipole momnet는 전자의 궤도운동에서 비롯된 것이다.
$$
\bold{\mu} = \gamma~ \text{S} ~~~~~	\gamma = \text{gyromagnetic ratio}
$$
자기장과 Magnetic dipole의 식을 통해서 자기장과 스핀의 관계를 알 수 있다.
$$
H = - \mu \cdot \bold{B}
\\
\text{H} = -\gamma \bold{B} \cdot \text{S}
$$
이를 실험으로 증명하였다. **The Stern-Gerlach experiment**

---



#### Addition of Angular Moment

spin s1과 spin s2를 갖는 두개의 particles들이 있다고 가정해보자.

우리는 S^2의 연산자와 S_x, S_y, S_z 에 대해서 배웠다. 
$$
S_z = S^{(1)}_z + S^{(2)}_z \rightarrow m = m_1 + m_2
$$
그렇다면 S 연산자는 무엇일까?

#### 1) Spin : spin만을 고려한 두 입자의 상황

spin을 1/2를 갖는 전자와 양성자의 상황을 생각해보자
$$
\mid \uparrow \uparrow \rangle = \mid \frac{1}{2} \frac{1}{2} \frac{1}{2} \frac{1}{2} \rangle, m = 1
\\
\mid \uparrow \downarrow \rangle = \mid \frac{1}{2} \frac{1}{2} \frac{1}{2} -\frac{1}{2} \rangle, m = 0
\\
\mid \downarrow \uparrow \rangle = \mid \frac{1}{2} \frac{1}{2} -\frac{1}{2} \frac{1}{2} \rangle, m = 0
\\
\mid \downarrow \downarrow \rangle = \mid \frac{1}{2} \frac{1}{2} -\frac{1}{2} -\frac{1}{2} \rangle, m =- 1
$$
이름 다음과 같이 두 spin composite state에 대해서 L ^2(S^2)과 L_z(m)에 대한 그림으로 나타낼 수 있다.

<img src="/images/2023-01-09-Quantum Mechanics in Three Dimensions/KakaoTalk_20221218_090434187-1723885249899-3.jpg" alt="KakaoTalk_20221218_090434187" style="zoom:50%;" />

따라서, 이전과 마찬가지로 Lowering operator 에 대해 생각해 볼 수 있다.
$$
S_-{\mid \uparrow \uparrow \rangle = (S^{(1)}_- \mid \uparrow \rangle)}\mid \uparrow \rangle + \mid \uparrow \rangle (S^{(2)}_- \mid \uparrow \rangle)
\\
=\hbar(\mid \downarrow \uparrow \rangle + \mid \uparrow \downarrow \rangle)
$$
이를 통해서 다음을 확인할 수 있다.
$$
\text{Triplet in notation} \mid s m \rangle
\\\mid 1 1 \rangle = \mid \uparrow \uparrow \rangle
\\
\mid 1 0 \rangle = \frac{1}{\sqrt{2}}(\mid \uparrow \downarrow \rangle + \mid \downarrow \uparrow \rangle)
\\
\mid 1 -1\rangle = \mid \downarrow \downarrow \rangle
\\
\\
\text{다음 상황에 대해 예상해 볼 수 있다.}
\\
\text{Singlet in notation } \mid s m \rangle
\\
\mid 0 0 \rangle = \frac{1}{\sqrt{2}}(\mid \uparrow \downarrow \rangle - \mid \downarrow \uparrow \rangle) \\
\bold{\text{주의 : s = s1 + s2 가~아님}}
$$
반드시 알아야 하고 주의해야할 것은 다음과 같다.
$$
\text{1. total spin에 대한 이름표는 s이고 이에 대한 m값은 s, s-1,} \cdot\cdot\cdot, \text{-s를 갖는다.}
\\
\text{2.  total spin s에 대해} ~S^2\mid s m \rangle = \hbar^2 s(s+1) \mid s m \rangle\text{을 만족시키면 된다.}
\\
\text{증명방법} : S^2  \mid0~0\rangle = [(S^{(1)})^2 + (S^{(2)})^2 +2 S^{(1)} S^{(2)} ] \mid 0~0 \rangle = \hbar^2 0(0+1) \mid 0~0 \rangle
$$
즉 다음의 결론을 얻을 수 있다. 
$$
S_1 = \frac{1}{2},~ S_2 = \frac{1}{2} \text{일 때}
\\
s = (s_1 + s_2), (s_1 + s_2 -1), \cdot \cdot \cdot, ~\mid s_1 - s_2 \mid
$$

---

#### 2) Spin : spatial part(궤도운동) + spin part(스핀)을 고려한 두 입자의 상황

$$
\overrightarrow{J} = \overrightarrow{L} + \overrightarrow{S}
\\
\text{total Angular momentum = 궤도 운동량 + 스핀}
$$



보충자료에 의해 다음이 성립한다.
$$
\text{operator} ~J^2, J_z,J^2_1, J^2_2 \text{은 모두 commute해서 공통된 eigenstate를 갖는다.}
$$
따라서, 이를 다음과 같이 표기할 수 있다.
$$
\mid j ~ m ~ j_1 ~ j_2 \rangle = \sum _{m1+m2 = m} C^{j_1 j_2 j}_{m_1 m_2 m} \mid j_1~m_1~j_2~m_2 \rangle
\\
\text{이 때} C^{j_1~j_2~j}_{m_1 m_2 m}=\langle j_1~m_1~j_2~m_2 \mid j~m~j_1~j_2 \rangle : \bold{Clebsh-Gordan coefficients}
$$

<img src="/images/2023-01-09-Quantum Mechanics in Three Dimensions/KakaoTalk_20221218_155149421-1723885249899-1.png" alt="KakaoTalk_20221218_155149421" style="zoom:50%;" />

---

#### 정리



입자 한개에 대한 이름표 :
$$
\Psi = \mid n ~l ~m \rangle \mid s ~ m_s \rangle \text{의 이름표를 갖는 ~} \psi\text{의 선형 조합}
$$


| 이름표 (Label)                                   | Operator | Eigenvlaue      |
| ------------------------------------------------ | -------- | --------------- |
| n                                                | H        | E               |
| l                                                | L^2      | hbar^2 *l(l+1)  |
| l의 m = l, l-1, ..., -l                          | L_z      | hbar * m        |
| s                                                | S^2      | hbar^2 * s(s+1) |
| s의 m_s = s, s-1, ..., -s                        | S_z      | hbar * m        |
| s(total spin) = s1+s2, ..., abs(s1 - s2)         | S^2      | hbar^2*s(s+1)   |
| s(total spin)의 m_s = s, s-1, ..., -s            | S_z      |                 |
| j = l+s로 구성가능한 모든 수                     | j^2      | hbar^2 * j(j+1) |
| j의 m= j, j-1, ... , -j                          | j_z      | hbar * j        |
| j(total angular moment) = j1+j2, ..., abs(j1-j2) | J ^2     | hbar^2 * j(j+1) |
| j(total angular moment)의  m = j, j-1, ..., -j   | J_z      | hbar * j        |