---
layout: single
title: "1)Electrostatic"
typora-root-url: ../
categories : "Electromagnetic"
tag : charge
#tag : [me, me2, me3]
toc : true
toc_sticky : true
author_profile : false
---
## Electromagnetic

#### Columbs's laws

$$
E = \frac{Q}{4 \pi r^2 \epsilon_0}
$$

맥스웰 법칙을 풀기 전 기본적으로 Columb's law를 통해 풀 수 있다.



#### Principle of superposition

두 전하사이에 interaction을 고려할 때, 다른 전하들간의 interaction을 고려하지 않아도 된다.



위의 2개의 법칙과 원리가 Electrostatic를 구성하는 가장 기본적인 이론이다.

문제 푸는 방법 : 

쿨롱의 법칙

가우스 법칙

Electric Potential 먼저 구하기

Image Charge

---

#### Dipole

Electrical dipole 은 주변에서 정말 쉽게 발견된다. 

insulator에 경우 한 물질 안에서 발생 가능하고 전기장에 대해 토크도 발생할 수 있다.

Metal에 경우 전기장 속에서 두 Metal을 붙였다가 때는 형식으로 만들 수 있음.(Dipole은 한 물질 안에서만 정의하는 것이 아니구나!)

---

#### Gauss's Law



가우스 법칙은 Line Feild에서의 개념에서 나왔다. 따라서, 가우스 폐곡면 바깥에 있는 charge는 폐곡면 flux에 영향을 주지 않는다.

<img src="/images/figure/\image-20230322162620136.png" alt="image-20230322162620136" style="zoom:50%;" />
$$
\int E \cdot dl = Q
$$
다음의 식은 폐곡면에 대해 항상 성립한다. 

그러나, 착각하지 말아야할 것이 저식을 구했다고 E를 구할 수 있다는 생각은 버리자.

1.  기본식

$\triangledown \cdot E = \frac{\rho}{\epsilon _0}$

미소 볼륨에 대해서 위의 식을 생각할 수 있다.

2. 물리적으로 활용 법 :

   중첩의 원리로서 풀 수 있다.

   **가우스 법칙은 항상 3차원으로 나타내자.**



Gauss's Law는 폐곡면을 잡는 것이 가장 중요하다.

폐곡면을 잡기 위해서는 대칭성을 잘 나타내도록 잡아야한다.

ex) 구, 원기둥, 큐브 등 



* 등전압하에서 Curvature가 큰 금속이 표면 전하 밀도 (surface charge density)가 높은 이유 생각해보기

---

#### Electrostatic Potential

|             | Force              | Energy                             |
| ----------- | ------------------ | ---------------------------------- |
| Newton 역학 | Electric Force (F) | Electrostatic Potential Energy (u) |
| 단위 전하당 | Electric Field (E) | Electric Potential (V)             |

그렇다면 머릿속으로 Electric Field와 Electric Potential은 어떻게 생각하면 좋을까?

1. Reference Point는 V(Electric Potential) 이 0(x --> $\infty$ )인 곳 또는 Gauss'law 외부의 전하로 인한 전압을 생각할 수 있다.

2. 이를 기준으로 V(Electric Potential)이 값이 큰 부분은 언덕으로 생각할 수 있다.

3. 언덕에 공을 올려놓았을 때 공이 굴러가는 순간 속력과 방향은 E(Electric Field)를 가르킨다.

   <img src="/images/figure/image-20230227110407793.png" alt="image-20230227110407793" style="zoom:67%;" />

   Electric Potential을 Diagram으로 표현한 것을 Hill-Diagram이라 부른다.

<img src="/images/figure/hill-diagram.jpg" alt="hill-diagram" style="zoom:67%;" />

---

#### Electrical Potential Energy

$$
u = \frac{1}{2}QV = \frac{1}{2}CV^2
$$

#### eV 

1eV란 전자 1개가 1V 에 Electric Potential를 갖기 위해 필요한 Electric Potential Energy 이다. 

따라서 단위는 J이므로 이를 다음과 같이 표기할 수 있다.
$$
1eV = 1.6 \times 10^{-19}J
$$
만약, 500eV라 주어져 있으면 전자 1개가 500V에 놓이기 위해 필요한 에너지 이다.

---

#### Surface Charge Density

