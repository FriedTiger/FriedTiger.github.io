---
layout: single
title: "8) Transient Response"
typora-root-url: ../
categories : "Fundamental-of-Semicondutor"
tag : diode
#tag : [me, me2, me3]
toc : true
toc_sticky : true
author_profile : false
---
## Fundamental of semiconductor

전체 정리 : 

Small signal은 majority carrier , minority carrier를 분석하고

Transient response는 minority carrier를 분석한다.

**Minority Carrier를 채워 넣는데 오래 걸린다.**

---

#### Turn off transient

<img src="../friedtiger/friedtiger.github.io/images/8. pn Junction Diode Transient Response/image-20231220180750815.png" alt="image-20231220180750815" style="zoom:80%;" /><img src="../friedtiger/friedtiger.github.io/images/8. pn Junction Diode Transient Response/image-20231220181531193.png" alt="image-20231220181531193" style="zoom:80%;" />

<img src="../friedtiger/friedtiger.github.io/images/8. pn Junction Diode Transient Response/image-20231220185737096.png" alt="image-20231220185737096" />

해석)

1. $I_F$ 보다 $I_R$의 전류가 더 큰 이유는 다이오드 내의 minority carrier가 남아있기 때문이다. 

2. 0< t <$t_s$ 에서 $I_R$이 일정한 이유는 이 시간 동안 recombination rate보다 flow out of minority carrier의 양이 훨씬 많기 때문이다.

3. $t_s < t$ 에서 전류가 급격히 줄어드는 이유는 minority carrier가 급격히 줄어들어 $\frac{d \triangle p_n  }{dx} \vert_{x=x_n}$이 감소하기 때문이다. 

<img src="../friedtiger/friedtiger.github.io/images/8. pn Junction Diode Transient Response/image-20231220182713440.png" alt="image-20231220182713440" style="zoom:80%;" />

**정량적 분석**

책에는 나와있지 않지만 p+ -n 의 고농도 다이오드 (low level injection) 상황이라고 가정하자. 

Continuity equation에 따라 다음을 알 수 있다.
$$
\frac{dQ_p}{dt} = i - \frac{Q_p}{\tau _p}
$$
우리가 보려는 구간은 0<t<$t_s$ 이다.

따라서
$$
\begin{align}
\\
&\frac{dQ_p}{dt} = -(I_R + \frac{Q_p}{\tau _p})
\\
&\text{양변을 q와 t에 대해 적분하자.}
\\
&\int^{Q_p(t_s)}_{Q_p(0^+)}\frac{dQ_p}{I_R + Q_p /\tau _p} = - \int ^{t_s}_{0^+}dt = - t_s
\\
&\tau _p~ln[\frac{I_R + Q_P(0^+)/\tau _p}{I_R + Q_p(t_s)/\tau _p}] = - t_s
\\
&\text{보수적으로 일을 쉽게 접근하기 위해} ~Q_p(t_s)\text{는 0이라고 하자.}
\\
& \therefore \tau _p ln(1+\frac{I_F}{I_R}) = -t_s
\end{align}
$$
해석) 

1. $V_F$ 를 키우면 $\tau _s$가 커진다.
2. $V_R$를 키우면 $\tau_s$가 작아진다.
3. $ln(1 + \frac{I_F}{I_R}) = -\frac{t_s}{\tau _p}$ 의 관계식을 갖는다.

---

#### Turn on transient

turn on transient은 turn off transient와는 전류 전압 관점에서 다르게 해석할 수 있다.

상황을 쉽게 나타나기 위해 Current source를 가한 상황이다.

<img src="../friedtiger/friedtiger.github.io/images/8. pn Junction Diode Transient Response/image-20231220185807823.png" alt="image-20231220185807823" />

항상, 해석을 할 때, majority carrier와 minority carrier를 나누어서 생각해야한다. 

turn on 이 되는 순간 majority carrier는 이미 다 넘어가 버린 상황이므로 $I_F$가 흐른다.

turn on 이 되는 순간 majority carrier에 의해서 넘어간 minority carrier가 depletion region에 쌓이면서 $v_A$ 가 증가한다.

<img src="../friedtiger/friedtiger.github.io/images/8. pn Junction Diode Transient Response/image-20231220184323125.png" alt="image-20231220184323125" style="zoom:80%;" />

마찬가지로 continuity equation은 다음과 같다.
$$
\frac{dQ_p}{dt} = i - \frac{Q_p}{\tau _p}
$$
우리가 보려는 구간은 0<t 이다. 
$$
\begin{align}
\\
&\frac{dQ_p}{dt} = I_F - \frac{Q_p}{\tau _p}
\\
\end{align}
$$

$$
\begin{align}
\\
&t=0\text{일 때} ~~Q_p = 0\text{이라 가정하자.}
\\
&\int ^{Q_p(t)} _ 0 \frac{dQ_p}{I_f - Q_p / \tau _ p} = \int ^{t} _0 dt = t
\\
&t = -\tau _p ln(I_F - \frac{Q_p}{\tau _p}) \Big|^{Q_p(t)} _0 = -\tau _p ln[1- \frac{Q_p(t)}{I_F \tau _p}]
\\
&\text{이를 정리하면 다음과 같다.}
\\
&Q_p(t) = I_F \tau _p (1-e^{-t/\tau _p})
\\
&\text{우리가 알고 싶은 것은 } V_A (t) 이다.
\\
&Q_p =I_{\text{DIFF}}~\tau_p = I_0 \tau _p(e^{qV_a / kT}-1) : \text{in steady state}
\\
&\text{따라서, 이를 식(17)과 식(19)를 정리하면 다음과 같다.}
\\
&V_A(t) = \frac{kT}{q}ln\Big[1+ \frac{I_F}{I_0}(1 - e^{-t/\tau_p}) \Big]
\end{align}
$$
