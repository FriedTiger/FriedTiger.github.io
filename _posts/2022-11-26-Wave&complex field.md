---
layout: single
title: "8-2)Wave & Complex Field"
typora-root-url: ../
categories : "Electromagnetic"
tag : electrodynamics
#tag : [me, me2, me3]
toc : true
toc_sticky : true
author_profile : false
---
## Electromagnetic 

#### Angular Velocity & Velocity

<img src="/images/figure/131983d99261e01e6599bd8b93b002fcaa80eb21.jpg" alt="131983d99261e01e6599bd8b93b002fcaa80eb21" style="zoom:50%;" />

다음 그림에 대해 잘 생각해보자.

자동차가 앞으로 얼만틈 빠르게 가는지는 자동차 회전축의 속도와 반지름에 의해 결정된다.
$$
\vec{v} = \vec{w} \times \vec{r}
\\
\text{ 각 진동수 }w\text{는 바퀴의 축 방향을 가르킴}
$$
v는 자동차가 얼만큼 앞으로 빠르게 가는지를 나타내는 것이다.

즉, 위에 관한 모든 것은 particle에 관련된 식들이다.

이를 대조하여 wave는 어떻게 생각해야할지 탐구해보자.

---

#### 일과 운동에너지

상상 : 마찰력이 있거나 없는 미끄럼틀을 타고 내려오는 아이를 상상해보자.

1. Work - Energy Theorem

   물체에 알짜힘이 한 일은 물체의 운동에너지 변화량과 같다.
   $$
   \begin{align}
   \\
   W_{\text{net force}} = \triangle E_K
   \end{align}
   $$

2. Work(Conservative force) - Energy(Potential) Theorem

​	물체에 보존력이 한 일은 물체의 위치에너지 변화량과 같다. (경로와 무관)
$$
W_{\text{Conservative force}} = - \triangle E_P
$$


​	예시) 중력, 용수철의 탄성력, 전자기력

3. Work(Non-Conservative force) - Energy Theorem

​	비보존력이 한 일이 존재하면, 역학적 에너지 보존법칙(위치에너지+ 운동에너지)가 성립하지 않는다.
$$
W_{\text{Non-Conservative force}} = \triangle E_K + \triangle E_P
$$
​	비보존력은 무질서도 때문에 발생하고, 이는 열로서 방출된다.

​	예시) 마찰력



---

#### Wave

wave : disturbance of a continuous medium that porpagates with a fixed shape at constant velocity.

<img src="/images/figure/image-20230625142508940.png" alt="image-20230625142508940" style="zoom:67%;" />

1. 함수 f(z,t)에 관해서 시간 t에 대한 평행이동 함수는 공간에서 vt만큼 평행이동한 함수와 같다. 

$$
f(z,t) = f(z-vt,0)
$$

따라서. **공간과 시간에 대한 변수를 하나로 표현할 수 있는(공간과 시간이 어떠한 관계이 있음.) 함수를 Wave**라고 한다.

Wave는 시간에 대해서 두번 미분한 것과 공간에 대해서 두번 미분한 것의 비례관계로 나타낸다.
$$
\begin{align}
\\
&\frac{\partial ^2 f}{\partial ^2 z } : \text{x 근처에서 얼마나 빨리 변하느냐}
\\
&\frac{\partial ^2 f}{\partial ^2 t} : \text{시간 t 에서 얼마나 빨리 가속되느냐.}
\end{align}
$$


2. wave는 방정식적으로 다음을 만족시킨다.

$$
\frac{\partial ^2 f}{\partial z^2} = \frac{1}{v^2}\frac{\partial^2 f}{\partial t^2}
\\
:\text{공간에 대한 두번 미분과 시간에 대한 두번 미분은 비례한다.}
$$

위의 성질을 통하여 Sinusoidal wave를 만들 수 있다.
$$
f(z,t) = A cos [ k(z-vt)+\delta]
\\
\delta : \text{phase constant}
\\
\\
\text{wavelength : 시간 고정에서 공간에서 phase를 일치시킬 최소 길이}
\\
\lambda = \frac{2 \pi}{k} (\text{k는 wave number})
\\
\text{period : 공간 고정에서 시간에서 phase를 일치시킬 최소 시간}
\\
T = \frac{2 \pi}{kv} 
\\
* \text{frequency} ~~f = \frac{1}{T}
\\
** \text{angular frequency}~~ \omega = 2 \pi f = kv
\\
\\
\\
\therefore f(z,t) = Acos[kz-wt + \delta]
\\
\lambda = \frac{2\pi}{k}
\\
T = \frac{2 \pi}{\omega}
$$

고민을 많이 해봤지만.. 

Wavevector를 운동량의 개념으로 설명하는 것이 제일 좋은 것 같다.

---

#### Propagating wave & Standing wave