무한한 평면에서 surface charge density가 $\sigma$ 라 하자.

Gaussian pillbox를 만들고 Gauss law를 적용하면 다음을 얻을 수 있다.

<img src="/images/figure/image-20230403214527140.png" alt="image-20230403214527140" />
$$
\int E \cdot da= 2 A\vert E\vert = \frac{1}{\epsilon_0}\sigma A
\\
\therefore E = \frac{\sigma}{2 \epsilon _0} \hat{n}
\\
\text{or}
\\
\triangle E = \frac{\sigma}{\epsilon_0}\hat{n}
$$


이를 물리학적으로 해석하면 다음과 같다. 

1. 무한한 평면에서 surface charge density로 인한 전기장은 모든 공간에서 같다. 
2. 무한한 평면에서 surface charge density에 대해 전기장이 불연속이다.
3. 구든 어떤 도형이든 표면에 대한 전하를 생각할 때 다음처럼 표면에 대한 생각으로 생각하자.

<img src="/images/figure/image-20230404150728715.png" alt="image-20230404150728715" />

도체 안에서 디스크의 방향들의 합이 cancel 됨. 도체 밖에서 디스크의 방향들의 합이 normal vector를 가르킴.

---

#### Boundary Condition



<img src="/images/figure/image-20230403220431716.png" alt="image-20230403220431716" style="zoom: 150%;" />
$$
E^\perp_{above} - E^\perp_{below} = \frac{\sigma}{\epsilon_0}
\\
E^\parallel_{above} = E^\parallel_{below}
$$

- perpendicular 관련 물리적 성질은 위의 식을 참고하자.
- parallel 관련 식은 대칭에 대해 생각해보자.

IF) metal - 진공 계면이라면 
$$
E^\perp_{vaccuum} - E^\perp_{metal} = \frac{\sigma}{\epsilon_0}
\\
\therefore E^\perp_{vaccuum} = \frac{\sigma}{\epsilon _0} \hat{n}
$$
이를 조금더 물리적으로 해석해보자면 metal - 진공계면에서 전기장이 존재하고 이는 메탈 표면에서는 $E_{average}$ 의 전기장이 가해지고 있어 힘들 주고 있다.
$$
E_{average} = \frac{1}{2}(E^\perp_{vaccuum} - E^\perp_{metal}) = \frac{\sigma}{2 \epsilon_0}
\\
\therefore F = \sigma E_{average}=\frac{1}{2 \epsilon _0 }\sigma ^2 \hat{n}~~~ \text{F는 단위 면적당 힘 }
\\
\therefore P = F = \frac{1}{2 \epsilon_0}\sigma^2 = \frac{1}{2 \epsilon_0 }{\epsilon _0}^2 {E^\perp _{vaccuum }}^2 = \frac{\epsilon _0 }{2} E^2 
$$


---

#### Work and Energy

고정되어 있는 점전하가 존재할 때, point a 에서 point b로 Q의 전하를 갖고 있는 입자를 옮길 때 필요한 에너지를 의미한다.
$$
W = \int ^b _a F \cdot dl = -Q \int ^b _a E \cdot dl = Q[V(b) - V(a)]
$$

- 점전하 4개를 assemble 하는데 필요한 에너지는 얼마일까?

$$
\text{전하 q1 : } W = 0
\\
\text{전하 q2 : } W = \frac{1}{4\pi \epsilon_0}q_2 (\frac{q_1}{r_{12}}) 
\\
\text{전하 q3 : } W = \frac{1}{4\pi \epsilon_0}q_3(\frac{q_1}{r_{13}}+\frac{q_2}{r_{23}})
\\
\text{전하 q4 : } W = \frac{1}{4\pi \epsilon_0}q_4(\frac{q_1}{r_{14}}+\frac{q_2}{r_{24}}+\frac{q_2}{r_{34}})
\\
\text{총전하 :} W =\frac{1}{4\pi \epsilon_0}(\frac{q_1 q_2}{r_{12}}+\frac{q_1 q_3}{r_{13}}+\frac{q_1 q_4}{r_{14}}+\frac{q_2 q_3}{r_{23}}+\frac{q_2 q_4}{r_{24}}+\frac{q_3 q_4}{r_{34}})
\\
= \frac{1}{8 \pi \epsilon_0}\sum^n _{i=1} \sum ^n_{j \neq i} \frac{q_i q_j}{r_{ij}} = \frac{1}{2}\sum ^n _{i=1} q_i (\sum ^n _{j \neq i}\frac{1}{4 \pi \epsilon _0}\frac{q_j}{r_{ij}})
\\
= \frac{1}{2}\sum ^n _{i =1} q_i V(\bold{r}_i)
$$

