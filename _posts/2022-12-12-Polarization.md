---
layout: single
title: "9-2)Polarization"
typora-root-url: ../
categories : "Electromagnetic"
tag : electrodynamics
#tag : [me, me2, me3]
toc : true
toc_sticky : true
author_profile : false
---
## Electromagnetic 

#### Plane of Incidence

plane wave를 decompose 시키고 이를 Plane of incidence에서 분석할 수 있다.

<img src="/images/figure/image-20230223234736209.png" alt="image-20230223234736209" />

---

#### 거울대칭

<img src="/images/9.2 Polarization/image-20240104085120143.png" alt="image-20240104085120143" style="zoom:67%;" />

y축에 수직한 평면으로 자를 때 y축에 대해 어느 곳에서 잘라도 잘라진 두 도형은 거울대칭을 이루게 된다.

거울대칭을 이룬다는 말은 거울대칭에 대한 $\vec{S}$ 와 멕스웰 방정식의 operator가 같은 eigenfunction을 공유할 수 있다는 것이다.

이때,  y축에 대한 전기장 또는 자기장의 방향이 보존되는 사실을 알 수 있고.

x 축에 대한 자기장 또는 전기장의 방향도 마찬가지로 거울대칭이므로 보존되는 사실을 알 수 있다.

따라서, 전자기파를 전기장에 대해 S-Pol, Y-pol로 나누어 생각할 수 있고 이를 생각할 때, 전기장 또는 자기장 방향 보존을 고려해서 식을 풀면 된다.

---

#### S-polarization

<img src="/images/9.2 Polarization/image-20240104093835765.png" alt="image-20240104093835765" style="zoom:67%;" />
$$
\begin{align}
&\text{1) 전기장이 y축에 대해 보존성을 갖음.}
\\
&\vec{\bold{E}}_{inc} = \hat{y} E_0 e^{i\vec{k}\cdot \vec{r}}
\\
&\vec{\bold{E}}_{refl} = \hat{y} ~rE_0 e^{i\vec{K}\cdot \vec{r}}
\\
&\vec{\bold{E}}_{trans} = \hat{y} ~tE_0 e^{i\vec{q}\cdot \vec{r}}
\\
\\
&\text{Boundary condition : } \vec{\bold{E}}_1 = \vec{\bold{E}}_2\text{에 의해}
\\
&1+r = t
\\
\\
&\text{2) 자기장이 x축에 대해 보존성을 갖음.}
\\
&\triangledown \times \vec{\bold{E}}(r) = i \omega \mu ~\vec{\bold{H}}(r) \text{에 의해 다음으로 나타낼 수 있음.}
\\
&\vec{\bold{H}}_{inc} = \vec{k} \times \hat{y} ~\frac{E_0}{\omega \mu_1}e^{i \vec{k}\cdot \vec{r}}
\\
&\vec{\bold{H}}_{refl} = \vec{K} \times \hat{y} ~\frac{rE_0}{\omega \mu_1}e^{i \vec{K}\cdot \vec{r}}
\\
&\vec{\bold{H}}_{trans} = \vec{q} \times \hat{y} ~\frac{tE_0}{\omega \mu_2}e^{i \vec{q}\cdot \vec{r}}
\\
\\
&\text{Boundary condition : } \vec{\bold{H}}_1 = \vec{\bold{H}}_2\text{에 의해}
\\
&\frac{k_z}{\mu _1} + \frac{r K_z}{\mu_1}= \frac{t q_z}{\mu_2}
\\
\\
&\text{이를 모두 종합하여 정리하면 다음과 같다.}
\\
&r = \frac{\mu_2 k_z - \mu_1 q_z }{\mu_1 q_z - \mu_2 K_z} = \frac{\mu_2 k_z - \mu_1 q_z}{\mu_1 q_z + \mu_2 k_z} = r(k_z)
\\
&t= 1 + r = \frac{2\mu_2 k_z}{\mu_1 q_z + \mu_2 k_z} = t(k_z)
\\
&\text{이를 Fresnel's equation이라 한다.}
\\
\\
&R = \mid\frac{\langle S_r \rangle_z}{\langle S_{inc} \rangle_z}\vert = \frac{(\hat{K})_z\frac{1}{2}\sqrt{\frac{\epsilon _1}{\mu_1}}\vert r \vert ^2 \vec{\bold{E}}\cdot \vec{\bold{E}}*}{(\hat{k})_Z\frac{1}{2}\sqrt{\frac{\epsilon _1}{\mu_1}}\vec{\bold{E}}\cdot \vec{\bold{E}}*} = \vert r \vert ^2
\\
&T = \mid\frac{\langle S_t \rangle_z}{\langle S_{inc} \rangle_z}\vert = \frac{(\hat{q})_z\frac{1}{2}\sqrt{\frac{\epsilon _2}{\mu_2}}\vert t \vert ^2 \vec{\bold{E}}\cdot \vec{\bold{E}}*}{(\hat{k})_z\frac{1}{2}\sqrt{\frac{\epsilon _1}{\mu_1}}\vec{\bold{E}}\cdot \vec{\bold{E}}*} =  \frac{n_2 \cos\theta _t}{n_1 \cos\theta _i}\vert t \vert ^2
\end{align}
$$

#### S-pol에서 Energy 전달에 대한 상황

$$
\begin{align}
&\text{앞서 구한 }R_z, T_Z
\\
&R_z+T_z = 1\text{을 만족해야한다.}
\\
&R_z + T_z = \vert r \vert ^2 + \frac{n_2 cos \theta _t}{n_1 cos \theta _i }\vert t \vert ^2 = \vert r \vert ^2 + \frac{q_z}{k_z}\vert t \vert ^ 2 =   \vert r \vert ^2 + \frac{1-r}{t} \vert t \vert ^2 = \vert r \vert ^2 + (1-r)(1+r) = 1
\\
\\
&R_{x}, T_{x}\text{에 대해서도 파악해보자.}
\\
&R_{x} = \vert r \vert ^2
\\
&T_{x} = \vert t \vert ^2 \text{이유 : wave vector의 평행성분은 바뀌지 않으므로 전기장의 크기만 고려하면 된다.}
\\
&R_{x} + T_{x} = 1\text{이 성립 안하는 이유 :} \langle{S_{inc}}\rangle_x + \langle{S_r} \rangle _x\text{가 방향이 같아 복합적임.} 
\end{align}
$$

이를 그림으로 나타내면 다음과 같다.

<img src="/images/9.2 Polarization/image-20240104122637281.png" alt="image-20240104122637281" style="zoom:80%;" />

얻을 수 있는 것. 

1) wave vector가 커지면, 운동량이 커지고 에너지도 증가한다.
2) 그러나, 전기장 및 자기장의 세기가 작아져 전체적인 에너지가 차이가 날 수 있다.