진행파 : 시간에 따라 진폭의 크기가 바뀌는 파동.

정상파 : 시간에 따라 진폭의 크기가 변화하지 않는 파동.



만약, 포인팅 벡터로 시간당 평균에너지를 계산하면, 

진행파는 에너지가 존재하고 정상파는 에너지가 0을 나타낼 것이다.

---

#### Complex Field

1.  #### Harmonic oscillator

   Harmonic oscillator에서 $\omega$ 의 힘을 가하면 **steady-state**에서 $\omega$ 로 진동한다.

따라서, linear한 maxwell equation을 적용할 수 있다. 

이를 그림에서 살펴보자.

<img src="/images/figure/image-20230625150423394.png" alt="image-20230625150423394" />

전자기파의 관측자 A,B위치가 정해져있고 각 관측자가 전지기파를 볼 때 $\omega$는 모두 같다.

따라서, 전자기파를  서술할 때 **시간term은 모두 공통적으로 적용**되므로 전기장 세기 및 $\delta$ 를 위치에 대한 변수와 함께 적어주면 된다.

따라서 앞으로 다음과 같이 표시하자
$$
\text{상황 : Simple harmonic oscillator가 sinusoidal driving force에 있을 때}
\\
\begin{align}
X_{SS}(t) = X_0~cos(\omega t + \delta) &= Real(X_0 ~ e^{-i(\omega t + \delta )})
\\
&= Real( \color{red} {X_o e^{-i\omega t}} \color{black}e^{-i \delta})
\\
&= Real(\color{red}{\widetilde{X}}\color{black}{e^{-i\omega t})}
\end{align}
$$

미분에서의 상황도 알아보자.
$$
\dot{X_{SS}(t)} = Real(\color{red}{-i\omega \widetilde{X}}\color{black}{e^{-i\omega t})}
\\
\ddot{X_{SS}(t)} = Real(\color{red}{(-i\omega)^2 \widetilde{X}}\color{black}{e^{-i\omega t})}
$$


위 식에서 Phasor는 공간에 대한 정보를 담고 있지 않다.

그렇다면 Phasor는 공간에 대한 정보를 담고 있을 수 있을까?

#### 2. 공간에 대한Phasor

Phasor는 위의 정리에 따라 같은 wave가 같은 $\omega$를 가지기 때문에 시간 term을 제외한 개념이다.

전자는 워낙 가볍기 때문에 외부 frequency인 $\omega$ 에 대응되어 움직일 것이다.

Phasor 변수에 공간변수가 할당되어 있다면 Phasor는 공간에 대한 phasor의 의미를 갖는다.
$$
\begin{align}
f(z) &= A~cos(kz-\omega t + \delta)
\\
f(z) &= Real(Ae^{ikz}e^{i\delta}e^{- i\omega t})
\\
f(z) &= Real(\color{red}Ae^{ikz}e^{i\delta}\color{black}e^{- i\omega t})
\\
f(z) &= Real(\color{red}{\widetilde{f(z)}}\color{black}e^{-i\omega t} )
\\
\color{red}{\widetilde{f(z)}}\color{black} &\text{를 Complex Field(복소 필드)라 한다.}
\\
\end{align}
$$



---

<img src="/images/figure/Wave_group.gif" alt="Wave_group" />

**Phase velocity(빨간색 점)**  :  phase에 대한 속도를 나타낸다.

사고실험으로 빛의 속도로 움직이는 TEM 전자기파를 생각해보자.

<img src="/images/figure/image-20230223171444706.png" alt="image-20230223171444706" style="zoom:50%;" />

$\psi = A \cdot cos(kx -wt)$ 를 나타내므로 한 점에 대해서 시간에 따라 조사하면, $\psi$ 는 y축(E축)에 대해서는 같은 값을 가지고 x축에 대해서는 시간에 따라 같은 값을 가질 것이다. 

이를 수식적으로 해석해보자.
$$
\psi = A \cdot cos(k(x-\frac{w}{k}t))
$$
이렇게 표현할 수가 있다. 

따라서 
$$
v = \frac{w}{k}
$$
임을 알 수 있다. 이는, 주파수에 대해 $\vert \vec{k} \vert $ (wavevector)로 나타낸 값이다. 
$$
p = \hbar k ~~\text{De Broglie equation}
$$
$\vert \vec{k} \vert$ 는 운동량에 관한 값으로 생각하는 것이 좋다. 

즉. 전자기파의 속도는 k방향으로 k의 크기로 움직이는 크기와 w의 t진동에 따른 시간 term으로 나타낸다.



**Group velocity(연두색 점)**  :

파동의 superposition으로 생기는 envelope는 k 방향에 따라서 한 점의 phase가 계속 바뀌기 때문에 phase velocity로 나타내기 힘들다. 따라서 새로운 개념인 Group Velocity 개념이 도입되었다. 

