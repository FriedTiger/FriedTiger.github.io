---
layout: single
title: "8)OLED Charge Transport"
typora-root-url: ../
categories : "OLED"
tag : exciton
#tag : [me, me2, me3]
toc : true
toc_sticky : true
author_profile : false
---
## OLED

#### Conductivity

$$
j = \sigma E
\\
\sigma = q \mu n
$$

| Material      | Conductivity(S/m)                                            |
| ------------- | ------------------------------------------------------------ |
| Insulator     | $10^{-23}$ ~ $10^{-14}$                                      |
| Semiconductor | Variable($\because$ charge carrier density $\rightarrow$ Doping을 통해 조절할 수 있음.) |
| Metal         | $10^7$ ~ $10^8$                                              |

#### Mobility

$$
v = \mu E
$$



| Application | $\mu$ ($cm^2$ /V$\cdot$ s)         |
| ----------- | ---------------------------------- |
| Silicon     | 1000                               |
| TFT         | 0.1 $\rightarrow$ 1                |
| Opto        | $10^{-10}$ $\rightarrow$ $10^{-4}$ |

Why organic semiconductor have low conductivity?

1. $\bold{\text{Low carrier density}}$
2. $\bold{\text{Low electric mobility}}$ $\because$ 1) Polarization 2)Disorder $\rightarrow$ Localization of carrier density

---

#### View of Mobility

**1. Polarization**

<img src="/images/figure/image-20230604150451223.png" alt="image-20230604150451223" style="zoom:80%;" />

Inorganic이 Organic보다 residence time이 작다. 

그러나, Polarization time이 $10^{-15}(s)$ 이므로 Organic은 polarization에 영향을 받는다. 이는 Organic 물질의 bandwidth가 연속적이지 않고, 전자가 transfer 되기 위해서는 resonance가 발생해야하기 때문에 Organic이 residence time이 길다.

<img src="/images/figure/image-20230604151114312.png" alt="image-20230604151114312" />

이를 Organic에서 전자를 Polaron이라고 통틀어 칭하고 다음 configuration과 같다.

<img src="/images/figure/image-20230604151540823.png" alt="image-20230604151540823" style="zoom:80%;" />

Polaron을 통해 전자의 에너지는 더욱 안정해진다.(Binding E $\uparrow$ )

이는 다음처럼 핵-전자의 model로 설명할 수 있다.

<img src="/images/figure/image-20230604153907194.png" alt="image-20230604153907194" style="zoom:67%;" />

이를 에너지밴드로 설명하면 다음처럼 Resonance가 일어나야 charge transfer가 설명이 된다.

**Polaronic Transport**

<img src="/images/figure/image-20230604154010914.png" alt="image-20230604154010914" />

Resonance가 일어날 수 있는 상황은 Acceptor의 thermal agitation 또는 Donor의 thermal agitation 2가지 상황으로 나눠서 생각할 수 있다.

<img src="/images/figure/image-20230604154238437.png" alt="image-20230604154238437" style="zoom:67%;" />

**2.Disorder**

Organic 물질은 inorganic Crystalline과 다르게 Disorder로 배열이 존재한다.

<img src="/images/figure/image-20230604154735569.png" alt="image-20230604154735569" style="zoom:67%;" />

Inorganic Crystalline model $\rightarrow$ Wavefunction : Bloch's Theorem 

Organic model $\rightarrow$ Wavefunction : exponential function

<img src="/images/figure/image-20230604154924164.png" alt="image-20230604154924164" style="zoom:80%;" />

따라서, wavefunction의 overlap이 transport 정도를 결정한다.<img src="/images/figure/image-20230604155010486.png" alt="image-20230604155010486" style="zoom:70%;" />

---

#### View of Carrier density : Density of States

<img src="/images/figure/image-20230604155332599.png" alt="image-20230604155332599" />

Organic Semiconductor는 일반적으로 gaussian Density of states를 나타낸다. 이를 model화 하기 위해서 많은 노력들이 있다.

1. **Multiple trapping & Release (MTR) Model : weakly disorderd system (shallow trap)**

<img src="/images/figure/image-20230604160028954.png" alt="image-20230604160028954" style="zoom:80%;" />

이 model을 통해서 shallow trap의 에너지준위를 통해 mobility를 구할 수 있다.
$$
\text{Effective Mobility}
\\
\mu \approx\mu _0 \frac{N_c}{N_t}exp(- \frac{E_c - E_t}{k_B T})
$$

2. **Miller-Abraham's model**

<img src="/images/figure/image-20230604160832626.png" alt="image-20230604160832626" />ol

Shallow Trap으로 설명하는 것이 아닌 모든 state들을 hopping 개념으로 본다. 

에너지가 높은 곳에서 낮은 곳으로 가는 것이 자연스럽기 때문에 이를 평균내었을 때, Transport E를 MAX DOS보다 살짝 아래 위치한다고 여긴다.

<img src="/images/figure/image-20230604161006284.png" alt="image-20230604161006284" />

**3. Gaussian Disorder Model** : 제일중요

<img src="/images/figure/image-20230604161100872.png" alt="image-20230604161100872" />

mobility를 구할 때, 에너지와 위치 모두 고려한 식이고 이에 영향을 주는 변수는

Electric Field($F$), Temperature, Energetic disorder, Positional disorder이다.

이에 관해 깊게 공부한 내용들은 다음 페이지에 추가로 적기로 하자.