---
layout: single
title: "14)MS Contanct and Schottky Diodes"
typora-root-url: ../
categories : "Fundamental-of-Semicondutor"
tag : diode
#tag : [me, me2, me3]
toc : true
toc_sticky : true
author_profile : false
---
## Fundamental of semiconductor

#### 개념잡기 

1. Vacuum Level 

   <img src="/images/figure/image-20230718162811336.png" alt="image-20230718162811336" style="zoom:67%;" />

   전자 한개를 표면 밖으로 꺼낸 후의 전자의 E

   그러나 표면 바로 밖의 에너지 ($E_{vac}(s)$)$\neq$ 표면에서 아주 먼 곳의 에너지($E_{vac}(\infty)$) 이다. 

   어떻게 생각해야 할까?

반도체 소자에서 말하는 Vacuum Level은  Local Vacuum Level이다.

Local = 'microscopic한 것은 고려하지 않고 macroscopic한 것만 고려하겠다는 것이다.' --> 원자핵을 고려 x 

즉, Space Charge만 고려하겠다는 것이고, 이는 Band Bending을 따라서 연속적으로 나타난다. 
$$
\text{Local Vaccum level} = E^{\text{loc}}_{\text{vac}}(s)
$$

ex) 서울대 정문에 있는 harmonic oscillator, 서울대 301동에 있는 harmonic oscillator 에서 harmonic oscillator를 제외하고 생각하는 것

UPS를 측정할 때도 dector가 $E^{\text{loc}}_{\text{vac}}(d)$ 의 관점에서 감지를 하는 것이기 때문에, UPS data도 Local Vaccum level을 의미한다.

<img src="/images/14. MS Contacts and Schottky Diodes/image-20231226102105846.png" alt="image-20231226102105846" style="zoom:67%;" />



2. Electron Affinity

$$
\chi = E^{loc}_{vac} - E_c
$$

 전자를 bottom of the conduction band에서 local vacuum level까지 제거하는 데 필요한 에너지이다.



3. Ionization Energy

$$
IE = E^{loc}_{vac} - E_v
$$

전자를 top of the valence band에서 local vacuum level까지 제거하는 데 필요한 에너지이다.



---

#### Ideal MS Contact

생각하는 순서는 다음과 같다.

1) $E_F$가 Flat 하게 설정하기
2) Space Charge에 대한 Band Bending 그려주기
3) $E^{loc}_{vac}$ 연속적으로 그려주기 

***n doping 은 약한 금속 p doping은 홀의 바다 라고 생각하면 편하다***

***금속은 전기장이 없다***

<img src="/images/figure/image-20221226213141988.png" alt="image-20221226213141988" style="zoom:70%;" />

이 그림이 위의 순서에 따라 그려질 수 있어야한다.

Surface potential-energy barrier는 다음과 같다.
$$
\Phi_B = \Phi_M - \chi \text{~ in MS(n-type) contact}
\\
\text{Surface potential energy barrier = Metal Work function - Semiconductor electron affinity}
$$

---

#### Schottky Diode

Schottky Diode를 구성함으로써 p-n diode와 같은 Rectifying 작용을하는 다이오드를 만들 수 있다.

<img src="/images/figure/image-20221226213640441.png" alt="image-20221226213640441" style="zoom:80%;" />

MS(n-type) Diode를 보면 Schottky Diode이고 Majority Carrier인 전자가 전자의 바다인 금속으로 넘어가게 된다.

<img src="/images/figure/image-20221226213834417.png" alt="image-20221226213834417" style="zoom:80%;" />

이에 따라 Built in Voltage는 다음과 같이 기술된다.
$$
V_{Bi} = \frac{1}{q}(\Phi_B - (E_c - E_F)_{FB})
$$
금속은 전기장이 0이므로 넘어간 전자는 금속의 surface에 delta function으로 존재한다.

<img src="/images/figure/image-20221226214040638.png" alt="image-20221226214040638" style="zoom:80%;" />

이에 따른 전기장과 Voltage는 다음 그림처럼 서술된다.

<img src="/images/figure/image-20221226214121397.png" alt="image-20221226214121397" /><img src="/images/figure/image-20221226214131734.png" alt="image-20221226214131734" />

