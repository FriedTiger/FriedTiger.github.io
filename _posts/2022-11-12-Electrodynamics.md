---
layout: single
title: "6)Electrodynamics"
typora-root-url: ../
categories : "Electromagnetic"
tag : electrodynamics
#tag : [me, me2, me3]
toc : true
toc_sticky : true
author_profile : false
---
## Electromagnetic 

**자기장은 일을 하지 않는다. **

**자기장이 있는 곳에서 에너지의 전달이 있다면 에너지가 어떻게 전달 되었을까를 생각하자.**

**유도되는 전기장, 자기장 발생시 phase shift가 생긴다. **

#### Ohm's law

$$
\begin{align}
J &= \sigma f \text{ : f는 unit charge가 받는 힘}
\\
\therefore ~~J &=\sigma(E + v \times B)
\\
&\text{charge의 속도가 아주 느리므로}
\\
J &= \sigma E
\end{align}
$$

---

#### Electromotive Force

$$
f = f_s + E
\\
: \text{전하가 받는 힘은 source에 의한 힘과 source로 인해 생기는 전기장으로 생각할 수 있다.}
$$

유도기전력 Electromotive Force ( **EMF**)
$$
1.~ \epsilon = \int f\cdot  dl = \int (f_s+E)\cdot dl = \int f_s \cdot dl
\\
2. V = - \int^b _a \vec{E}\cdot dl = \int^b _af_s \cdot dl = \oint^b _af_s \cdot dl = \epsilon
\\
\text{1과 2 중에 1로 해석하는 것이 더 편하다.}
$$
베터리를 상상속으로 생각하자.

예제)

<img src="/images/figure/image-20230623225653090.png" alt="image-20230623225653090" style="zoom:70%;" /><img src="/images/figure/image-20230623225718387.png" alt="image-20230623225718387" style="zoom:80%;" />

1. particle 입자를 생각하자.
2. Lorentz froce에 의해 위로 움직인다.
3. 시점을 외부시점에서 생각하면 particle은 오른쪽그림과 같이 $\vec{w}$ 로 움직인다.
4. 따라서. $F = q \vec{w} \times \vec{B}$ 이므로 $f_{mag}$ 를 생각할 수 있다.
5. 따라서 EMF 는 $vB(b-a)$ , 이를 위해 해주는 근천적 힘은 uB임을 알 수 있다.



**Flux rule **

유도기전력 EMF를 쉽게 Flux의 개념으로 구할 수 있다.
$$
\epsilon = - \frac{d\Phi}{dt} : \Phi = BA
$$
**유도기전력을 베터리로 해석 **

<img src="/images/figure/image-20230623230708822.png" alt="image-20230623230708822" style="zoom:67%;" />

배터리의 원천은 속도를 v로 가져가는 외부힘이다.

---

#### Faraday's Law

<img src="/images/figure/image-20230624003510853.png" alt="image-20230624003510853" />

(a)는 위의 그림을 나타낸 그림이다.

(b)처럼 자기장을 이동시킨다면 어떻게 해석할 수 있을까?

입자의 입장에서 입자는 움직이지 않는다.

