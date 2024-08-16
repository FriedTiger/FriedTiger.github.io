---
layout: single
title: "2-2)Concpept of Carrier"
typora-root-url: ../
categories : "Fundamental-of-Semicondutor"
tag : carrier
#tag : [me, me2, me3]
toc : true
toc_sticky : true
author_profile : false
---

## Fundamental of semiconductor

  가장 큰 목표는 Carrier의 농도와 분포를 아는 것이다! 

이를 위해서는 여러 개념들이 필요하다.

---

#### Density of States

**Density of States** : State 수 / 에너지 를 나타낸다.

<img src="/images/2-2. Concept of Carrier/image-20221021171405072.png" alt="image-20221021171405072" style="zoom:50%;" />

root안을 잘 살펴보면, 

* conduction band의 경우 Ec보다 클 때 Root(E)에 비례함을 알 수 있다.
* Valence band의 경우 En보다 작을 때, Root(E)에 비례함을 알 수 있다.



---

#### Fermi Energy

Fermi function f(E) : Electrons 수 / State 를 나타낸다.

Fermi Energy는 T가 절대영도에 가까워질 때, fermi function의 sharp cutoff가 일어나는 E이다.

<img src="/images/2-2. Concept of Carrier/image-20221021172255759.png" alt="image-20221021172255759" style="zoom:67%;" />

이를 그래프로 살펴보면 다음과 같다.

<img src="/images/2-2. Concept of Carrier/image-20221021172325705.png" alt="image-20221021172325705" style="zoom:67%;" />

Fermi Energy의 개념을 도입함으로써 Carrier의 농도와 분포를 기술하는 것이 무척 편해졌다.

따라서, Fermi Energy가 해석을 하는데 있어서 가장 중요하다.

---

#### Carrier의 농도 계산하기

$$
n = \int^{\infty}_{E_c} g_c(E)f(E)dE
$$

Density of State 식과 Fermi function 식을 대입하면 다음과 같다.
$$
n = \frac{m_n^* \sqrt{2m_n^*}}{\pi^2 \hbar^3} \int^{\infty}_{E_c} \frac{\sqrt{E - E_c} dE}{1 + e^{\frac{E-E_F}{kT}}} ----(1)
$$
이를 적분하기 위해서는 반드시 scaling을 해주어야 한다. (numerical calculation을 위해서는 scaling이 필수)
$$
\eta = \frac{E-E_c}{kT}
$$


계산결과 다음과 같다.
$$
n = \frac{m_n^*\sqrt{2m^*_n}(kT)^\frac{3}{2}}{\pi^2 \hbar^3} \int^{\infty}_{0}\frac{\eta^{\frac{1}{2}}d\eta}{1+ e^{\eta-\eta_c}}
$$
이 복잡한 식을 어떻게 간단하게 나타낼 수 있을까?

* 먼저 적분 앞의 값은 상태에 대한 식이므로 Constant로 나타낼 수 있다.
  $$
  N_c = 2[\frac{m_n^*kT}{2\pi\hbar^2}]^\frac{3}{2}
  $$

* 뒤의 적분식은 "Fermi dirac integral of order 1/2"로 표현가능하다.
  $$
  F_{1/2}(\eta_c)=\cong\int^{\infty}_{0}\frac{\eta^{1/2}d\eta}{1+e^{\eta-\eta_c}}
  $$
  

따라서, 정리하면 다음과 같다.
$$
\mathbf{n = N_c \frac{2}{\sqrt{\pi}} F_{1/2} (\eta_c)}
$$
이를 계산하는 것은 numerical calculation만 가능하다. 

따라서, approximation을 하게 되는데, 

(1)식에서 E-EF>> 3kT 이면 20>>1 의 형태가 되어 분모의 1을 지울 수 있다. --> **Boltzman distribution**

즉, 조금 더 생각해보면 Boltzman distribution 을 적용할 수 있는 상황은 다음과 같다.

* **non-dengeneracy 상황**
* Eg이 3kT보다 큰 상황에서 기술 할 수 있다. 

이는 다음으로 표현된다. 
$$
F_{1/2}(\eta_c) = \frac{\sqrt{\pi}}{2} e ^{\frac{(E_F - E_c)}{kT}}
$$
따라서, 이를 정리하면 다음과같다.
$$
\mathbf{n = N_c e^\frac{{(E_F - E_c)}}{kT}}
$$

<img src="/images/2-2. Concept of Carrier/image-20221021175209698.png" alt="image-20221021175209698" style="zoom:80%;" />

---

이를 통해 해석해보는 시간을 갖자.



1) Doping에 상관 없이 n*p는 일정하다. 즉, 전체의 Carrier의 농도 곱은 온도에 대한 값이다.
   $$
   
   $$
   

$$
n \cdot p = n_i^2=p_i^2
$$

 2. Doped materials이 total ionization 되었을 때 charge neutrality relationship을 만족해야한다.
    $$
    p + N_D^+ = n + N_A^-
    $$
    이를 n에 대해서 서술하면,
    $$
    \frac{n_i^2}{n} + N_D^+ = n + N_A^-
    $$
    
 3. 앞서서 언급했다시피 intrinsic carrier concentration은 의미가 없을 정도로 작았다.

    Non-degeneracy 상황과, Total ionization 상황에서는 다음이 성립한다.

$$
N_D>>n_i 일때
$$

$$
n\approx N_D
$$

4. 온도가 높은 상황에서는 불순물이 있더라도 Intrinsic한 상황이 나타날 수 있다.

   
   $$
   n \approx p \approx n_i
   $$

5.  불순물을 피할 수 없을 때는 compensate한 반대의 dopant를 도핑하여 사용할 수 있다. 
   $$
   N_A = N_D
   $$

   ---

   #### 페르미E 계산하기 (소자 측정시, Simulation시)
   
   페르미E를 계산한다는 것은 전자와 홀의 농도를 구하고 역으로 페르미 E를 계산하는 것을 의미한다.

1) Intrinsic Material

$$
N_c e^{(E_F-E_c)} = N_ve^{(E_v-E_F)}
$$

$$
\frac{N_V}{N_C}=\left({\frac{m_p^*}{m_n^*}}\right)^{3/2}
$$

따라서, 계산하면 다음과 같이 계산할 수 있다.
$$
\mathbf{E_i = \frac{E_c + E_v}{2} + \frac{3}{4}kT ~ln\left(\frac{m_p^*}{m_n^*}\right)}
$$

2. Doped Semiconductor(when N_D>>ni)

$$
\mathbf{E_F - E_i = kT~ln{\left(N_D/n_i\right)}}
$$

이것에 대해 조금 더 살펴볼 필요가 있다.

전자의 농도는 식에 대해서 잘 생각해보면, 온도와 페르미E가 영향을 미칠 수 있다. 

지수함수의 분자승이 페르미 E 이므로, 페르미E가 훨씬 더 영향을 많이 미치는 것을 알 수 있다.

이것은 페르미 E가 조금만 변해도 전자의 농도에 큰 영향을 미치는 것을 알 수 있다 .



반대로 이를 생각해보자

페르미 E는 전자의 농도와 온도에 관해 계산할 수 있다.

페르미 E와 온도는 비례 관계를 갖지만 전자의 농도와는 로그함수 형태를 갖는다.

따라서, 페르미 E는 전자의 농도가 많이 변해도 조금만 변한다.