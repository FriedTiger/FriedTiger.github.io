---
layout: single
title: "5)Crystal Vibration-Dispersion Relation"
typora-root-url: ../
categories : "Solid-State-Physics"
tag : phonon
#tag : [me, me2, me3]
toc : true
toc_sticky : true
author_profile : false
---
## Solid State Physics

앞서 Drude model과 Sommerfeld model은 Free-electron approximation을 적용하였다.

그러나, 실제로 ions들의 영향력이 크다.

---

#### 1-D atomic model

<img src="/images/5. Crystal vibration/image-20240413174724881.png" alt="image-20240413174724881" style="zoom:67%;" />

1-D atomic model은 $x_e$​ 근처에서 진자운동으로 표현가능하다. 

<img src="/images/5. Crystal vibration/image-20240413175401745.png" alt="image-20240413175401745" style="zoom:50%;" />
$$
\text{용수철에 저장된 에너지} : U(x) \approx U(x_e) + \frac{U^{''}(x_e)}{2!} (x-x_e)^2 = U(x_e) + \frac{\kappa}{2}(x-x_e)^2
$$
우리가 modeling하고자 하는 것은 여러 원자들이 용수철로 연결되어 있는 상황이다.

<img src="/images/5. Crystal vibration/image-20240413175450330.png" alt="image-20240413175450330" style="zoom:67%;" />
$$
\begin{align}
&\text{1. 두 원자 사이의 평형상태 거리 : a}
\\
&\text{2. n번째 원자의 위치 : }x_n
\\
&\text{3. n번째 원자의 평형상태 거리  : } \bar{x}_n =na
\\
&\text{4. n번째 원자의 움직이는 거리 : } \triangle x_n = x_n - \bar{x}_n
\\
\\
&\text{Chain에 저장되어 있는 에너지는 다음과 같다.}
\\
&U = \sum_i (x_{i+1} - x_i) = \sum_i \frac{\kappa}{2}[(x_{i+1} - x_i )-a]^2 = \sum_i \frac{\kappa}{2}[(x_{i+1} - \bar{x}_{i+1}) - (x_i - \bar{x}_{i})]^2 = \sum_i \frac{\kappa}{2}(\triangle x_{i+1}- \triangle x_i)^2
\\
\\
&\text{n번째 atom에 가해지는 힘은 다음과 같다.}
\\
&F_n = m \triangle \ddot{x}_n =  -\frac{\partial U}{\partial x_n} = \kappa(\triangle x_{n+1} - \triangle x_n) ~+~ \kappa(\triangle x_{n-1} - \triangle x_n) = \kappa(\triangle x_{n+1} - 2 \triangle x_n + \triangle x_{n-1})
\\
\\
&\text{진자 운동에서 우리는 steady-state일 때 진자들이 동일한 omega로 진동한다는 사실을 안다.}
\\
&\triangle x_n = A e ^{j(\omega t - k \bar{x}_n)} = A e^{j(\omega t - k n a)}
\\
\\
&\text{이를 위의 식에 대입하면 다음과 같음을 알 수 있다.}
\\
&-m \omega ^2 A e^{j(\omega t - k na )} = \kappa A e ^{ j \omega t }[e^{-jk(n+1)a} + e^{-jk(n-1)a} - 2e^{-jkna}]
\\
&-m\omega ^2 = \kappa[e^{-jka} + e^{jka}-2]
\\
& m\omega ^2 = 2\kappa(1-\cos ka) = 4 \kappa \sin ^2 ( \frac{ka}{2})
\\
\\
&\therefore \omega = 2 \sqrt{\frac{\kappa}{m}} \mid \sin (\frac{ka}{2}) \mid : \text{Dispersion relation}

\end{align}
$$
<img src="/images/5. Crystal vibration - Dispersion relation/image-20240414181302431.png" alt="image-20240414181302431" style="zoom:67%;" />

---

#### Dispersion relation

기본 개념

**Brillouin zone**: Dispersion relation을 k-space의 unit cell에서 표현한 것

**1st Brillouin zone** : $k=0$​​ 에서의 unit cell

<img src="/images/5. Crystal vibration - Dispersion relation/image-20240415103312113.png" alt="image-20240415103312113" style="zoom:50%;" />

**Longitudinal Wave(종파)** : 파동의 진동방향과 파동이 전파되는 방향이 같음. (유체)

**Transverse Wave(횡파)**  : 파동의 진동방향과 파동이 전파되는 방향이 수직임. (고체)

고체는 원자들이 결속되어 있음. 유체는 입자들 간의 결합력이 굉장히 약함. 따라서, 종파와 횡파의 차이가 발생함. 