이를 페러더이는 자기장 경계에서의 자기장 변화로 설명하였다. --> **변화하는 자기장이 전기장을 유도한다.**
$$
\text{Faraday's Law : } \triangledown \times E = -\frac{\partial B}{\partial t}
$$

#### Universial Flux rule

$$
\epsilon = - \frac{\partial \Phi}{\partial t}
$$

자기장은 일을 전달하지 않는다.

그러나, 시간에 따라 변하는 자기장은 전기장의 변화를 일으킴으로 에너지를 전달한다.

이러한 에너지를 EMF라 하고 이는 면적을 통과하는 flux의 시간변화율로 쉽게 구할 수 있다.



#### 주의 점

$$
\text{Ampere's Law} : \triangledown \times B = \mu_0\vec{J} \text{는 qusaistatic 상황에서만 성립한다.}
\\
\text{전류의 변화가 자기장에 linear(time - independent) 하게 변할것이란 보장이 없다.}
\\
\text{따라서, 전기장의 변화가 자기장에 변화를 일으키기까지 시간이 우리가 구하고자하는 범위보다 짧은 구간이면 괜찮다. }
\\
\text{따라서, 일반적으로 성립한다.}
$$



---

#### Lenz's Law

$$
\text{Nature abhors a chang in flux}
$$

<img src="/images/figure/image-20230624003905616.png" alt="image-20230624003905616" style="zoom:80%;" />

위의 상황에서 유도기전력은 자기장 변화에 마이너스 부호를 갖는다. 

--> **힘을 방해하는 방향으로 에너지 전달이 일어난다. **

<img src="/images/figure/image-20230624003952742.png" alt="image-20230624003952742" />

---

#### Inductance

capacitor와 비슷하게 두개의 loop를 상상해볼 수 있다.

<img src="/images/figure/image-20230624205206645.png" alt="image-20230624205206645" style="zoom:67%;" />
$$
\text{Loop1에 흐르는 전류로 인해 생성된 Vector potential은 다음과 같다.}
\\
A_1 = \frac{\mu_0 I_1}{4 \pi}\oint\frac{dl_1}{\eta}
\\
\Phi_B = \int B_1\cdot da_2 = \int (\triangledown \times A_1)\cdot da_2 = \oint A_1 \cdot dl_2 \text{이므로}
\\
\Phi_B = \frac{\mu_o I_1}{4\pi}\oint\frac{dl_1 \cdot l_2}{\eta} \text{이다.}
\\
\text{우리가 관심있는 것은 } \Phi_B \text{이므로, (왜냐하면 에너지 전달이 중요하므로)}
\\
\Phi_2 = M_{21}I_1 이고
\\
M_{21} = \frac{\mu_0}{4 \pi} \oint \frac{dl_1 \cdot dl_2}{\eta} \text{이다.}
$$
**M을 Mutal Inductance라 한다. **

이를 수학적으로 해석하면 다음과 같다.
$$
\begin{align}
&1. M_{12}~\text{완전히 기하학적 양이다. }
\\
&2.M_{12} = M_{21}이다.
\\
\end{align}
$$
이것을 왜 배울까??
$$
\text{ Mutal Inductance 게념을 통해 쉽게 에너지 전달을 이해할 수 있기 때문이다.}
\\
\epsilon_2 = -\frac{\partial \Phi_2}{\partial t} = - M\frac{\partial I_1}{\partial t}
\\
\text{ : Loop1에 current를 시간에 따라 변화시키면 Loop2에 에너지 전달이 생긴다는 것이고 이는 Loop2에 전류가 생긴다는 것을 의미한다.}
$$
그러나 변화하는 전류는 주변 Loop에 대한 에너지 전달 뿐만이 아니라 자신에게도 영향을 미친다.

이를 L로 표현한다.
$$
\epsilon = -L\frac{d I}{d t}
$$
**L을 Self Inductance라 한다. **
$$
\text{L은 어떤의미를 갖을 수 있을까?}
\\
\text{Inductance는 Lenz's law에 의해 변화에 반대되는 방향으로 작용한다.}
\\
\text{따라서, 에너지 저장의 emf로 작동할 것이고 이를} ~\bold{\text{back emf}}\text{라고 한다.}
$$
**회로적 성분 **

<img src="/images/figure/254BB836569B30881A.png" alt="254BB836569B30881A" style="zoom:48%;" />

다음의 RL 회로를 생각해보자. 

전압을 가하고 전류를 흐르는 것을 계산해보면, $I_{max}$ 가 흐르는데 까지 걸리는 시간이 $R < RL $ 회로 인 것을 알 수 있다. 

이는 Inductacne(에너지를 안에 저장함)가 EMF 형태로 에너지를 저장하기 때문이다. 

만약 전압이 교류 전압일 시에는 

저항은 주파수 x L(inductacne)에 비례한다. 

이를 더 생각하면 주파수가 높을수록 에너지를 더 많이 저장하기 때문에 

주파수가 높은 전류는 L회로를 통과하기 어렵다. 

즉, 높은 주파수에 대해 filter 역할을 할 수 있다.

<img src="/images/figure/2212.png" alt="2212" style="zoom:49%;" />

Capacitor는 EMF와 관련된 것은 아니지만 Inductacne와 비교되는 개념으로 여기서 설정한다.

자기장을 통한 EMF로 인한 Inductance와는 다르게 전기장을 통해 에너지를 저장한다. 



전압이 교류 전압일 시에는 

저항은 주파수 x C(capacitor)에 반비례한다. 

이를 더 생각하면 주파수가 낮을수록 에너지를 더 많이 저장하기 때문에

주파수가 낮은 전류는 C회로를 통과하기 어렵다.

즉, 낮은 주파수에 대해 filter역할을 할 수 있다.

---

#### Energy in Magnetic Field

Back EMF를 통해 에너지가 자기장에 대한 형태로 저장되는 의미임을 알 수 있다.

따라서, 자기장의 에너지를 구한다는 것은 Back EMF 에너지를 구한다는 것이다. 

초기 자기장 0 --> 자기장 존재. 계산을 통해 Back EMF를 구할 수 있다.
$$
\frac{dW}{dt} = -\epsilon I = LI\frac{dI}{dt}
\\
\text{이를 적분하면 다음과 같다.}
\\
W = \frac{1}{2}L I^2 
\\
\text{current 변화가 얼마나 오래 걸리는지에 대해 중요하지 않다라는 것을 알 수 있다.}
\\
\text{Magnetic Field에 관한 식으로 정라하면 다음과 같다.}
\\
W = \frac{1}{2}LI^2 = \frac{1}{2\mu_0}\int B^2 d\tau
$$

---

#### Fixed Ampere's Law by Maxwell

$$
\begin{align}
\triangledown \times B = \mu_0\vec{J} : &\text{x}
\\
\triangledown \times B = \mu_0(\vec{J}) + \epsilon_0 \mu_0\vec{E} : &\text{o}
\end{align}
$$

물리적 의미를 조금 더 살펴보면 다음과 같다. Ampere's Law식은 steadystate상태에서의 상황만 다루고 있다. 

steadystate가 아닌 transient상태를 다루기 위해서는 charge 변화에 대해 서술해야한다.

$\triangledown \cdot \vec{J} = - \frac{\partial \rho}{\partial t}$ 이므로 이를 Ampere's Law에 적용하면 Fixed Ampere's Law by Maxwell을 얻을 수 있다.
