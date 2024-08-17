---
layout: single
title: "5)Identical Particles, Symmetries & Conservation"
typora-root-url: ../
categories : "Quantum-Mechanics"
tag : Quantum
#tag : [me, me2, me3]
toc : true
toc_sticky : true
author_profile : false
---
## Quantum Mechanics 

#### Two Particle System

$$
\Psi(\bold{r_1, ~\bold{r_2, ~t}})\text{에 대해}
\\
\hat{H} = -\frac{\hbar ^2}{2m_1} \triangledown^2_1 - \frac{\hbar ^2}{2m_2} \triangledown^2_2 + V(\bold{r_1}, \bold{r_2}, t) \text{로 작용한다.}
$$

1. Noninteracting Particle

   Two particle are **Entangled**
   $$
   V(\bold{r_1}, \bold{r_2}) = V_1(\bold{r_1}) ~ + ~ V_2(\bold{r_2}) \text{인 상황이다.}
   \\
   \psi(\bold{r_1}, \bold{r_2}) = \psi_a(\bold{r_1}) \psi_b(\bold{r_2})\text{로 변수분리를 할 수 있다.}
   \\
   \text{따라서 다음의 상황에 대해 생각해볼 수 있다.}
   \\
   \Psi(\bold{r_1}, \bold{r_2, t}) = \frac{3}{5}\Psi_a(\bold{r_1}, t)\Psi_b(\bold{r_2}, t) ~ + ~ \frac{4}{5}\Psi_c (\bold{r_1}, t)\Psi_d(\bold{r_2}, t)
   \\
   \text{이는, Particle1에 대해 Ea를 얻으면 Particle2는 반드시 100\%로 Eb를 얻는다.}
   \\
   \text{혹은 Particle2에 대해 Ed를 얻으면 Particle1은 반드시 100\%로 Ec를 얻는다.}
   $$

2. Central Potentials
   $$
   V(\bold{r_1, \bold{r_2}}) \rightarrow V(\mid \bold{r_1}-\bold{r_2} \mid)\text{인 상황이다.}
   \\
   V(\bold{r_1}, \bold{r_2}) = \frac{1}{4 \pi \epsilon _0}\left( -\frac{2e^2}{\mid \bold{r_1}\mid} - \frac{2e^2}{\mid \bold{r_2} \mid} + \frac{e^2}{\mid \bold{r_1} - \bold{r_2} \mid }\right) \text{로 나타낼 수 있다.}
   \\
   $$



#### Bosons and Fermions

스핀을 갖는 입자들을 구별할 수 없을 때, 다음의 스핀을 갖는 입자의 위치에 대한 psi 식으로 나타낼 수 있다. 

다음은 공리처럼 받아들이자.
$$
\psi _{\pm} ( \bold{r_1}, \bold{r_2}) = \frac{1}{\sqrt{2}} [ \psi_a(\bold{r_1})\psi_b(\bold{r_2}) ~\pm ~ \psi_b{(\bold{r_1})}\psi_a(\bold{r_2})]
\\
bosons으로 ~구성된 ~\psi ~: \psi_+ (\bold{r_2}, \bold{r_1}) = \psi_+(\bold{r_1}, \bold{r_2}) ~\rightarrow \bold{symmetric}
\\
fermions으로 ~구성된 ~\psi ~: \psi_-(\bold{r_2}, \bold{r_1}) = -\psi_-(\bold{r_1}, \bold{r_2}) ~\rightarrow \bold{antisymmetric}
$$
또한 다음의 성질을 갖는다.
$$
\text{정수 스핀은 bosons이다.}
\\
\frac{\text{정수}}{2}~\text{스핀은 fermions이다.}
\\
\text{fermions는} ~\psi_a \neq \psi_b \text{를 갖을 수 없다.} \rightarrow \bold{Pauli ~excluion~principle}
$$
ex 5.1)을 통해서 조금 더 알아보자.
$$
\psi_n (x) = \sqrt{\frac{2}{a}} sin\left(\frac{n \pi}{a}x \right), ~E_n = n^2 K
\\
\text{ 1) particles are distinguishable like electron and proton}
\\
\psi_{11} ( x_1, x_2) = \frac{2}{a} sin \left( \frac{ \pi x_1}{a}\right)sin \left( \frac{ \pi x_2}{a}\right), ~ E_{11} = 2K
\\
\text{2) particles are identical bosons}
\\
\psi_{11} ( x_1, x_2) = \frac{\sqrt{2}}{a} \left[ sin \left( \frac{ \pi x_1}{a}\right)sin \left( \frac{ \pi x_2}{a}\right) + sin \left( \frac{ \pi x_2}{a}\right)sin \left( \frac{ \pi x_1}{a}\right) \right], ~ E_{11} = 2K
\\
\psi_{12} ( x_1, x_2) = \frac{\sqrt{2}}{a} \left[ sin \left( \frac{ \pi x_1}{a}\right)sin \left( \frac{ 2\pi x_2}{a}\right) + sin \left( \frac{ \pi x_2}{a}\right)sin \left( \frac{ 2\pi x_1}{a}\right) \right], ~ E_{11} = 5K
\\
3) \text{particles are identical fermions}
\\
\psi_{11} \rightarrow \text{존재할 수 없음.}
\\
\psi_{12} ( x_1, x_2) = \frac{\sqrt{2}}{a} \left[ sin \left( \frac{ \pi x_1}{a}\right)sin \left( \frac{ 2\pi x_2}{a}\right) - sin \left( \frac{ \pi x_2}{a}\right)sin \left( \frac{ 2\pi x_1}{a}\right) \right], ~ E_{11} = 5K
$$
이를 아래를 통해 **Exchange Force** 의 개념으로 표현할 수 있다.

