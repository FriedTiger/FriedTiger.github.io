---
layout: single
title: "6)Crystal Vibration-phonon"
typora-root-url: ../
categories : "Solid State Physics"
tag : phonon
#tag : [me, me2, me3]
toc : true
toc_sticky : true
author_profile : false
---
## Solid State Physics

<img src="/images/6. Crystal vibration - phonon/image-20240429133755187.png" alt="image-20240429133755187" />

phonon : quantized crystal vibration을 의미한다.

따라서, 다음과 같이 기술할 수 있다.
$$
\text{Phonon} = \text{The quantum of vibrational energy at given} ~\omega _k
$$
<img src="/images/6. Crystal vibration - phonon/image-20240429155404445.png" alt="image-20240429155404445" style="zoom:67%;" />

---

#### 1D 'Diatomic chain'

<img src="/images/6. Crystal vibration - phonon/image-20240429160201872.png" alt="image-20240429160201872" style="zoom:67%;" />

다음과 같은 개념을 생각을 한후, 검은색 입자는 $y_n$, 하얀색 입자는 $x_n$​이라고 가정하자.

<img src="/images/6. Crystal vibration - phonon/image-20240430100335483.png" alt="image-20240430100335483" style="zoom:80%;" />
$$
\begin{align}
&\text{Steady State에서 다음과 같다.}
\\
&m \triangle \ddot{x}_n = \kappa_2(\triangle y_n - \triangle x_n) + \kappa_1 (\triangle y_{n-1} - \triangle x_n)
\\
&m \triangle \ddot{y}_n = \kappa_1(\triangle x_{n+1} - \triangle y_n) + \kappa_2 (\triangle x_{n} - \triangle y_n)
\\
&\text{이를 정리하면 다음과 같다.}
\\
\\
&m\omega^2 = (\kappa_1 + \kappa_2) ~\pm ~ \vert\kappa _1 + \kappa _2 e^{jka} \vert 
\\
&\therefore \omega _{\pm} = \sqrt{\frac{\kappa _1 + \kappa _ 2}{m}\pm\frac{1}{m}\sqrt{(\kappa _1 + \kappa _2 )^2 - 4 \kappa _1 \kappa _2 \sin^2(\frac{ka}{2})}}
\end{align}
$$
이를 통해 다음의 Dispersion relation을 나타낼 수 있다.

<img src="/images/6. Crystal vibration - phonon/image-20240430101114530.png" alt="image-20240430101114530" style="zoom:67%;" />
$$
\text{Low-energy branch}(\omega_{-}) &= \text{Acousitc phonon}
\\
\text{High-energy branch}(\omega_{+}) &= ~\text{Optical phonon}
$$
이것이 의미하는 사실은 다음과 같다.

<img src="/images/6. Crystal vibration - phonon/image-20240430101335926.png" alt="image-20240430101335926" style="zoom:67%;" />

Acoustic phonon은 k = 0 근처에서, linear dispersion을 갖는다. 

Optical phonon은 k = 0 근처에서 Momentum : $\frac{d \omega}{d k } = 0$을 갖는다. 이는 photon과 비슷한 의미를 갖는것을 의미한다. 따라서, photon의 흡수로만 가능하고 이를 optical phonon이라고 부른다.