이를 적분을 통해 서술하고, $V(0)=-(V_{Bi}-V_A)$ 로 생각될 수 있다. 
$$
\therefore W = \left[\frac{2K_S \epsilon_0}{qN_D}(V_{Bi}-V_{A})\right]^{1/2}
$$
***Schottky Diode의 I-V 특성을 살펴보려 한다.***

***Forward Bias***

Schottky diode는 n-type semiconductor에서 majority carrier가 금속으로 넘어가는 것이기 때문에 majority carrier가 전자의 바다로 들어간다. 따라서, diffusion이 아닌 새로운 방식의 설명이 필요하다. 따라서, 이를 ***Thermionic Emission Current***라 한다.
$$
KE_x \geq q(V_{Bi} - V_A) \text{여야 하므로}
\\
\vert v_X \vert\geq v_{min} \equiv \left[\frac{2q}{m^* _n}(V_{Bi} - V_A)\right]^{1/2}
$$
Current 에 대한 공식으로 Current 식을 구할 수 있다.
$$
I_{S \rightarrow M} = - q\cdot~A\cdot~v_x~n(v_x)
\\
I_{S \rightarrow M} = - q\cdot~A\int ^{-V_{min}}_{\infty}v_x~n(v_x)dx
\\
\text{이를 알려진 식으로 적분하면 다음의 결과를 얻을 수 있다.}
\\
I_{S \rightarrow M} = \Alpha s\Alpha^* \cdot T^2 \cdot e^{-\Phi_B/kT} e^{qV_A /kT}
$$
위 식을 정리하면 다음을 얻을 수 있다.
$$
I = I_s \left(e^{qV_A/kT}-1\right)
\\
I_s \equiv \Alpha s\Alpha^* \cdot T^2 \cdot e^{-\Phi_B/kT}
$$
***Reverse Bias***

<img src="/images/figure/image-20221226222326955.png" alt="image-20221226222326955" style="zoom:80%;" />

Reverse Bias 전압을 가함에 따라 전자의 바다인 금속에서 약한 금속은 n-type semiconductor로 전자가 넘어간다. 따라서, 금속의 surface에 delta function으로 charge가 생긴다. 이때 이를 쉽게 생각하기 위해서 **Image Charge**를 도입할 수 있다. 따라서, 금속에 +전하가 n-type의 -전하와 같이 있다고 생각할 수 있고 이에 Columb Interaction(+입자에 대해 생각 ex) 수소원자핵)에 의해 전기장이 발생한다. 이에 따라 $\Phi_B$가 낮아지게 된다. 이를 **Schottky Barrier Lowering** 이라 한다.

따라서, 역전압이 커짐에 따라 Current가 증가한다.

***AC Response***

Metal에서의 + charge는 delta function 이므로 움직이지 않고, n-type semicondutcor의 width만 변하게 된다.
$$
C = K_s \epsilon _0 \frac{A}{W}
\\
\therefore ~C =\frac{K_s \epsilon _0 A}{\left[\frac{2K_s \epsilon_0}{qN_D}(V_{Bi}-V_A)\right]^{1/2}}
$$
Schottky Diode는 Majority Carrier에 의해 움직이므로 diffusion capacitance or diffusion conductance가 거의 없다. 

#### thermionic emission

<img src="/images/figure/image-20230719211851757.png" alt="image-20230719211851757" style="zoom:80%;" />

전압을 건 상태에서 semiconductor의 majority carrier가 barrier가 작기 때문에 열적으로 전자가 metal 쪽으로 넘어가는 current가 우세할 때 이를 thermionic emission이라고 한다.

따라서 junction capacitance만 존재하며 굉장히 빠르게 AC에 반응한다.

---

#### Non Ideal Diode

실제로는 Metal에 Surface charges가 반드시 존재하기 때문에 ***Fermi Level 'pin'***이 발생한다.

n-type Semiconductor의 경우 밴드갭의 2/3의 $\Phi_B$ 가 발생한다.

p-type Semiconductor의 경우 밴드갭의 1/3의 $\Phi_B$가 발생한다.

 즉, Ohmic Contact을 못 만든다.

따라서 이에 대한 해결책으로 반도체에 Depletion Region 에 Highly Doping을 하여 Tunneling 현상을 일어나도록 한다.



QD 소자에서도 반드시 어디선가 Pining이 발생하겠네. 