---

#### S-pol에서 Total reflection(전반사)

$$
\begin{align}
&r^s(k_z) = \frac{\mu _2k_z - \mu_1q_z}{\mu _1q_z + \mu_2 k_z} = \frac{\mu _2 \sqrt{\mu_1 \epsilon _1}cos\theta _i - \mu _1 \sqrt{\mu_2 \epsilon _2}cos\theta _t}{\mu _2 \sqrt{\mu _1 \epsilon _1}cos\theta _i + \mu_1 \sqrt{\mu _2 \epsilon _2} cos\theta_t}
\\
&r = 1\text{을 만족하는 값이 존재할 것인지 알아봐야한다.}
\\
\\
&\text{if, loss less media라면}
\\
&r^s(k_z) = \text{(준식)} = \frac{\alpha - \beta}{\alpha + \beta} < 1 \text{이다.}
\\
\\
&\text{if, lossy media라면}
\\
&r^s(k_z) = \frac{\sqrt{\frac{\epsilon _1}{\mu _1}}cos\theta _i - \sqrt{\frac{\epsilon _2}{\mu _2}}cos\theta _t}{\sqrt{\frac{\epsilon _1}{\mu _1}}cos\theta _i + \sqrt{\frac{\epsilon _2}{\mu _2}}cos\theta _t}
\\
\\
&\vert r^s \vert = 1\text{이라 가정하고, } \eta = \sqrt{\frac{\mu}{\epsilon}} \text{라고 정의하자.}
\\
&\vert r^s \vert^2 = r^s r^{s*} = \frac{\eta^{-1}_1 cos \theta_i - \eta^{-1}_2 cos \theta_t}{\eta^{-1}_1 cos \theta_i + \eta^{-1}_2 cos \theta_t} \frac{\eta^{-1}_1 cos^* \theta_i - \eta^{-1}_2 cos^* \theta_t}{\eta^{-1}_1 cos^* \theta_i + \eta^{-1}_2 cos^* \theta_t} = 1
\\
&\text{이를 전개하여 정리하면 다음과 같다.}
\\
&\eta^{-1}_1 \eta^{-1}_2 Real(cos \theta _i cos ^* \theta _t) = 0 
\\
&\therefore Real(cos^* \theta_t) = 0
\\
\\
&\therefore cos \theta_t : \text{purely imaginary}
\\
&\therefore sin \theta_t = \frac{\sqrt{\epsilon_1 \mu_1}}{\sqrt{\epsilon _2 \mu _2}}sin \theta_i > 1
\end{align}
$$

