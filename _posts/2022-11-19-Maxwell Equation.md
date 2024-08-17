---
layout: single
title: "7)Maxwell equation"
typora-root-url: ../
categories : "Electromagnetic"
tag : electrodynamics
#tag : [me, me2, me3]
toc : true
toc_sticky : true
author_profile : false
---
## Electromagnetic 

#### Maxwell Equation

$$
\begin{align}
\triangledown \cdot E &= \frac{\rho}{\epsilon_0}
\\
\triangledown \times E &= - \frac{\partial B}{\partial t}
\\
\triangledown \cdot B &= 0
\\
\triangledown \times B &= \mu_0J+\mu_0\epsilon_0\frac{\partial E}{\partial t}
\\
\end{align}
$$

위 식이 진실된 Maxwell Equation이다.

만약, Macroscopic 한 관점에서 volume density의 개념을 도입하여 $\vec{P}$ , $\vec{M}$ 을 생각하여 물질 내에서의 방정식을 만들 수 있다.

물질 내에서 전류 J는$J_P = \frac{\partial P}{\partial t}$ 의 영향을 받으므로 다음과 같이 표현할 수 있다. --> H에 의미가 포함되어 있음.
$$
\triangledown \cdot D = \rho _f
\\
\triangledown \times E = - \frac{\partial B}{\partial t}
\\
\triangledown \cdot B = 0
\\
\triangledown \times H = \mu J_f + \frac{\partial D}{\partial t}
$$

#### Boundary condition

$$
\begin{align}
D^\perp_1 - D^\perp_2 &= \sigma_f
\\
E^\parallel_1 - E^\parallel_2 &= 0
\\
B^\perp_1 - B^\perp_2 &= 0
\\
H^\parallel_1 - H^\parallel_2 &= \text{K}_f \times \hat{\eta}
\end{align}
$$



## Conservation Law

**에너지를 항상 위치에너지 + 운동에너지로 생각하자 **

**'일을 한다는 것'은 운동에너지에 변화에 관련된 이야기이다. **

**전자기학에서 위치 에너지를 구하기 위해서는 all space에 해당하는 전기장과 자기장의 에너지를 모두 적분하면 된다.** 

1. Charge Conservation

<img src="/images/figure/image-20230625121952480.png" alt="image-20230625121952480" style="zoom:67%;" />
$$
\text{어떠한 domain에 charge가 들어오면 charge들은 모두 보존된다.}
\\
\frac{dQ}{dt} = -\oint \vec{J} \cdot d\vec{a}
\\
\text{이를 다시 쓰면 다음과 같다.}
\\
\frac{\partial \rho}{\partial t} = - \triangledown \cdot \vec{J}
$$

2. Energy Conservation

<img src="/images/figure/image-20230625122344661.png" alt="image-20230625122344661" style="zoom:80%;" />
$$
\text{total energy stored in electromagnetic fields, per unit volume는 다음과 같다.}
\\
u = \frac{1}{2}(\epsilon_0E^2 + \frac{1}{\mu_0}B^2)
\\
\\
\text{Lorentz Force에서 일과 위치에너지에 관한 식은 다음과 같다.}
\\
F\cdot dl = q(\vec{E}+\vec{v}\times \vec{B})\cdot \vec{v}dt = q\vec{E}\cdot\vec{v}dt
\\
\therefore \frac{dW}{dt} = \int_V (\vec{E}\cdot \vec{J})d\tau
\\
\\
\text{이를 에너지 보존법칙에 관해 정리하면 다음과 같다.}
\\
\frac{dW}{dt}+\frac{d}{dt}\int_V \frac{1}{2}(\epsilon_0 E^2 + \frac{1}{\mu_0}B^2)d\tau =-\frac{1}{\mu_0}\oint _S(\vec{E}\times \vec{B})\cdot d\vec{a}
\\
\text{내 생각: 어차피 시간에 따른 변화율을 구하는 것이므로  all space에 대한 전기장 및 자기장을 적분할 필요가 없다.}
$$
좌식은 운동에너지 변화량 + 위치에너지 변화량을 뜻하고, 우식은 에너지의 들어온 흐름을 이야기한다. 

우식을 Poynting theorem이라 정의한다. 
$$
\bold{\text{Poynting vector}} : \text{Energy Flux Desnity : energy per unit time, per unit area}
\\
S \equiv \frac{1}{\mu_0}(\vec{E}\times \vec{B})
$$
(11)식을 compact하게 쓰면 다음과 같다.
$$
\frac{dW}{dt} +\frac{d}{dt}\int_V u ~d\tau = - \oint_S \vec{S}\cdot d\vec{a}
\\
\text{만약 charge 없는 domain이라면, 일을 하지 않으므로}
\\
\frac{d}{dt}\int_V u~d\tau = - \int(\triangledown \cdot \vec{S})d\tau
\\
\therefore \frac{\partial u}{\partial t} = - \triangledown \cdot \vec{S}
$$




| name                  | equation                 | source                                                       |
| --------------------- | ------------------------ | ------------------------------------------------------------ |
| Gaussian's law        | $\triangledown \cdot E$  | $\frac{\rho}{K\epsilon_0 }$                                  |
| Faraday's law         | $\triangledown \times E$ | $-\frac{\partial B}{\partial t}$                             |
| Gaussian's law        | $\triangledown \cdot B$  | 0                                                            |
| Amperer & Maxwell law | $\triangledown \times B$ | $K_{\text{magnetic}}~\mu_0( I + K\epsilon _0 \frac{\partial E}{\partial t})$ |

