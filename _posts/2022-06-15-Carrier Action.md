---
layout: single
title: "4)Carrier Action"
typora-root-url: ../
categories : "Fundamental-of-Semicondutor"
tag : carrier
#tag : [me, me2, me3]
toc : true
toc_sticky : true
author_profile : false
---
## Fundamental of semiconductor

수학적으로 정의되는 Carrier Action의 대한 방정식은 흔히 Continuity Equation으로 구성된다.

Continuity Equationd으로 표현하기 위해 여러 개념들을 이 단원에서 배우고 정의하려고 한다. 

주의해야할 점은 Carrier Action은 Thermal non-Equilibrium 상황에서 Thermal Equilibrium 상황을 만들기 위해 Carrier가 이동하는 현상을 의미한다.

equilitbrium 상황에서 전자들은 빛의 속드의 1/1000으로 움직이지만 Macroscopic 관점에서 보면 zero로 나타낸다. 따라서 우리는 Carrier를 하나의 개개인으로 보는 것이 아닌 Macroscopic 관점에서 볼 것이다.

---

#### Drift Current 

Drift Current의 개념을 배우기 전에 Current의 개념을 배워야한다. 

반도체에서 말하는 Current는 Volume Current Density를 의미한다. 

이는 다음으로 표시 된다. 
$$
J(Volume ~Current ~Density)=\frac{Current의 개념}{Volume}=\sum_i\frac{q_i\times v_i}{V}
$$
<img src="/images/2022-06-15-Carrier Action/image-20230829095402323.png" alt="image-20230829095402323" style="zoom:120%;" />

이를 머릿속으로 정성적으로 그림을 그릴 때는 임의의 부피 안에 charge에 대한 v벡터를 그려줄 수 있다.

이러한 개념으로 Current(I)는 정성적으로 임의의 부피를 면적에 대한 적분으로 생각 할 수 있다.

따라서 다음으로 표시 된다.
$$
I(Current) = \int J\cdot dA
$$

* 1. 조금 더 생각해보기

  J를 수열의 합의 개념이 아닌 parameter 값으로 정의 내리기 위해서는 어떻게 해야 할까?



​		전자는 Wavepacket으로 Group Velocity로 표현되는데 이의 평균의 개념으로 따라서 생각할 수 있다. 따라서 다음과 같이 표현된다.
$$
J(Volume Current Denisty) = (charge density)\times (average~of~Group ~velocity)=\rho \cdot v_{avg}
$$

* 2. 조금 더 생각해보기 

     Flux의 개념에 대해서 생각해볼 수 있다. 
     $$
     J(Volume ~number~ Density) = F(flux) = \sum_i\frac{v_i}{V}
     $$
     따라서, Flux란 Volume number density의 의미를 갖고 있는 것을 생각할 수 있다.





위의 개념으로 종합하면 다음으로 정리 된다. 
$$
J_{p\mid drift}=(charge ~density)\cdot(average~of~group~ velocity) = qpv_{avg}
$$

$$
J_{n\mid drift}=(charge ~density)\cdot(average~of~group~ velocity) = -qnv_{avg}
$$

보통 전자의 속도는 얼마나 될까? v = 10^6m/s = 1000km/s

전자의 속도는  아주 큰 전압 미만(1000V)에서는 전기장에 비례한다. 

따라서 다음으로 정리된다. 
$$
J_{p\mid drift}=qp\mu_pE
$$

$$
J_{n\mid drift}=qn\mu_n E
$$

이제 mobility의 개념에 대해서 살펴보자.
$$
\mu = mobility
$$
Mobility는 전기장과 속도에 대한 비례상수이다. Mobility는 어떻게 결정되어지는 걸까?

이를 정성적으로 생각하면 다음과  같다.

1. Ionized Impurity에 의해 영향을 받음.
2. Phonon(lattice vibration)에 의해 영향을 받음.

이제 정량적으로 생각해볼 시간이다.

mobility의 입장에서 충돌하기 까지의 평균 시간을 mean free time이라 한다. 

이는 다음으로서 표현할 수 있다. 