여기서 알 수 있는거는 Electric Potential 이라는 것은 Combination 조합이 아닌 Permutation 순열로 계산 되는구나.

Electrostatic Energy 인 W는 energy stored in the configuration을 의미한다.

- 연속 전하 분포를 assemble 하는데 필요한 에너지는 얼마일까?

$$
W = \frac{1}{2} \int \rho V d \tau
$$

다음처럼 생각을 할 수 도 있다.
$$
\begin{align}
W &= \frac{1}{2}\int \rho V d\tau = \frac{\epsilon_0}{2}\int (\triangledown \cdot E)V d\tau 
\\
&= \frac{\epsilon_0}{2}[-\int E \cdot (\triangledown V)d\tau + \oint_S V E\cdot da] \text{ : integration by parts}
\\
&= \frac{\epsilon_0}{2}(\int _V E^2 d\tau + \oint _s V E \cdot da) : \triangledown V = -E 
\\
&=\frac{\epsilon_0}{2} \int E^2 d\tau ~~\text{ in all space}
\end{align}
$$

에너지가 'Charge의 분포로 저장되어 있다' 또는 '전기장의 형태'로 분포되어 있다 라고 생각할 수 있는 결론을 얻는다.



1. $\frac{\epsilon _0 }{2}E^2$ 은 단위 부피당 에너지를 의미한다.

2. $$
   W _{tot} = \frac{\epsilon_0}{2}\int E^2 d\tau = \frac{\epsilon _0}{2}\int (E_1+E_2)^2 d\tau
   \\
   = \frac{\epsilon_0}{2}\int (E^2_1 + E^2_2 + 2E_1 \cdot E_2 )d\tau
   \\
   = W_1 + W_2 + \epsilon_0 \int E_1 \cdot E_2 d\tau
   $$

   따라서, 중첩의 원리를 따르지 않는다. 사실 전기장과 자기장 모두를 고려해야해서 고려해야하기 때문일까?

3. (11)식과 (12)식이 차이가 난다. (12)식은 음수가 불가능. 

​	그 이유는 점전하를 만든다 라는 것은 임의의 미소의 구에서 charge들 한 점으로 모아야 만들어진다. (10)식을 통해 계산하면 필요한 에너지가 무한대이다. 

따라서, 이 모든 것을 계산한 식이 (12)이므로 (12)은 항상 양수만 된다. 따라서, 12식의 경우는 전지기파와 같이 charge가 없는 곳에서 쓰는 것이 좋다.

4. (11)식은 한 point charge가 가상으로 존재하고 그 주위에 모든 charge들을 configuration 할 때 사용하는 식이다. 모든 현실 상황들이 이런 상황(charge가 이미 고정되어있는 상황)이므로 일반적인 상황에서는 (11)식을 사용한다.

---

#### Metal

<img src="/images/figure/image-20230227201840372.png" alt="image-20230227201840372" style="zoom:67%;" />

1. 금속 표면에 Induced Charge들이 생긴다. 

2. 금속 내부는 항상 전기장이 0이며, 내부에 원자핵만 남는다고 생각하지는 말자.

이유 : 1. 자유전자만 움직이므로 속박전자는 없다.

이유 : 2. 외부 전기장에 값자기 생길 때를 상상해보면 전자들이 표면으로 움직인다. --> 전기장이 0이 될 때까지 움직인다. 

 전자가 움직이는 이유는 금속 내의 전자의 flux가 발생하기 때문이다. (current density). 금속 내부는 전자가 만약에 +y로 움직이여도 -y에서 바로 채워줌. 따라서 전기장이 0이 될 수 밖에 없다.

3. Any net charge는 표면에 위치한다.

<img src="/images/figure/image-20230227202824271.png" alt="image-20230227202824271" style="zoom:67%;" />

