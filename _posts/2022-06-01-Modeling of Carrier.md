---
layout: single
title: "2)Modeling of carrier"
typora-root-url: ../
categories : "Fundamental-of-Semicondutor"
tag : carrier
#tag : [me, me2, me3]
toc : true
toc_sticky : true
author_profile : false
---
## Fundamental of semiconductor

* Carrier는 WavePacket이다.
* Modeling을 한다는 것은 현상을 간단한 형태로 나타내는 것이다.
* Carrier는 전하를 운반하는 entities이다.

금속의 전하 운반자는 electron이다.

그렇다면 금속이 아닌 insulator 또는 반도체의 Carrier는 무엇일까?

이를 설명하기 위해서는 Electron + Phonon의 Coupling을 이해해야한다.

전자가 phonon과 coupling 하며 움직이는 것을 상상할 수 있다. 

이러한 개념으로 Polaron = Electron + Phonon의 Coupling 개념이 만들어졌다.

따라서, 이제 Positive Polaron, Negative Polaron으로 분류를 할 수 있고 

이를 더 직관적인 말로 **Carrier** 라고 한다.

<img src="/images/2-1. Modeling of Carrier/image-20230302150835867.png" alt="image-20230302150835867" style="zoom:47%;" />

Polaron 이라는 Wave Packet이 움직인다고 생각하면 좋다.





따라서, Electron Carrier는 자유전자를 이야기하고 Hole Carrier는 자유정공을 이야기한다.

이 구간부터 Electron과 Hole은 Carrier의 Electron과 Hole을 뜻한다.



이번 포스트에서는 Equilibrium condition에서의 Carrier를 Modeling 하려고 한다.

먼저 반도체를 다루는 가장 기본 원소인 Si를 살펴보자.

Si은 다음의 원자 밀도를 갖고있다.
$$
5 \times 10^{22}atoms/cm^{3}
$$
Si 원소 기호는 14이다. 따라서, 다음의 (Bounded+자유)전자 밀도를 갖고있다.
$$
7 \times 10^{23}electrons/cm^{3}
$$
그렇다면 T = 298K에서 electron density는 어떻게 될까?
$$
At ~room ~temperature,~~ n_{i} = 1 \times 10^{10}/cm^{3}~~in ~Si
$$
이는, 1조분의 1로 그냥 체감이 안된다.. 체감할 수 없는 정도의 수이다.

이렇게 적은 정도의 electron을 이번 포스트에서 modeling을 할 예정이다. 이것이 과연 의미가 있는 행동일까? 궁금할 수 있다. 

Doping이나 Voltage가 인가되어있을 때는 electron 수가 많아져 상황이 꽤 달라질 수 있기 때문에 이 modeling이 의미가 있는 행동이다.

---

#### Energy Band model

<img src="/images/2-1. Modeling of Carrier/image-20230821193638071.png" alt="image-20230821193638071" style="zoom:50%;" />

어떻게 원자들이 모일수록 에너지 밴드가 형성 되는 것일까?

원자가 2개가 모이면 다음처럼 생각할 수 있다.

![image-20230821194326797](/images/2-1. Modeling of Carrier/image-20230821194326797.png)

따라서, 이를 에너지(진동수)로 표현하면 다음과 같다.

![image-20230821194348843](/images/2024-08-06-2-Modeling of Carrier/image-20230821194348843-1723795327911-2.png)

원자들이 모일수록 에너지가 더 갈라질 수 있음을 알 수 있다. 

따라서 Si 원자 N개가 있을 때 다음을 알 수 있다.

<img src="/images/2-1. Modeling of Carrier/image-20230821194632357.png" alt="image-20230821194632357" style="zoom:67%;" /><img src="/images/2-1. Modeling of Carrier/image-20230821194648558.png" alt="image-20230821194648558" style="zoom:67%;" /><img src="/images/2-1. Modeling of Carrier/image-20230821194658638.png" alt="image-20230821194658638" style="zoom:67%;" />