고체에서는 파동의 전파방향과 수직으로 shear stress가 작용함. 고체 막대 끝을 횡방향으로 흔들 떄 전파가 어떻게 되는지를 생각해보면 편하다.
$$
\begin{align}
&\text{The speed of sound}
\\
&v = \sqrt{\frac{B}{\rho}} : B :\text{Bulk modulus}, ~ \rho :\text{mass density of a medium}
\\
&\text{고체가 물보다 B(탄성력과 관련)이 훨씬 크기 때문에 속도가 빠르다.}
\end{align}
$$
Dispersion relation
$$
\begin{align}
&\text{The speed of sound in 1D}
\\
&v = \sqrt{\frac{1}{\rho \beta}} = \sqrt{\frac{1}{\frac{m}{a} \cdot \frac{1}{\kappa a}}} = a \sqrt{\frac{\kappa}{m}}
\end{align}
$$
**Phase velocity(위상속도)** : $v_p = \frac{\omega}{k}$(0,0) 에서 (k,w)의 변화율

**Group velocity(군속도)** : $v_g = \frac{\partial \omega}{\partial k}$​(k,w)에서의 순간변화율

Group이라는 말이 이 현상에 대한 정확한 표현인지는 동의하지 않는다.

물리적 현상에 대한 알짜라는 말이 더 맞는 말 같다.

**Non-dispersive** : Phase velocity(위상속도) = Group velocity(군속도), 전파 도중에 wave의 모양이 바뀌지 않음.

**Dispersive** : Phase velocity(위상속도) $\neq$ Group velocity(군속도), 전파 도중에 wave가 점점 커지면서 사라짐.

다음의 상황이 가능하다.

<img src="/images/5. Crystal vibration - Dispersion relation/image-20240415152735299.png" alt="image-20240415152735299" style="zoom:67%;" />
$$
\begin{align}
&\omega = 2 \sqrt{\frac{\kappa}{m}}\mid \sin (\frac{ka}{2})\mid
\\
\\
&k \approx 0 \text{일 때}
\\
&\omega \approx 2 \sqrt{\frac{\kappa}{m}} \cdot \frac{ka}{2} = a \sqrt{\frac{\kappa}{m}} k
\\
&\text{이를 아래 그램으로 나타내자.}
\end{align}
$$
<img src="/images/5. Crystal vibration - Dispersion relation/image-20240415111140292.png" alt="image-20240415111140292" style="zoom:50%;" />

1-D atomic model은 k $\rightarrow$ k+ 2$\pi$m/a ( a: integer)의 periodic을 갖는다.

따라서, oscillation mode로 주기를 갖는 것을 알 수 있다. 이것이 의미하는 것은 무엇일까?
$$
\begin{align}
& G_m = \frac{2\pi}{a}m \text{~: 주기적인 set of points in k-space}
\\
&k\text{와}~ k+G_m\text{을 비교해보자.}
\\
&1.k \rightarrow \triangle x_n = Ae^{j(\omega t - k na )}
\\
&2.k + G_m \rightarrow \triangle x_n = Ae^{j(\omega t - (k + G_m)na)}
\\
\\
&\text{의미 :}
\\
&1. \omega \text{는 동일하다.}
\\
&2. \lambda \text{는 다르다.}
\\
&3. \bar{x}_n\text{(equilibrium position)는 같다.}
\\
&4. x\text{(arbitrary position)는 다르다.}
\\
\\
&\text{dispersion relation을 나타내는 파동은 파동 진행에 따라, 파장이 커지며 점점 사라지는 모습을 보인다.}
\\
&\text{그러나, periodic를 갖는다면 점점 사라지지 않고 진행하는 파동이 가능하다는 것을 알 수 있다.}
\end{align}
$$

---

#### Number of normal modes

$$
\begin{align}
&\text{Periodic boundary condition}
\\
&\triangle x_{n+N} = \triangle x_n
\\
&\text{이를 적용하면 다음과 같다.}
\\
&e^{-jkNa} =1
\\
&\therefore k = \frac{2\pi}{Na}p :~~~ p = \text{integer}
\\
&\text{Normal mode의 개수는 다음과 같다.}
\\
&\frac{\text{Range of k}}{\text{spacing between k}} = \frac{2\pi/a}{2\pi/Na} = N
\\
&\text{chain에서 원자 1개당 1개의 normal mode를 갖는다. }
\end{align}
$$

Question, Chain의 의미. Chain은 어떻게 잡아야 하는걸까?

--> by ChatGPt, Chain을 설정할 때, unit cell의 원자의 수로 주기로 잡는다. 이러한 unitcell은 3차원 상에서 무한히 반복되므로 실제로 많은 mode를 갖을 것이다.