---

#### S-pol에서 전반사시에 Energy 전달

$$
\begin{align}
&\vec{\bold{E}}_{trans} = \hat{y} ~tE_0 e^{i\vec{q}\cdot \vec{r}}
\\
&\vec{\bold{E}}_{trans} = \hat{y} ~t E_0 e^{iq(sin\theta_t x + cos\theta_t z)}
\\
\\
&cos\theta _t = 1- sin^2 \theta_t = 1 - \frac{\epsilon _1 \mu _1}{\epsilon _2 \mu _2}sin^2 \theta_i
\\
&cos\theta _t = \pm i \sqrt{\frac{\epsilon _1 \mu _1 sin^2 \theta _i - \epsilon _2\mu_2}{\epsilon _2\mu_2}}
\\
&sin\theta _t = \frac{\sqrt{\epsilon _1 \mu_1}}{\sqrt{\epsilon _2 \mu _2}}sin\theta _i \text{이를 모두 대입하면 다음과 같다.}
\\
&\vec{\bold{E}}_{trans} = \hat{y} ~t E_0 e^{i \omega \sqrt{\epsilon _2 \mu _2}(\frac{\sqrt{\epsilon _1 \mu_1}}{\sqrt{\epsilon _2 \mu _2}}sin\theta _i x \pm i \sqrt{\frac{\epsilon _1 \mu _1 sin^2 \theta _i - \epsilon _2\mu_2}{\epsilon _2\mu_2}} z)}
\\
&\vec{\bold{E}}_{trans} = \hat{y} ~t E_0e^{- \omega \sqrt{\epsilon _1 \mu _1 sin^2 \theta_i - \epsilon _2 \mu _2}~z}~e^{i\omega \sqrt{\epsilon _1 \mu _1}sin\theta _i ~x}
\\
&\vec{\bold{E}}_{trans} = \hat{y} ~t E_0 e^{- \frac{\omega}{c}\sqrt{n^2_1sin^2 \theta_i-n^2_2}~ z} ~e^{i \frac{\omega}{c}\sqrt{n_1}sin\theta_i x}
\\
&\text{이를 evanescent wave라 표현한다.}
\end{align}
$$

그림으로 나타내면 다음과 같다.

<img src="/images/9.2 Polarization/image-20240106092638371.png" alt="image-20240106092638371" style="zoom:67%;" />

자기장에 대해서도 생각해보자.
$$
\begin{align}
&\vec{\bold{H}}_{trans} = \vec{q} \times \hat{y} ~\frac{tE_0}{\omega \mu_2}e^{i \vec{q}\cdot \vec{r}}
\\
&\vec{\bold{E}}_{trans} = \hat{y} ~tE_0 e^{i\vec{q}\cdot \vec{r}}
\\
&\text{따라서, 전기장과 마찬가지로 evanescent field로 나타나는 것을 알 수 있다.}
\\
&\text{wave와 field는 엄격하게 다르다.}
\\
&\text{propagating wave와 evanescent를 구분할 줄 알아야 한다. 8참고}
\\
&\vec{k}\text{가 표면을 따라서 움직인다. } ~\vec{\bold{H}}\text{는} \pm\hat{z}\text{을 가리킨다.}
\\
&\vec{k}\text{가 있지 않은 공간(evanescent field)에서 poynting vector의 시간평균을 계산하면 0으로 예상된다.}
\\
&\text{wavevector가 허수 값을 갖는다 라는 것은 무슨 의미일까?}
\end{align}
\\
$$


---

#### P-polarization

