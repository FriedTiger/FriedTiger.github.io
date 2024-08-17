---
layout: single
title: "6)OLED Evolution"
typora-root-url: ../
categories : "OLED"
tag : [PHOLED, TADF]
#tag : [me, me2, me3]
toc : true
toc_sticky : true
author_profile : false
---
## OLED

#### 1. Fluorescence 

<img src="/images/figure/image-20230529134634369.png" alt="image-20230529134634369" />

전극으로 random한 spin을 갖은 전자가 들어오기 때문에 Singlet : Triplet의 비율이 1 : 3을 갖는다. 따라서 MAX IQE = 25%이다.

Dopant의 Dopping 농도가 낮아야 한다. 이유 : Dopant 농도가 높아지면 Exciton collision으로 인한 TTA가 일어날 확률이 높음.

#### 1-1 Delayed Fluorescence(TTA-F OLED)

<img src="/images/figure/image-20230529135912707.png" alt="image-20230529135912707" style="zoom:80%;" />

TTA Annihilation을 이용하여 Delayed process를 통해 추가로 Singlet Exciton을 얻는다.
$$
\begin{align}
T_1 + T_1 &\rightarrow (\alpha S_n +\beta T_n + \gamma Q_n) + S_0
\\
&\text{이는 다음의 의미를 갖는다.}
\\
\text{Exciton 2개} &\rightarrow \text{Exciton 1개} \rightarrow S_0 
\end{align}
$$
무한 급수를 통하여 이를 계산하면 총 IQE는 다음과 같다.
$$
\begin{align}
&n_{IQE} = 25\% +n_{DF} = 25\% + (75\% \cdot \frac{\alpha}{2}) + (75\% \cdot \frac{\alpha}{2})\cdot \frac{\beta}{2}+ (75\% \cdot \frac{\alpha}{2})\cdot {(\frac{\beta}{2})}^2+\cdot \cdot \cdot
\\
&n_{IQE} = 25\% + \frac{75\% \cdot \alpha}{2 - \beta}
\end{align}
$$
따라서 $\alpha = 1, \beta=0$ 일 때, $n_{IQE max} = 62.5\%$ 이다.

따라서 이론적인 max를 달성하기 위해서 어떻게 물질을 설게해야 할까?

<img src="/images/figure/image-20230529170413151.png" alt="4" />

$\beta = 0$ 이 되게 하는 것이 중요하므로  $2 \times T_1 < T_2$ 이 되도록 설계한다. 이를 만족시키는 Blue host가 바로 ![image-20230529171452228](/images/figure/image-20230529171452228.png) (Anthracence) 이다.

Anthracence (host)와 Pyrene(dopant)를 이용하여 다음의 상황을 만들 수 있다.

<img src="/images/figure/image-20230529172445881.png" alt="image-20230529172445881" />

따라서 Fluorescence와 마찬가지로 Delayed Fluorescence도 Dopant의 doping 농도를 낮추어야 할 것이다.

**Trade off**

<img src="/images/figure/image-20230529173018601.png" alt="image-20230529173018601" /><img src="/images/figure/image-20230529173048326.png" alt="image-20230529173048326" />

전류가 낮은 부분에서 전류가 커질 때 TTA가 dominant 하여 Efficiency가 상승하지만,

전류가 놓은 부분에서 전류가 커질 때 STA가 dominant 하여 Efficiency가 감소한다.

**Triplet을 기준으로 Exciton collision을 생각하는 것이 중요하다.**



#### 1- 2 TADF (Thermally activated delayed fluorescence)

<img src="/images/figure/image-20230530132348792.png" alt="image-20230530132348792" style="zoom:80%;" />

온도적으로 $T_1$ 에서 $S_1$ 으로 up-converted 되는 원리를 이용한다. : Reverse-intersystem Crossing

$\triangle E_{ST}$ 가 최소가 되는 것이 가장 중요하다. 이를 위해서는 LUMO 와 HOMO의 wavefunction이 spatially seperated 되는 것이 중요하다.

<img src="/images/figure/image-20230530132717846.png" alt="image-20230530132717846" /><img src="/images/figure/image-20230530132729873.png" alt="image-20230530132729873" />

그렇다면 Reverse-intersystem Crossing은 어떻게 발생할 수 있는 것일까?
$$
\text{from Nature : Highly efficient organic light-emitting diodes from delayed fluorescene . Adachi group}
\\
\lambda \propto \frac{H_{SO}}{\triangle E_{ST}}
\\
\lambda : \text{the first-order mixing coefficient between singlet and triplet}
$$
이를 조금 더 개념적으로 이해하면 Fermi's Golden Rule의 Born-oppenhierm approximation으로 해석할 수 있을 것 같다. - 내생각
$$
k_{if} = \alpha \langle \psi _f \vert \hat{x} \vert\psi_i \rangle ~\vert \langle\psi_{nf} \vert \psi_{ni} \rangle \vert~ \vert \langle \Phi_f \vert \Phi_i \rangle \vert
$$
따라서, spin에 대해 first-order perturbation이 존재 할 때, electron의 wavefunction이 많이 겹치게 된다면 electron trasition이 가능할 수 있을 것 같다.