두 입자 사이의 거리의 제곱의 평균은 다음과 같다.
$$
\left< (x_1 - x_2)^2 \right>_\pm = \left< (\triangle x)^2 \right> _d ~\mp~ 2 \mid \left< x \right>_{ab} \mid ^2
$$
따라서, bosons은 distinguishable particles보다 더 거리가 가까워 땡기는 힘의 개념이 작용하고

fermions는 distinguishable particles보다 더 거리가 멀어 미는 힘의 개념이 작용한다. 
$$
\text{단, } \left< x \right> _{ab} \equiv \int x \psi_a(x)^* \psi_b(x)dx \text{이므로 두 함수가 overlap되어 있을 때 힘이 작용한다.}
$$

---

#### Spin

따라서, bosons인지 fermions 인지에 따라 psi가 다르게 나타난다. 

따라서, 이를 구별하는 표기법이 필요하다.
$$
\psi(\bold{r}) \chi
$$
만약 two-particle state라면
$$
\psi(\bold{r_1}, \bold{r_2})\chi(1,2)
$$
모든 입자에 대해 위의 식에서 공리로 받아들였다. 
$$
\text{따라서,} ~ \psi (\bold{r_1}, \bold{r_2}) \chi(1,2) = -\psi(\bold{r_2}, \bold{r_1}) \chi(2 , 1)\text{이 성립한다.}
\\
\\

 \underline{\therefore \text{전자들로 표현된~} \psi \text{는 어떠한 모든 상황에서} ~\bold{antisymmetric} \text{하다.}}
\\
\\
\therefore 1) ~\text{위치가 symmetric하면 spin은 antisymmetric}
\\
\ ~~~2)~\text{위치가 antisymmetric하면 ~spin은 symmtetric}
$$


---

#### Symmetries & Conservation Laws

1. 운동량 보존 

   -- Position - invariant ( 평행이동에 대한 동등성) 을 갖을 때 운동량이 보존된다.

   

2.  각운동량 보존

   -- axis - invariant (축이 바뀌어도 동등성)을 갖을 떄 각운동량이 보존된다.



3. 에너지 보존

   -- time - invariant (시간이 바뀌어도 동등성)을 갖을 때 에너지가 보존된다.



4. symmetrization 보존

​		-- exchange operator는 Hamiltonian operator와 commute하므로 시간에 대해서 보존된다.

​		따라서 시간에 관계 없이 
$$
\mid(1, 2, ..., n)\rangle = \pm \mid ( 1, 2, ..., n)\rangle \text{이 항상 보존된다.(Bosons = +, Fermions = -)}
$$

---

#### Atoms

ex) Helium
$$
\hat{H} = \left[ -\frac{\hbar ^2}{2m} \triangledown^2 _1 -\frac{1}{4 \pi \epsilon_0}\frac{2e^2}{r_1} \right]
+
\left[ -\frac{\hbar ^2}{2m} \triangledown^2 _2 -\frac{1}{4 \pi \epsilon_0}\frac{2e^2}{r_2} \right]
+ \frac{1}{4 \pi \epsilon_0} \frac{e^2}{\mid \bold{r}_1 - \bold{r}_2\mid}
$$

$$
\text{ground state는} ~\psi_{100}(r_{1}) \psi_{100}(r_2)\text{로 표현된다. 이때, total spin은 anti-symmetric}
\\
\text{excited state는} ~\psi_{200}(r_{1})\psi_{100}(r_2) ~~\text{X}
\\
\text{excited state는} ~\psi_{200}(r_{1})\psi_{100}(r_2) + \psi_{200}(r_{2})\psi_{100}(r_1) ~~\text{O}
\\
\text{이 때, total spin은 anti-symmetric이다.}
$$

이러한 방식 및 Hund's Rules로 오비탈이 결정된다.