1. 이런 상황에서는 내부 금속의 전기장은 0이 되지만, 외부 전기장은 존재한다. 

2. $\text{내부 전기장:} 0 = E_q + E_{induced}+E_{leftover}$ 로 정의되는데, $E_q$ 와 $E_{induced}$ 가 서로 cancel 된다.

   즉, 외부 전하(금속 밖)에 의한 전기장은 금속 외부 표면에 의해 cancel되고, 내부 전하 (q)에 대한 전기장은 금속 내부 표면에 의해 cancel된다.

   즉, **외부 전기장에 의한 값은 내부에 영향을 미치지 않는다.**. ( Faraday Cage)

   그러나, **내부 q는 금속 외부 전기장에 영향을 미친다.**

3. 외부 전기장이 존재하고 전기장 세기가 바뀌더라도 내부의 전기장은 변하지 않음. : Faraday Cage

---

#### Dielectric

외부 전기장 안에 있으면 물질 내의 Charge는 Bound Volume charges($\rho_b$ ), Bound Surface charges($\sigma_b$ )로 나누어 생각한다.<img src="/images/figure/image-20230227205306059.png" alt="image-20230227205306059" style="zoom:150%;" />

1. **Surface Charge Density** 

저자 왈 : Tiny Displacements add up to one large one. 

<img src="/images/figure/image-20230227205634079.png" alt="image-20230227205634079" style="zoom:80%;" />

Single dipole moment = $p$

Polarization = $\bold{P}$ =  $p \cdot A \cdot d$

따라서 다음과 같이 나타낼 수 있다.
$$
\sigma_b = \frac{Q}{A} = \bold{P}
$$

2. **Volume Charge Density**

저자 왈 : If the Polarization is nonuniform, we get accumulations of bound charge **within**  the material

그러나. 생각해보면 위치마다 $\bold{P}$가 다르기 때문에 Volume에서의 $\bold{P}$ 를 구하는 것은 만만치가 않다. 

따라서, $\bold{P}$는 macroscopic 에서의 **Averaged volume dipole moment**라 여기자.

---



#### Capacitance

<img src="/images/figure/image-20230412134608691.png" alt="image-20230412134608691" />
$$
C = \frac{Q_{free}}{V}
\\
\text{두개의 conductor에 각 각 +Q charge, -Q charge를 넣은 상황}
$$
Capacitance는 Q와 Electrical Potential의 비를 나타낸다. 즉, Q와  V는 linear하다.

이 때 $V$ 는 두 전극 사이의 Potential difference를 나타낸다. 

Capacitance 내에서는 전기장이 일정한다. 이는, Capacitance내에서 한 점이 금속들과 먼 거리에 있어도, 각도에 대한 값($sin \theta$)이 커져서 모두 cancel 되어 전기장이 일정하게 된다.

이를 잘 이해하기 위해서는 대칭에 대해서 깊게 생각해야한다.

이를 가우스 법칙에 적용하면 다음으로도 구할 수 있다.
$$
C = \epsilon _0 \frac{A}{d}
$$

- Capacitance가 가지고 있는 에너지는 어떻게 계산할 수 있을까?

  initial 양쪽 금속 charge 0 --> finial 양쪽 금속 charge +Q, -Q 상황을 생각해보자.
  $$
  W = \int dw = \int V dq = \int ^Q  _0\frac{q}{C}dq = \frac{Q^2}{2C} = \frac{1}{2}CV^2 
  $$
  

#### Dielectric Constant

유전상수란 Free Charge에 의해 Induced 되는 Charge 정도를 말한다. 

유전상수는 Capacitor를 생각하는 것이 좋다.
$$
E_{total} = E_{free} + E_{induced} = \frac{Q_{free}}{\epsilon _0} - \frac{Q_{induced}}{\epsilon _0} = \frac{Q_{free}}{\epsilon_0}- l \cdot\frac{Q_{free}}{\epsilon_0} =(1-l)\frac{Q_{free}}{\epsilon _0} = \frac{Q_{free}}{ \bold{K} \cdot \epsilon _0}
$$
따라서, Dielectric Constant 정의는 다음과 같다.
$$
\vec{E} = \frac{\vec{E}_{free}}{\bold{K}}
$$
진공은 1, glass는 5, water는 80, 금속은 거의 무한대에 가깝다. 