TADF는 Donor와 Acceptor가 aromatic bridge로 twisted geometry 상태로 진동하기 때문에 많은 진동을 하게 된다. 따라서, 스펙트럼이 굉장히 넓은 단점이 있다.

<img src="/images/figure/image-20230530145137606.png" alt="image-20230530145137606" style="zoom:80%;" /> 

위 그림에서 오른쪽의 $S_1$ 이 더 넓은 포물선을 그리고 있다. 

이를 해결하기 위해 새로운 컨셉이 등장하였다.

**Boron-based TADF **

TADF의 Donor와 Acceptor가 aromatic bridge 형태로 수직 각도로 진동하여 스펙트럼이 넓어지는 문제점을 해결하기 위해 Donor와 Acceptor를 원자단위로 구분하여 만든 새 연구가 발표되었다.

<img src="/images/figure/image-20230530143416801.png" alt="image-20230530143416801" />

이를 통해 아주 narrow한 spectrum을 얻을 수 있게 되었다. 하지만, 높은 밝기와 긴 수명은 달성하지 못하였다. 이유 : Triplet의 very long lifetime(less efficient R-ISC due to large $\triangle E_{ST} \approx 0.2eV$ ) 

따라서 이또한 해결하기 위해 Boron based TTA-F도 제시되었다.

<img src="/images/figure/image-20230530144704220.png" alt="image-20230530144704220" style="zoom:80%;" />

#### 1-3 Hyper-Fluorescence

<img src="/images/figure/image-20230530142337727.png" alt="image-20230530142337727" />

Spectrum이 넓은 문제를 해결하기 위해 TADF 를 Sensitized(감작, 점진적 자극) 역할로 사용하였다. 이를 통해 rigid한 상태를 만들 수 있다.

$T_{AD} \rightarrow T_D$의 Dexter를 막기 위해 적은 양의 Fluorescent를 doping해야한다.

만약 dopant를 Fluorescent dopant가 아닌 Phosphorescene dopant를 사용한다면 $T_{AD} \rightarrow T_D$ 의 Dexter를 이용하여야한다. 따라서 많은 양을 doping해야한다.



#### 2. Phosphorescence

<img src="/images/figure/image-20230530122644775.png" alt="image-20230530122644775" style="zoom:80%;" />

Host 물질에서 Singlet의 Forster+Intersystem crossing과 Triplet의 Dexter를 통해 Dopant에서의 Triplet이 발광할 수 있도록 Spin orbit coupling 을 이용하여 발광한다.

인광은 Dexter를 이용해야하므로 Doping농도가 높아야 한다.

**SOC(Spin-orbit Coupling)**

selection rule에 의하여 electronic transitions은 $\triangle S = 0$ (total spin 변하량)을 만족시켜야 가능하다. 하지만 다음과 같은 상황에서 spin selection rule이 깨지는 상황이 발생한다.

<img src="/images/figure/image-20230530124836073.png" alt="image-20230530124836073" style="zoom:67%;" />

Heavy Metal이 doping 되면 다음을 생각할 수 있다.

1. 전자가 무거운 원소 주변을 돈다 $\rightarrow$ 무거운 원소가 전자를 돈다. (자기장 의 생성)
2. 전자는 고유의 spin을 가지고 있다.
3. 1과 2에 의한 Coupling이 발생한다. : $\vec{L} \cdot \vec{S} \text{~~coupling}$

따라서, selection rule을 만족시키지 않더라도 electron transition이 가능하게 된다.

다음의 수식들로 나타낼 수 있다.
$$
\triangle H_{SOC} = - \mu \cdot B ~~ : \mu (\text{magnetic moment. spin}), B(\text{Magnetic field})
\\
\triangle S = 0 \text{의 규칙이} ~ J\text{의 보존으로 설명 가능 함.} ~~~~J = L + S
\\
\therefore \text{A change in spin angular momentum}~S~ \text{compensated by an opposite change in orbital angular momentum}~L~
$$

$$
\text{Transition from}~ T'_1 ~\text{to} ~S'_0~ \text{by Fermi's Golden Rule}
\\
\begin{align}
\\
k_{if} &= \frac{2\pi}{\hbar} \vert \langle \mu \rangle_T \cdot F \vert ^2 \rho ~~~~~~~~~~~~~ \langle \mu \rangle_T = \langle ^{3}\Psi'_1 \vert e \hat{r} \vert ^{1}\Psi'_0 \rangle
\\
&\approx \frac{2 \pi}{\hbar}\rho \left[\sum_k \frac{\langle ^{1}\Psi^{0}_k \vert \triangle\hat{H}_{SOC} \vert ^{3}\Psi^{0}_1 \rangle}{E(T_1) - E(S_k)} \langle ^{1}\Psi^0 _k \vert e \hat{r} \vert ^{1}\Psi^0_0 \rangle\right]^2
\end{align}
$$