원자들이 N개 있으므로, 에너지 준위가 2N개로 분리된다. 전자는 sp3에서 4개 자리가 있으므로 4N, 4N 밴드형태로 분리된다.

---

#### Modeling of Carrier in Equilibrium Condition

Equilibrium condition에서의 Carrier를 Modeling 해보자. 

### <Bloch's theorem>

Solid Crystal에서 진행이 되고 다음의 Hamiltonian은 다음과 같다. 
$$
H\psi = \left(-\frac{h^2}{2m}\triangledown^2+U(r)\right)\psi =\epsilon\psi
$$
이는 일반적인 Hamiltonian과 같고 potential Energy는 주기성을 띤다.
$$
U(\bold r + \bold R) = U(\bold r)
$$
따라서, 이를 대입하고 Hamiltonian 연산자와 k operator 에 대해 적용하면 다음과 같다. 
$$
wavepacket의 ~k는 ~k,~~ planewave의~k는~ \bold k'라고 하자
$$

$$
\psi_{nk}(r) =<r| \int_{-\infty}^{\infty}\left(|K'>dK'~ \psi_{n}(K')\right)= e^{ik\cdot r}u_{nk}(r)
\\
\text{Bloch's theorem : 전자의 함수는 plane wave(전자의 wavefunction)와 원자의 주기의 곱으로 나타낼 수 있다.}
$$


이는 Labeling이 두번이나 되어있어 Collapse가 두번이나 일어난 wavefunction을 의미한다. 따라서, 가장 최소의 기본단위로 생각할 수 있다.

이러한 **wavefunction을 wavepocket으로 만들면 Localized (Bounded+자유)electron model**을 만들 수 있다. 
$$
\psi_{nk}( \bold r, t) = 
\sum_{k'} \left( g(\bold K')\psi_{nk'}(\bold  r)exp\left\{-\frac{i}{\hbar}\epsilon_n(\bold k')t\right\}\right)
$$
**Localized 된 wavepacket을 통해 전자를 semiclassical model로 해석할 수 있다.**

이를 통해 모든 E와 K에 대해 Labeling을 하며 구하면 다음과 같은 그래프가 나온다.

<img src="/images/2024-08-06-2-Modeling of Carrier/image-20221021143559453.png" alt="image-20221021143559453" style="zoom:50%;" />

---

#### Semi-classical modeling of electron dynamics

Equilibrium condition에서 확장을 하여 전자의 dynamics를 서술해보려고한다.

<img src="/images/2024-08-06-2-Modeling of Carrier/image-20221021143816980.png" alt="image-20221021143816980" style="zoom:50%;" />
$$
\text {Figure : Nearly Free model}
\\
E= E_p + E_k= E_k = \frac{\hbar ^2 k^2}{2m} \text{운동에너지만 거의 존재 } \rightarrow \text{포물선으로 존재}
\\
\text{y축 : 에너지, x 축 : 운동량}
\\
\text{if k =0 : 위치에너지만 존재}
$$


Localized electron을 묘사하는 것이므로 First-Brillouin zone에서 생각을 해볼 수 있다. 

* 원자들이 Translational symmetry를 가지고 있으므로 First-Brillouin zone에서 모든 전자의 상태를 기술할 수 있다. 
* 그래프들을 각 Reciprocal Lattice들에서 대칭한 것이라고 생각하면 편하다. 

Semi-Classical model 이므로, 입자에 관해 생각할 수 있다.

따라서, 전자와 양공이라는 입자가 어떤 위치와 속도를 갖는지 알아야한다.
$$
(위치에~대한~시간미분) = R'=v_n(k)=\frac{1}{\hbar}\frac{\partial \epsilon_n(k)}{\partial k}
$$

$$
(운동량에~대한~시간미분) = F_{ext} = \hbar\cdot k' \text{: 전기장을 가하면 k가 커지는 방향으로 움직인다.}
$$

$$
(가속도)=(속도에~대한~시간미분)=\frac{1}{\hbar^2}\frac{\text{d}^2\epsilon(k)}{\text{d}k^2}F_{ext}=\frac{1}{m^*}F_{ext}
$$



이를 해석하면 다음과 같다.

* E-k diagram에서 기울기는 속도를 의미한다.

* E-k diagram에서 전기장이 존재하면 k가 시간에 대해 일정한 크기로 증가한다. 

  ![image-20230821212108268](/images/2024-08-06-2-Modeling of Carrier/image-20230821212108268.png)

  그렇다면 다음처럼 전자는 결국에 localized 된 상태로 움직이지 않을까? X 

  전자는 phonon에 의해 scattering 되기 때문에 평균적인 속도는 양수일 것임. : Drift Velocity.

  ![image-20230821213614770](/images/2024-08-06-2-Modeling of Carrier/image-20230821213614770.png)

  위의 그림처럼 scattering이 있으면 wavefunction의 $K^{'}$(wavepacket의 k임. wavefunction이 공간에 전체적으로 퍼진게 X)가 커졌다 scattering되어 x가 커졌다가 k가 커졌다를 반복하여. 평균적으로 거리는 증가할 것이다.

* E-k diagram에서 두번 미분한 값은 1/(유효질량)로 생각할 수 있다.

![image-20230822095321154](/images/2024-08-06-2-Modeling of Carrier/image-20230822095321154.png)

각 각 점 1개를 Wave packet 이라고 생각하자.

---

#### Modeling of Weakly bounded electron by doping

Weakly bounded는 Bounded가 약하게 되어있는 상태로 자연스럽게 생각할 수 있다.

Bounded 상태는 수소원자의 model을 먼저 생각해볼 수 있다.
$$
H\psi = \left(-\frac{h^2}{2m}\triangledown^2+U(r)\right)\psi =\epsilon\psi
$$

$$
U(r) = \frac{1}{4\pi\epsilon}\cdot\frac{|q|^2}{r}
$$

Weakly Bounded를 수식적으로 살펴보기 전에, Doped Si에서 Weakly bounded electron은 다음의 상황을 생각할 수 있다.

<img src="/images/2024-08-06-2-Modeling of Carrier/image-20221021164836984.png" alt="image-20221021164836984" style="zoom:50%;" />

위의 수소원자 model을 수식적으로 적으면 다음과 같고 이를 위 상황에 맞게 해석할 수 있다.
$$
E_{binding} \simeq -\frac{m_n^* q^4}{2\left(4\pi K_s \epsilon_0 \hbar\right)^2}=\frac{m_n^*}{m_0}\frac{1}{K_s^2}E_{n=1}(수소원자 ~n=1일때)\simeq-0.1eV
$$

* m_n : effective mass
* K_s : dielectric constant

수소원자 n=1 일때의 Binding energy는 13.6eV 이다. 

수소원자의 effective mass는 m_0, dielectric constant는 1이다. 그러나 Doped Si에서 effective mass는 변하게 된다.

Si의 dielectric constant는 11.8을 갖는다. Dielectric constant를 갖는 상황을 조금 더 살표보자.

수소원자는 원자핵과 전자 사이의 아무것도 없다.(진공이다)

그러나 Si의 P+ 주위에는 Polarization으로 인해 전자 구름이 형성된다. 따라서, p+와 전자 사이의 쿨롱의 힘을 줄이는 screening 현상이 일어난다.

그에 대한 크기를 나타낸 것이 Dielectric constant이다. 

따라서, Dielectric constant는 두 전하 사이의 쿨롱 법칙을 설명하기 위해 도입된 constant로 생각할 수 있다.



결론 짓자면, 0.1eV라는 적은 E로 weakly bounded되어있다는 것을 알 수 있고 이를 쉽게 표현하기 위해서 E_c 바로 아래에 E_D를 그려주면 된다.

<img src="/images/2024-08-06-2-Modeling of Carrier/image-20221021170721190.png" alt="image-20221021170721190" style="zoom:50%;" />

