---
layout: single
title: "Sub)Statistical Mechanics in Semiconductor"
typora-root-url: ../
categories : "Fundamental-of-Semicondutor"
tag : MOSFET
#tag : [me, me2, me3]
toc : true
toc_sticky : true
author_profile : false
---
## Fundamental of semiconductor 

> we are interested only in the statistical **behavior of the group** as a whole rather than in the behavior of each individual particle.
> **the electrical characteristics** will be determined by the  statistical behavior of a large number of electrons. 

--> electron or hole의 움직임을 나타낼 때 어떤 통계학적 분포로 나타내야할까?



> There are three distribution laws determining the distribution of  particles among available energy states. 
>
> 1. Maxwell-Boltzman probability function
> 2. Fermi-Dirac probability function
> 3. Bose-Einstein function


#### 1. Maxwell-Boltzman distribution

<img src="https://upload.wikimedia.org/wikipedia/commons/3/37/MaxwellBoltzmann.gif" alt="img" />

Maxwell-Boltzman distribution은 구별가능한 입자에 대해 성립하는 분포이다.

대표적인 예로, 기체분자의 속도가 다음의 형태를 갖는다.

<img src="/images/Statistical mechanics in Semiconductor physics/image-20240418094820439.png" alt="image-20240418094820439" />

들어갈 수 있는 자리가 3개, 입자가 2개일 때, 3^2의 경우의 수를 갖는다. 이러한 규칙으로 다음의 최종 식을 얻을 수 있다.
$$
\text{Maxwell-Boltzman distribution} = f_{MB} \propto e^{-\frac{E}{k_B T}}
$$


일상생활이나 Macroscopic 관점에서 관찰할 수 있는 현상들에 대해 나타낼 수 있는 대표적인 통계분포이다. 이를 반도체에 적용할 수 있을까?

내 대답은 No다. 반도체는 Microscopic 관점에서 관찰해야 한다. 







#### 2. Fermi-Dirac distribution

<img src="https://mblogthumb-phinf.pstatic.net/MjAyMDA4MjVfMjU2/MDAxNTk4MzUxNzAxNzcx.uNVtdsYhr2SdlznxkIdhwlWtLHEkjZbWi6QTR7v6oRYg.4N0b3SaLyJ7TRma16MKDRhn3S1Cx6NrLGquZ-EKXI8Ug.PNG.leeneer/image.png?type=w800" alt="img" />

Fermi-Dirac distribution과 Bose-Einstein distribution은  공통적으로 구별 불가능한 입자를 가진 것에 대한 분포를 나타낸다.

Fermi-Dirac distribution은 각 에너지 별로 (스핀을 제외하고) 하나의 입자만 존재가능하다. : Fermion

Bose-Einstein distribution은 각 에너지 별로 여러 입자가 존재 가능하다. : Boson

<img src="/images/Statistical mechanics in Semiconductor physics/image-20240418095611431.png" alt="image-20240418095611431" />

에너지가 3이고 입자가 2개일 때, 3X2/2! 의 형태를 갖는다. 이러한 규칙으로 다음의 최종 식을 나타낼 수 있다.
$$
\text{Fermi-Dirac distribution} = f_{FD} \propto \frac{1}{e^{\frac{(E-E_F)}{K_B T}}+1}
$$


#### 3. Bose-Einstein distribution

Bose-Einstein distribution은 각 에너지 별로 여러 입자가 존재가능한 상황에 대해 나타낸다. ex_ photon

<img src="/images/Statistical mechanics in Semiconductor physics/image-20240418100139796.png" alt="image-20240418100139796" />

에너지가 3이고, 입자가 2개일 때, 3+2+1의 형태를 갖는다. 이러한 규칙으로 다음의 최종 식을 나타낼 수 있다.
$$
\text{Bose-Einstein distribution} = f_{BE} = \frac{1}{Be^{\frac{E}{k_B T}}-1}
$$