그렇다면 Hamiltonian은 어떤식으로 표현해야 할까?

***Approximation : Born - Oppenheimer***
$$
\text{양성자 2개가 X1, X2에 위치하고 전자가 x에 위치하는 상황을 생각해보자}
\\
\Psi(x, X_1, X_2) = \psi(x;X_1, X_2)~\chi(X_1, X_2) ---(1)
\\
-\frac{\hbar ^2}{2m_e} \frac{\delta ^ \psi}{\delta x^2} + V(x, X_1, X_2)\psi = E(X_1, X_2)\psi --- (2)
\\
-\sum \frac{\hbar ^2}{2m_j}\frac{\delta ^2 \chi}{\delta X^2 _j} + E(X_1, X_2) \chi = E^{'}\chi ---(3)
$$
(1)을 통해 Psi를 phi와 chi 형태로 나누어 생각한다.

phi : 전자의 configuration을 결정하는 wavefunction

chi : 원자핵의 configuration을 결정한는 wavefunction

chi는 보정값으로, 양성자가 훨씬 무거우니까 양성자에 대한 보정값을 넣어줘야한다.

(2)식을 통해 E(X_1, X_2)를 구하고 (3)식에 Potential 형태로 대입한다. 즉, x로 나타나기 전에 X_1과 X_2에 대한 값들을 모두 구해야한다.

(3)식을 통해 chi를 구한다. 

이를 통해 Psi를 구한다. 

이를 통해 나타난 그래프를 Frank-Condon이라 한다. 

<img src="https://www.researchgate.net/publication/252628866/figure/fig1/AS:669568653619227@1536649015892/Franck-Condon-principle-energy-diagram-The-potential-wells-are-shown-favoring.ppm" alt="1: Franck-Condon principle energy diagram. The potential wells are... |  Download Scientific Diagram" style="zoom:50%;" />

q는 원자핵들 사이의 거리에 대한 정보를 나타낸다 : Configuration Coordinate 

만약, 기체상태라면 q가 커져 resonance가 더 뚜렷하게 나타난다.(wavefunction overlap이 줄어들었기 때문에)

선은 전자의 E가 같은 선을 의미한다 : 전자의 Configuration coordinate

주황색 선은 원자핵의 harmonic oscillate를 의미한다. 원자핵의 Configuration coordinate

---

#### Solid

Electron gas 모델과 Bloch 모델로 나누어 생각할 수 있다.

 ***Free Electron Gas***
$$
V(x,y,z) = 0, 0< x<l_x, 0<y<l_y, 0<z<l_z
\\
\psi_{n_x n_y n_z} = \sqrt{\frac{8}{l_x l_y l_z}} sin\left(\frac{n_x \pi}{l_x}x\right)sin\left(\frac{n_y \pi}{l_y}y\right)sin\left(\frac{n_z \pi}{l_z}z\right)
\\
E_{n_x n_y n_z} = \frac{\hbar^2 k ^2}{2m}
$$
 이 상황에서 Fermi Surface, Fermi Energy, Degeneracy Pressure 개념이 나온다. 책 참조



***Bloch theorem in Band Structure***
$$
V(x+a) = V(x) \text{이다. 이는 다음의 phi로 나타낼 수 있다.}
\\
\psi(x+a) = e^{iqa} \psi(x)
\\
\text{또는}
\\
\psi(x) = e^{iqx} u(x)
$$
즉 위의 아래 식에서 다음으로 해석할 수 있다.
$$
\psi = \text{plane wave} \times \text{주기함수}
\\
\psi \text{는 주기를 나타내는 label q와 E label n으로 나타낸다.}
$$
V(x)를 delta function의 주기함수인 상황이고 

이를 통해 정리하면 다음이 나타낸다.
$$
cos(qa) = cos(ka) + \frac{m \alpha}{\hbar ^2 k }sin(ka)
\\
\text{ q가 정해지면 }k_n \text{이 정해지고 } E_n\text{이 정해진다.}
$$
이를 다음으로도 나타낼 수 있다.
$$
-1\leq f(z) \equiv cos(z) + \beta \frac{sin(z)}{z} \leq 1
\\
\text{ 한 주기 동안에 선의 갯수 N(원자핵)개}
\\
\text{왼쪽 흰색 박스 내의 수: }\frac{N}{2}개
\\
\text{오른쪽 밴드 내의 수 : }N개
$$
<img src="/images/figure/KakaoTalk_20221220_213331115.jpg" alt="KakaoTalk_20221220_213331115" style="zoom:50%;" /><img src="/images/figure/KakaoTalk_20221220_213354640.jpg" alt="KakaoTalk_20221220_213354640" style="zoom:40%;" />

따라서, 원자가 전자 1인 금속은 band의 절반만 채워져서 전기가 잘흐름.

