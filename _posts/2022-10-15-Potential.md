---
layout: single
title: "2)Potential"
typora-root-url: ../
categories : "Electromagnetic"
tag : charge
#tag : [me, me2, me3]
toc : true
toc_sticky : true
author_profile : false
---
## Electromagnetic 

 정전기학은 Coulumb's Law와 중첩의 원리가 가장 기본이다. 그러나, 이 2가지만 가지고 푸는 것은 쉽지 않다. 

왜냐하면 charge distribution을 아는 것이 어렵기 때문이다.

따라서, Electrical Potential에 대한 Poisson's equation --> Laplace's equation으로 이를 알아보려한다. 

즉, 이번 Chapter는 미분방정식 관점에서 어떻게 Electrostatic을 나타낼 수 있을지 알아보려고 한다.

---

#### Laplace's equation

$$
\triangledown ^2 V = - \frac{1}{\epsilon _0}\rho \text{ : Poission's equation}
\\
\triangledown ^2 V = 0 \text{ : Laplace's equation}
$$

Laplaces's equation의 해를 harmonic functions 이라고 한다. 

harmonic function으로 인해 다음의 성질을 갖는다.

1. 

   $$
   V(x) = \frac{1}{2}[V(x+a) + V(x-a)]
   \\
   \text{Laplace's equation은 boring 하다. }
   $$

2. $$
   \text{Laplace's equation은 local maxima or local minima 를 갖지 않는다.}
   $$

3. 

이와 관련된 정리를 **Uniqueness Theorems**이라고 한다.

#### Uniqueness Theorems

**First uniqueness theroem : ** Laplace's equation의 solution은 오로지 Boundary Surface S 에 의해 specified 된다.

**Second uniqueness theorem : ** Volume V가 conductor에 둘러 쌓여있더라도 conductor's charge density를 알면 specified 된다. (아래그림 참조)

<img src="/images/figure/image-20230504090432565.png" alt="image-20230504090432565" style="zoom:70%;" /><img src="/images/figure/image-20230504090522618.png" alt="image-20230504090522618" style="zoom:90%;" />

**--> Boundary Condition이 존재하고 내부 방정식이 Laplace'eqauation이라면 Boundary Condition의 평균이 그 점의 Potential이다.**

**Boundary Condition만 존재한다면 Laplace's Equation을 풀면 된다. **

1. 만약 Boundary Condition이 V로 딱 주어지지않고, 금속의 전하로 주어져도 uniqueness theorems를 적용할 수 있다.
2. $\triangledown ^2 V = \rho$ 와 같이 Laplace's equation이 아니더라도, 일정한 상수를 갖는 경우에 uniquencess thoerem이 성립한다.

---

#### Technique 1 - Image Problem

가상의 Image Charge를 통해 Boundary Condition은 유지하면서 Laplace's Equation을 푸는 방법이다.

<img src="/images/figure/image-20230504140308022.png" alt="image-20230504140308022" style="zoom:67%;" />

#### Technique 2 - Separation of Variables

Electrical Potential(V) 또는 Charge Density($\sigma$ )가 specified 된 상황에서 활용된다.

1. Cartesian Coordinate

<img src="/images/figure/image-20230504141034560.png" alt="image-20230504141034560" style="zoom:67%;" />

**풀이 **

Laplace's equation : $\frac{\partial ^2 V}{\partial x^2} + \frac{\partial ^2 V}{\partial y^2} = 0$

Boundary Condition : $V$= 0 ( y= 0, y = a), $V$ = $V_0$ (y) ( x = 0), $V \rightarrow 0 $  ( $ x \rightarrow \infty$ )
$$
V(x,y) = X(x)Y(y)
\\
\frac{1}{X} \frac{d^2 X}{d x^2} + \frac{1}{Y} \frac{d^2 Y}{d y^2} = 0
\\
\text{Let}~~~ \frac{d^2 X}{d x^2} = k^2 X, ~~\frac{d^2 Y}{d y^2} = -k^2 Y
\\
\therefore V (x,y) = (A e^{kx} + B e^{-kx})(C sinky + D cosky) 
\\
\text{Boundary Condition을 적용하면 다음과 같다.}
\\
V(x,y) = Ce^{-kx}sinky ~~\text{단,} ~~~k = \frac{n \pi}{a} ~~~\text{n = 1, 2, 3, ...}
$$
중요한 핵심은 **변수분리법은 Solution의 inifite family** 이다. 즉, Familty의 각 성분들은 모두 complete하다.
$$
\therefore V(x,y) = \sum ^{\infty} _{n=1} C_n e^{-n \pi x /a}sin(n \pi y /a)
\\
C_n\text{은 Fourier's Trick에 의해 다음과 같이 구할 수 있다.}
\\
C_n = \frac{2}{a} \int ^{a}_{0}V(0,y)sin(n \pi y / a)dy
$$

2. Spherical Coordinate - Legendre polynomial

---

#### Technique 3 - Multiple expansion : 먼 곳에서 바라보는 관점(dipole moment를 계산하고 이를 거리 r 에대해서 계산)

<img src="/images/figure/image-20230504144600335.png" alt="image-20230504144600335" style="zoom:80%;" />
$$
V(\bold{r}) = \frac{1}{4 \pi \epsilon _0}(\frac{q}{\eta_+} - \frac{q}{\eta_-}) 
\\
\eta^2_{\pm} = r^2(1 \mp\frac{d}{r}cos\theta + \frac{d^2}{4r^2}) \approx r^2(1 \mp \frac{d}{r}cos{\theta})
\\

\text{Binomial Expansion :} (1+x)^n = 1 + nx + n(n-1)x^2 + n(n-1)(n-2)x^3 + \cdot \cdot \cdot \text{에 따라 다음의 생략이 가능하다.}
\\
\frac{1}{\eta_{\pm}} \approx \frac{1}{r}(1 \pm \frac{d}{2r}cos\theta)
\\
\therefore \frac{1}{\eta_{+}} - \frac{1}{\eta_{-}} = \frac{d}{r^2}cos\theta
\\
\therefore V(\bold{r}) = \frac{1}{4 \pi \epsilon _0} \frac{qdcos\theta}{r^2}
$$
만약, 위의 식처럼 Dipole이 아닌 Charge distribution이 있다면 binomial expansion 을 approximation 하지 않고 그대로 쓴다면 다음과 같다.

<img src="/images/figure/image-20230504150434283.png" alt="image-20230504150434283" style="zoom:60%;" /> 
$$
V(\bold{r}) = \frac{1}{4 \pi \epsilon _ 0 }[\frac{1}{r}\int \rho(\bold{r^{'}})d\tau ^{'} +\frac{1}{r^2}\int r' cos{\alpha} \rho(\bold{r^{'}})d\tau ^{'}+ \cdot \cdot \cdot ]
\\
= \text{ monopole term + dipole term + quadratic term +} \cdot \cdot \cdot \text{: 물리적 의미}
$$

|         | Physical Dipole (Dipole moment : $p=\int r' \rho(\bold{r'})d\tau ')$ | Pure Dipole                         | Multipole                                |
| ------- | ------------------------------------------------------------ | ----------------------------------- | ---------------------------------------- |
| Meaning | monopole term + dipole term = 근사                           | monopole term + dipole term=실제 값 | monopole term + dipole term + quadrupole |

 ex) Physical Dipole in atom = monopole term + dipole term

: monopole term : 0 

: dipole term : $\frac{1}{4 \pi \epsilon _0} \frac{1}{r^2} \int r' cos \alpha \rho(\bold{r}')d\tau'$