<img src="/images/9.2 Polarization/image-20240104160052106.png" alt="image-20240104160052106" style="zoom:67%;" />
$$
\begin{align}
&\text{1) 자기장이 y축에 대해 보존성을 갖음.}
\\
&\vec{\bold{H}}_{inc} = \hat{y} H_0 e^{i\vec{k}\cdot \vec{r}}
\\
&\vec{\bold{H}}_{refl} = \hat{y} ~rH_0 e^{i\vec{K}\cdot \vec{r}}
\\
&\vec{\bold{H}}_{trans} = \hat{y} ~tH_0 e^{i\vec{q}\cdot \vec{r}}
\\
\\
&\text{Boundary condition : } \vec{\bold{H}}_1 = \vec{\bold{H}}_2\text{에 의해}
\\
&1+r = t
\\
\\
&\text{2) 전기장이 x축에 대해 보존성을 갖음.}
\\
&\triangledown \times \vec{\bold{H}}(r) = -i \omega \vec{\bold{D}}(r) \text{에 의해 다음으로 나타낼 수 있음.}
\\
&\vec{\bold{E}}_{inc} = -(\vec{k} \times \hat{y}) ~~\frac{H_0}{\omega \epsilon_1}e^{i \vec{k}\cdot \vec{r}}
\\
&\vec{\bold{E}}_{refl} = -(\vec{K} \times \hat{y}) ~~\frac{rH_0}{\omega \epsilon_1}e^{i \vec{K}\cdot \vec{r}}
\\
&\vec{\bold{E}}_{inc} = -(\vec{q} \times \hat{y}) ~~\frac{tH_0}{\omega \epsilon_2}e^{i \vec{q}\cdot \vec{r}}
\\
\\
&\text{Boundary condition : } \vec{\bold{E}}_1 = \vec{\bold{E}}_2\text{에 의해}
\\
&\frac{k_z}{\epsilon _1} + \frac{r K_z}{\epsilon_1}= \frac{t q_z}{\epsilon_2}
\\
&\text{S-pol에서 분모에}\mu\text{가} \epsilon\text{로 된 것을 알 수 있다.}
\\
\\
&\text{이를 모두 종합하여 정리하면 다음과 같다.}
\\
&r = \frac{\epsilon_2 k_z - \epsilon_1 q_z }{\epsilon_1 q_z - \epsilon_2 K_z} = \frac{\epsilon_2 k_z - \epsilon_1 q_z}{\epsilon_1 q_z + \epsilon_2 k_z} = r(k_z)
\\
&t= 1 + r = \frac{2\epsilon_2 k_z}{\epsilon_1 q_z + \epsilon_2 k_z} = t(k_z)
\\
&\text{이를 Fresnel's equation이라 한다.}
\\
\\
&\text{S-pol 상황과는 다르게 } r = 0\text{인 상황이 존재한다.}
\\
&\epsilon _2 k_z = \epsilon_1 q_z
\\
&\text{이를 만족시키는 }\theta\text{를 Brewster's angle이라고 한다.}
\\
\\
&\vec{S}(r,t) = \vec{E}(r,t) \times \vec{H}(r,t) = - \frac{\vec{k} \times \vec{H}(r,t)}{\omega \epsilon} \times \vec{H}(r,t) = \frac{1}{\omega \epsilon} \vec{H}(r,t) \times (\vec{k} \times \vec{H}(r,t)) = \vec{k} \frac{\vec{H}(r,t) \cdot \vec{H}(r,t)}{\omega \epsilon}
\\
&\text{이를 phasor로 나타내고 시간평균으로 표현하면 다음과 같다.}
\\
&\langle \vec{S} \rangle = \vec{k} \frac{1}{2\omega \epsilon} Real(\vec{\bold{H}}\cdot \vec{\bold{H}}^*)
\\
&R = \mid\frac{\langle S_r \rangle_z}{\langle S_{inc} \rangle_z}\vert = \frac{(\vec{K})_z\frac{1}{2}\frac{1}{\epsilon _1}\vert r \vert ^2 \vec{\bold{H}}\cdot \vec{\bold{H}}*}{(\vec{k})_z\frac{1}{2}\frac{1}{\epsilon_1}\vec{\bold{H}}\cdot \vec{\bold{H}}*} = \vert r \vert ^2
\\
&T = \mid\frac{\langle S_t \rangle_z}{\langle S_{inc} \rangle_z}\vert = \frac{(\vec{q})_z\frac{1}{2}\frac{1}{\epsilon_2}\vert t \vert ^2 \vec{\bold{H}}\cdot \vec{\bold{H}}*}{(\vec{k})_z\frac{1}{2}\frac{1}{\epsilon_1}\vec{\bold{H}}\cdot \vec{\bold{H}}*} =  \frac{q_z \frac{1}{\epsilon _2}}{k_z \frac{1}{\epsilon _1}}\vert t \vert ^2 = \frac{\epsilon _ 1 q_z}{\epsilon _2 k_z}\vert t \vert ^2
\end{align}
$$

---

#### P-pol에서 Energy 전달 상황

<img src="/images/9.2 Polarization/image-20240105104626568.png" alt="image-20240105104626568" style="zoom:67%;" />

평행한 면에서의 Energy 전달 상황을 S-pol에서 처럼 에너지가 그냥 흘러간다 라고 생각하는게 좋을 것 같다.

---

#### P-pol에서 Total transmission(전투과)

$$ { }
\begin{align}
&r(k_z) = \frac{\epsilon_2 k_z - \epsilon_1 q_z}{\epsilon_1 q_z + \epsilon_2 k_z}\text{이므로}
\\
&\epsilon_2k_z = \epsilon_1q_z\text{일 때}~r = 0\text{을 나타낸다.}
\\
&\text{이를 서술하여 나타내보자.}
\\
&\epsilon_2\sqrt{\epsilon_1 \mu _1}cos\theta_i = \epsilon_1 \sqrt{\epsilon_2 \mu _2}cos\theta_t
\\
&\epsilon_2 ^2  \epsilon_1 \mu _1 cos^2\theta _i = \epsilon_1 ^2 \epsilon_2 \mu_2cos^2\theta_t
\\
&\text{좌변 : }\epsilon_2 ^2  \epsilon_1 \mu _1(1 - sin^2\theta _i)
\\
&\text{우변 : }\epsilon_1 ^2 \epsilon_2 \mu_2(1 - sin^2\theta _t) = \epsilon_1 ^2 \epsilon_2\mu _2(1 - \frac{\epsilon _1 \mu _1}{\epsilon _2 \mu_2}sin^2 \theta _i) = \epsilon ^2_1 \epsilon_2 \mu _2 - \epsilon^2_1 \epsilon_1\mu _1sin^2 \theta_i
\\
&\text{좌변 = 우변이므로}
\\
&\epsilon _1 \mu _1(\epsilon^2 _2\mu _1 - \epsilon^2 _1 \mu_2) = \epsilon_1 \epsilon_2(\epsilon^2_2 - \epsilon ^2_1)sin^2 \theta _i
\\
&sin^2 \theta _i = \frac{\epsilon _1 \epsilon _2 ( \epsilon_2 \mu _1 - \epsilon _1 \mu _2)}{\epsilon _1 \mu_1 (\epsilon^2_2 - \epsilon^2_1)} = \frac{\epsilon ^2 _2 - \frac{\epsilon _1 \epsilon _2 \mu_2}{\mu_1}}{\epsilon ^2_2 - \epsilon ^2_1}
\\
&sin^2 \theta _i = \frac{\frac{\epsilon _2}{\epsilon _1} - \frac{\mu _2}{\mu _1}}{\frac{\epsilon _2}{\epsilon _1} - \frac{\epsilon _1}{\epsilon _2}} = \frac{\epsilon _2}{\epsilon _1 + \epsilon _2}(\text{for non-magnetic materials})
\\
&\therefore \theta _i = \theta_B = tan^{-1}\sqrt{\frac{\epsilon _2}{\epsilon _1}} : \text{Brewster's angle}
\end{align}
$$




---

#### Brewster's angle 

P polarized에서 저굴절률에서 고굴절률로 빛이 진행해 갈 때, 입사각 $\theta_1$ 과 굴절각 $\theta_2$ 의 합이 90이 된다면 

나타내는 현상으로 모든 빛이 굴절되는 것을 의미한다.

* 전반사와는 다른 개념이다.

---

#### Scattering 

빛이 입자를 만났을 때 90도 넘게 꺾이는 것을 scattering이라 한다.

이때, 입자의 크기가 micron 이하라면, Blue파장 이하가 Scattering이 많아지고,

입자의 크기가 micron 이상이라면, 색에 대한 dependency가 없다.

<img src="/images/figure/image-20230224000342949.png" alt="image-20230224000342949" style="zoom:67%;" />



* 빛의 모든 것은 plane wave로 부터 생각하자. --> unpolarized light는 plane wave의 중첩

1) 구름은 물분자의 입자가 커서 scattering이 색에 대해 dependent하지 않는다
2) 하늘이 파랗게 보이는 이유는 입자가 먼지수준으로 작아서, 파란 빛이 scattering이 많이 되기 때문이다.
3) 노을이 빨갛게 보이는 이유는 많은 공기중을 지나오며 파란 빛이 많이 scattering 되어 나갔기 때문이다.
4) 태양 빛에서 polarized된 빛을 보고 싶다면, 노을과 같이 90도 방향으로 빛이 들어올 때 정중앙에 하늘 빛을 보면 관측할 수 있다.