* 전류라는 개념을 다르게 생각하면 움직이는 charge로 생각할 수 있다. 

  움직이는 charge는 $\frac{\partial E}{\partial t}$ 로 생각할 수 있다. 

  따라서, 전류도 $\frac{\partial E}{\partial t}$의 개념으로 생각할 수 있다.
  
* 문제 푸는 법 :

  1) symmetric loop or surface or volume를 만들자. ex) loop or surface에 대해 모두 같은 E or B를 갖도록 만들어줘야한다.
  2) 위에 symmetric 안에 존재하는 source들을 한번에 나타내면 된다. 
  3) Divergence에 대해서는 공간에 대해 적분을 하고, curl에 대해서는 open surface에 대해 적분해야 된다.

---

#### Susceptibilty, dieletric constant, ..., permittivity, permeability

|          | kappa : relative permittivity(dielectric constant), relative permeability | Susceptibility      | 서로의 관계                | Polarization(Input : P, M) | 서로의 관계    |
| -------- | ------------------------------------------------------------ | ------------------- | -------------------------- | -------------------------- | -------------- |
| Eletric  | $\text{K}$ , $\epsilon _ r$ , $\frac{\epsilon}{\epsilon _0}$ (단위 x) | $\chi$  (단위 x )   | $\epsilon _ r = 1 + \chi $ | $P = \chi \epsilon _0 E $  | $D=\epsilon E$ |
| Magnetic | $\text{K}_{magnetic}, \mu_r, \frac{\mu}{\mu_0}$ (단위 x)     | $\chi _M$  (단위 x) | $\mu_r = 1 + \chi_M$       | $M = \chi_M \mu_0 H$       | $B = \mu H$    |

**반드시 주의 맟 알아야 할 것 : 1) E, B 모두 내부의 전기장 자기장을 의미한다. 2) 외부의 전기장과 내부의 전기장, 외부의 자기장과 내부의 자기장 모두 coupling 되어 있다. 따라서 간단히 생각해서는 안된다.** 



1) **전기장 E** 

   전기장이란 한 점에서 1Q의 전하가 받는 힘을 나타낸다. 

   즉, 물질 안에 있다면 물질 내에서의 한 점에서의 1Q의 전하가 받는 힘($F_{total}$}을 나타낸다. 
   $$
   D = \epsilon _0 E + P
   \\
   \epsilon_0 E = D - P \text{로 생각하는 것이 편하다.}
   $$
   이를 해석하면 다음 과 같다. 

   <img src="/images/figure/image-20230219013514362.png" alt="image-20230219013514362" style="zoom:150%;" />

   상황 1) D가 고정

   $\text{K}$ 가 커지면 E는 감소한다. 즉, 물질 내에서 P가 커지므로 전기장 E는 감소한다. 

   상황 2)  E가 고정

   $\text{K}$가 커지면 금속에 전하들이 더 몰려온다. 즉, D도 커지고 P도 커진다. 



2. **자기장 B**

   자기장이란 Magnetic flux density로 원형 고리에 흐르는 전류에 의해 생기는 Magnetic의 flux density를 의미한다. 

   자기장도 전기장과 마찬가지로 물질 내에서의 총 자기력에 의한 것(total)을 의미한다.
   $$
   B = \mu_0 H + M
   \\
   \frac{B}{\mu _0} = H +\frac{M}{\mu_0}\text{로 생각하는 것이 편하다.}
   $$
   

<img src="/images/figure/image-20230219020025612.png" alt="image-20230219020025612" style="zoom:75%;" />



상황 1) H가 고정

$\mu_r$ 이 커지면, B가 커진다. 즉, 물질 내에서 M이 커지므로 자기장 B는 커진다.

자기장과는 약간 다르게 상당히 coupling 되어있는 상황이다. 따라서 전체적으로  생각하기가 까다롭다.

---

#### Green function

$$
\begin{align}
&\triangledown ^2 V = - \frac{\rho}{\epsilon}
\\
&V(r) = \frac{q}{4 \pi \epsilon \vert \bold{r} - \bold{r'} \vert} 
\\
\\
&\text{이를 point charge에 대해 서술하면 다음과 같다.}
\\
&\triangledown ^2 g(\bold{r} -\bold{r}^{'}) = - \delta (\bold{r} -\bold{r}^{'})
\\
&g(\bold{r}- \bold{r}^{'}) = \frac{1}{4 \pi \vert \delta - \delta ^ {'} \vert }
\\
\\
&\text{Point source에 대한 inpulse는 다음처럼 생각할 수 있다.}
\\
&J(r) = \int _V d\vec{r}^{'} \delta (r- r')J(r') 
\\
\\
&\therefore \text{일반적인 Gauss's law와 Green function을 결합하고 linear combination으로 나타내면 다음과 같다.}
\\
&\triangledown^2 V(\bold{r}) = - \frac{1}{\epsilon} \int_V dV' \delta(\bold{r}- \bold{r'})J(\bold{r'})
\\
&V(\bold{r}) = \frac{1}{4 \pi\epsilon} \int_V  \frac{J(\bold{r'})}{\vert \bold{r} - \bold{r'} \vert}dV'
\\
\\
&\text{결론 : }
\\
&J(r) = \int _V d\vec{r}^{'} \delta (r- r')J(r') 
\\
&\text{이 가정을 통해 모든 식을 도출하였다. 즉, 임의의 소스에 대해 가우스법칙을 구할 때, point source response(Green function을 활용한 convolution)를 활용하자.}
\end{align}
$$

Green function을 찾는 것이 중요하다.

Weng Cho CHEW, Purdue Univ 왈 

"Once you know the green function of the system is like(=) you know the point source response of the impulse response of the system"