이를 **Wave Packet** 이라 한다.

파동의 superposition은 carrier와 같은 반도체에서 자주 일어남으로 반도체소자해서 자주 사용되는 개념이다.

이를 더 자세하게 살펴보면 다음과 같다.
$$
\psi_1 = A \cdot cos(k_1x-w_1t), ~\psi_2 = A \cdot cos(k_2 x - w_2 t)
\\
\text{superposition 되면 다음과 같다.}
\\
\psi = 2A \cdot cos(\frac{(k_2 - k_1)t - (w_2 - w_1)t}{2})cos(\frac{(k_2 + k_1)t+(w_2+w_1)t}{2})
$$
이를 해석하면 다음과 같다. 두개의 함수가 곱해져 있는 모양을 갖는다.

앞쪽 함수는 
$$
v_f = \frac{w_2 - w_1}{k_2 - k_1}
$$
뒤쪽 함수는
$$
v_b = \frac{k_2 + k_1}{w_2 + w_1}
$$
를 갖는다.

$v_f$ 가 $v_b$ 보다 더 작은 w와 k값의 형태를 갖는다. 따라서,

**WavePacket** 속에서 앞쪽 함수는 **Envelope wave**(Group velocity) 의 대한 속도를 나타내고 뒤쪽 함수는 **Carrier wave**(phase velocity) 에 대한 속도를 나타낸다. 

이를 그림으로 표현하면 다음과 같다.

<img src="/images/figure/Wave_opposite-group-phase-velocity.gif" alt="Wave_opposite-group-phase-velocity" />

다음처럼 Group velocity와 phase velocity는 다른 방향을 가질 수 있다.

---



#### Electromagnetic Wave

전자기파는 전기장과 자기장의 수직을 통해 앞으로 나아가는 wave이다.

Ampere's Law에 따른
$$
\triangledown \times B = \mu_0(I + \epsilon_0 \frac{dE}{dt})
\\
\text{전류가 없는 상황이므로}
\\
\triangledown \times B = \mu_0 \epsilon_0 \frac{dE}{dt}
$$
식으로 설명할 수 있다.

이를 통해 계산하면 다음을 알 수 있다.
$$
B_0 = \frac{E_0}{c}
$$

$$
c = \frac{1}{\sqrt{\epsilon _0\mu_0}}
$$

$$
n = \frac{1}{\sqrt{\mu_r \epsilon _r}}
$$

---


#### Oscillating Charges

전자기파가 빛을 내기위해서는 charge가 oscillate를 함으로써 빛을 낼 수 있다.

<video src="/images/figure/ExhaustedAlarmedDeinonychus-mobile.mp4"></video>

charge가 oscillate를 함으로써 $\frac{dE}{dt}$ 의 변화가 생기고 이를 통해 Ampere's law에 따라 전자기파가 생긴다. 

따라서, 만약 y축으로 oscillate하는 charge가 있다먼 이는 y축에 따라 진행하는 빛을 방출하지 않으며 

oscillating charge를 바라보는 양 x 축 끝에서,  $E_y (polarization)$ 를 관측할 수 있다.

---

#### Poynting Vector

Poynting Vector란 $1m^2$ 의 면적에 시간당 빛이 얼마만큼 에너지를 주는지를 나타내기 위해 만든 개념이다.

<img src="/images/figure/image-20230223181241197.png" alt="image-20230223181241197" style="zoom:67%;" />
$$
S = \frac{\vec{E} \times \vec{B}}{\mu_0}
$$
로 나타낸다. 

만약 시간에 따라 다르게 나타난다면 이는 다음과 같이 구할 수 있다.
$$
<S> = \frac{1}{2}\frac{\vec{E} \times \vec{B}}{\mu_0}
$$

---

#### Convolution의 의미 

impulse response에 대해 convolution으로 곱해야 한다.

---

#### 운동량의 의미

운동량을 생각할 때 힘과 운동량에 대해 생각하지 말고 에너지와 운동량에 대해 생각하자.

**운동량은 에너지의 최소 단위로 나타내는 것이다**

전자기파에서 에너지를 wave vector, 진폭 크기를 고려하여 $\vec{S} = \vec{E} \times \vec{H}$ 라하는데 

이때, 평균에너지를 구할 수 있다.

이러한 평균에너지의 가장 작은 단위가 Poynting vector이기 떄문에 (에너지의 단위 시간 및 단위 공간)

Poynting  vector를 Energy에 대한 momentum이라고 생각하는게 좋을 것 같다.

이와 비슷한 생각 :

고전역학 - Particle 운동E에 대한 운동량

전자기학 - Wave 평균 E에 대한 운동량

반도체소자 - charge에 대한 flux ($\triangledown \cdot \vec{J} = \frac{\partial q}{\partial t}$)
