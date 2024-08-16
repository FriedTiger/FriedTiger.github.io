---
layout: single
title: "5)PN Junction Diodes"
typora-root-url: ../
categories : "Fundamental-of-Semicondutor"
tag : diode
#tag : [me, me2, me3]
toc : true
toc_sticky : true
author_profile : false
---
## Fundamental of semiconductor

<img src="/images/5. pn Junction Diodes/image-20221102200301524.png" alt="image-20221102200301524" style="zoom:80%;" />

#### How to make PN junction?

전기가 잘 흐르지 않는 반도체를 도핑을 통해 전기가 잘 흐르게 만든다. 

PN junction은 각각 도핑된 반도체를 접한 한 것이 아니라, 두번 도핑을 통해서 junction을 만든 것이다. 

도핑된 반도체는 금속과 같이 전류가 잘 흐를 수 있기 때문에 junction을 **metallurgical junction**이라 한다.

Metallurgical junction에서 non-zero charges 인 곳을 발견 할 수 있는데 이를

#### Space chage region 

or

#### Depletion region

이라 한다.

<img src="/images/5. pn Junction Diodes/image-20221102194935017.png" alt="image-20221102194935017" style="zoom:80%;" />

이를 다음과 같이 두가지 측면으로 근사시킬 수 있다.

<img src="/images/5. pn Junction Diodes/image-20221102195204760.png" alt="image-20221102195204760" style="zoom:80%;" />

---

#### Non-Bias 정성적 이해 ( Qualitative )

<img src="/images/5. pn Junction Diodes/image-20221102200633128.png" alt="image-20221102200633128" style="zoom:80%;" /><img src="/images/5. pn Junction Diodes/image-20221102200651487.png" alt="image-20221102200651487" style="zoom:80%;" /><img src="/images/5. pn Junction Diodes/image-20221102200707103.png" alt="image-20221102200707103" style="zoom:80%;" />

charge density --> 전기장 --> Potential 차이 로 생각할 수 있다.

즉, 원자핵과 전자의 관계를 harmonic oscillator라고 생각 한다면

 charge denisty 차이로 인해 p형반도체가 높은 electron potential energy(관악산)에 harmonic oscillator가 있다고 생각할 수 있다.

---

#### Non-Bias, Built-in Potential($V_{bi}$) 정성적 이해 (Qualitative)

1)  평형 조건 & Einstein Relationship 활용 

$$
\text{ 평형 조건 in depletion region}
\\
\rightarrow J_N = q \mu_n n E + qD_N \frac{dn}{dx} = 0
\\
\\
\text{Einstein Relationship}
\\ E = - \frac{D_N}{\mu_n}\frac{dn/dx}{n} = -\frac{kT}{q}\frac{dn/dx}{n}
\\
\\
\therefore V_{bi} \text{는 다음과 같다.}
\\
V_{bi} = - \int ^{x_n} _{x_p} E dx =  \frac{kT}{q}ln[\frac{n(x_n)}{n(-x_p)}]= \underline {\frac{kT}{q}ln[\frac{N_A N_D}{n_i^2}]}
$$

이를 해석해보자. 

Einstein Relationship을 평형조건을 통해 전기장에 대한 식을 만들었다.

도핑 농도가 클수록 V_bi는 로그함수 적으로 증가한다. 이를 다르게 해석하면 V_bi는 생각보다 크지 않은 값임을 알 수 있다.

또한 Built-in Potential 을 Fermi Level 에너지 차이로도 해석할 수 있다.
$$
V_{bi} = \frac{1}{q}[(E_i - E_F)_{p-side}+(E_F - E_i)_{n-side}]
$$




2. Depletion Approxim ation으로 부터 구해보기

Poisson equation은 다음과 같다.
$$
\frac{dE}{dx} = \frac{ \rho}{k_s \epsilon _0} = \frac{q}{k_s \epsilon_0}(p~-n~+N^+_D - N^-_A)
\\
\text{Dopant는 모두 완전히 이온화되어있다고 생각한다.}
$$
따라서 이 식을 단순히 구하면 모든 것이 풀린다. 그러나, ex) p or n은 에너지준위로 구할 수 있는데 이는 전기장과 관련있다. 그러나 전기장은 p or n으로 구할 수 있다. 따라서 얽히고 섥혀있다. 이를 구하려면 computer로 풀어야한다.

따라서, Approximation을 통해서 구하려한다.

<img src="/images/5. pn Junction Diodes/image-20221102202045392.png" alt="image-20221102202045392" style="zoom:80%;" /> 

Gauss's law를 적용하면 다음을 알 수 있다.
$$
N_D^+ x_n = N_A^- x_p
$$

$$
V_{bi} = E_{Fi} - E_F (in~p형) + E_F-E_{Fi} (in~n형)
$$

위의 charge density - x 그래프를 적분해보자.

<img src="/images/5. pn Junction Diodes/image-20221224152318913.png" alt="image-20221224152318913" style="zoom:80%;" />

적분을 통해 식을 전개하면 $V_{bi}$을 얻을 수 있다,
$$
V_{bi} = \frac{qN_A}{2K_s \epsilon_0}x_p^2 + \frac{qN_D}{2K_s \epsilon_0}x_n^2
$$
따라서, (1)식과 (2)식을 조합하면 depletion width를 구할 수 있다.
$$
W = x_n + x_p = [\frac{2K_s\epsilon_0}{q}(\frac{1}{N_A}+\frac{1}{N_D})V_{bi}]^{1/2}
$$
(6)식을 조합해서 생각하면 V_bi와 W는 마치, 찰흙을 누르는 것과 비슷한 성질을 띠는 것을 알 수 있다.



#### 정리

<img src="/images/5. pn Junction Diodes/image-20231004094201043.png" alt="image-20231004094201043" style="zoom:67%;" />

---

#### On-Bias, Built-in Potential($V_{bi}$) 정량적 이해 (Quantitative)

Bias가 가해진 상황에서 depletion region의 $N_{D}$ 와 $N_{A}$ 는 변하지 않는다. 

따라서 on-bias에서 달라지는 것은 $x_{n}$ 과 $x_{p}$ 이다. 이를 그래프로 그리면 다음과 같다.

<img src="/images/5. pn Junction Diodes/image-20221224164328909.png" alt="image-20221224164328909" style="zoom:80%;" />

그래프에서 살펴보면 $ V_A $가 변화함에 따라 $ x_n $ 와 $ x _ p $ 가 linear 하게 변화하는 것을 알 수 있다. 

이에 따라 depletion region에 작용하는 $V_{bi} $ 가 linear 하게 변화한다. 따라서, 이를 6식에 대입하면 다음과 같다.
$$
W = x_n + x_p = [\frac{2K_s\epsilon_0}{q}(\frac{1}{N_A}+\frac{1}{N_D})(V_{bi} - V_{A})]^{1/2}
$$


만약 step junction이 아닌 다른 doping profile을 보인다면 위의 1. 2. 를 모두 이용하여 구하면 된다.