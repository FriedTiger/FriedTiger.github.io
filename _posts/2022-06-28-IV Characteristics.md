---
layout: single
title: "6)IV Characteristics"
typora-root-url: ../
categories : "Fundamental-of-Semicondutor"
tag : diode
#tag : [me, me2, me3]
toc : true
toc_sticky : true
author_profile : false
---
## Fundamental of semiconductor

먼저 알아야 할 것은 다음과 같다.

1. 금속은 hole이 없다. 
2. 도핑되어있는 반도체는 약한 금속( 전자의 바다 or 홀의 바다)이라고 생각하면  편하다.

#### Ideal Diode

1. p-n diode depletion 내에서 G-R이 없다고 가정하자.
2. Low-level Injection 으로 가정하자.
3. depletion region이 아닌 영역에서는 전기장이 0 으로 가정하자.

---

#### Qualitative Derivation

#### Non-bias 에서의 depletion region

<img src="/images/figure/image-20221225124752770.png" alt="image-20221225124752770" style="zoom:70%;" />

drift 전류와 diffusion 전류가 평형을 이룬다. 

#### Positive-bias 에서의 depletion region

<img src="/images/figure/image-20221225125127439.png" alt="image-20221225125127439" style="zoom:70%;" />

n-형에서 major carrier의 농도가 높아져 diffusion 전류가 우세하게 된다. 

#### Reverse-bias 에서의 depletion region

<img src="/images/figure/image-20221225125333340.png" alt="image-20221225125333340" style="zoom:70%;" />

diffusion carrier에 의한 전류가 없어지고 drift 만 존재하게 된다. 

이때, drift 전류는 minor carrier 이기 때문에 generation을 통해서만 만들어진다. 

따라서, 전압에 관계 없이 일정한 전류가 흐른다.  이를 전체 diagram으로 확인하면 다음과 같다. 

<img src="/images/figure/image-20221225125733771.png" alt="image-20221225125733771" style="zoom:80%;" /> 

---

#### Quantitative Derivation

step junction으로 구성되어 있다고 가정하자. 

<img src="/images/figure/image-20221225154156314.png" alt="image-20221225154156314" style="zoom:80%;" />

Quasi-neutral region에서는 다음과 같이 continuity equation을 표시할 수 있다 .
$$
\text{Continuity equation of Minority Carrier}
\\
0 = D_N \frac{d^2 \triangle n_p}{dx^2} - \frac{\triangle n _p}{\tau _n}
\\
0 = D_p \frac{d^2 \triangle p_n}{dx^2} - \frac{\triangle p _n}{\tau _p}
$$
Quasi-neutral region에서 위의 식을 통해 current density를 구할 수 있다.
$$
\text{Current Density of Minority Carrier}
\\
J_N = qD_N\frac{d \triangle n_p}{dx}
\\
J_P =-qd_P\frac{d \triangle p_n}{dx}
$$
Depletion region에서는 다음과 같이 continuity equation을 표시할 수 있다. 
$$
\text{Continuity equation of Carrier}
\\
0 = \frac{1}{q}\frac{dJ_N}{dx}
\\
0 = -\frac{1}{q}\frac{dJ_P}{dx}
$$
위 식을 통해 일정한 $J_N$ 과 $J_P$이 일정한 값을 갖는 다는 것을 알 수 있고 다음과 같이 current density를 구할 수 있다.
$$
J = J_N(-x_p) + J_p(x_n)
$$


식을 모두 구했으므로 B.C를 설정해야한다.

Quasi-neutral region이 diffusion length보다 충분히 길다고 가정하자.
$$
\triangle n_p ( x \rightarrow - \infty) = 0
\\
\triangle p_n ( x \rightarrow \infty) = 0
$$
이를 통해 결과를 구해보면 다음과 같다. 

1. Depletion region 에서의 carrier concentration
   $$
   np = n^2 _i e^{(F_N - F_P)/kT}
   $$

2. **Law of the junction**

   1) $F_N - F_P \leq E_{Fn} - E_{Fp} = qV_A $ 라 가정하자. :  Quasi -Fermi E가 monotonic 하게 감소한다고 가정
   2) $F_N - F_P = E_{Fn} - E_{Fp} = qV_A $이 depletion region에서 성립한다고 가정 

   $$
   np = n^2 _i e ^{qV_A / kT} : \bold{\text{Law of the junction}}
   $$

    

   <img src="/images/figure/image-20221225160653823.png" alt="image-20221225160653823" style="zoom:67%;" />

3. Minority Carrier concentration
   $$
   \text{Depletion Region}
   \\n(-x_p) = \frac{ n^2 _i}{N_A}e^{qV_A /kT}
   \\
   \underline{\triangle n_p(-x_p) = \frac{ n^2 _i}{N_A} (e^{qV_A /kT} - 1)}
   \\
   p(x_n) = \frac{n^2 _i}{N_D}e^{qV_A /kT}
   \\
   \underline{\triangle p_n(x_n) = \frac{n^2 _i}{N_D}(e^{qV_A /kT}-1)}
   \\
   \\
   \text{Quasi-neutral Region}
   \\
   \triangle p_n(x^{'}) = \frac{ n^2 _i}{N_D} (e^{qV_A /kT} - 1)e^{-x^{'}/L_P}
   \\
   \triangle n_p(x^{'}) = \frac{ n^2 _i}{N_A} (e^{qV_A /kT} - 1)e^{-x^{'}/L_N}
   $$
   이를 통해 이름 그래프로 그려보면 다음과 같다.

   Forward- Bias

   <img src="/images/figure/image-20221225173845344.png" alt="image-20221225173845344" style="zoom:80%;" />

   해석 

   1) Quasi- region에서 $np = n_i^2 exp^{V_a / kT} $ 이므로 위 그래프에서는 log scale에서 n+p가 일정하다.
   2) majority carrier가 넘어가 minority carrier가 되는데 exp함수를 띠고 depletion region 경계면 부터 쌓이면서 없어진다고 해석할 수 있다. 따라서 일종의 Capacitor 역할을 한다. 

   

   Reverse-Bias

   <img src="/images/figure/image-20221225174232944.png" alt="image-20221225174232944" style="zoom:80%;" />

   해석

   1. 위의 식에 따라 Reverse-Bias에서 minority carrier의 농도는 depletion 경계면에서 0에 가까워진다.(전류가 거의 안흐름)
   2. 경계면에서 minority carrier 양은 generation 으로 생성되는데, 이는 majority carrier의 변화에 영향을 받는다. majority carrier의 변화가 거의 없기 때문에 minority carrier양의 generation 값은 거의 없다.

4. Current Density 

   <img src="/images/figure/image-20221225161455016.png" alt="image-20221225161455016" style="zoom:80%;" />

$J_p$ 가 exponential 하게 $ x \geq x_n$ 에서 줄어드는데, 이는 minority carrier하게  exponential하게 감소하기 때문이다.

이에 따라 majority carrier를 공급해줘야 하고 $J_N$ 는 exponential 하게 증가한다.

이를 식으로 표현하면 다음과 같다. 
$$
\text{Quasi-neutral Region}
\\
J_P(x^{'}) = -qD_P \frac{d \triangle p_n}{dx^{'}} = q \frac{D_p}{L_P} \frac{n^2 _i}{N_D}(e^{qV_A / kT}-1) e^{-x^{'}/L_P}
\\
J_N(x^{'}) = -qD_N \frac{d \triangle n_p}{dx^{'}} = q \frac{D_n}{L_n} \frac{n^2 _i}{N_A}(e^{qV_A / kT}-1) e^{-x^{'}/L_N}
\\
\\
Current 
\\
I = A J = qA(\frac{D_N}{L_N}\frac{n_i ^2}{N_A}+ \frac{D_p}{L_p}\frac{n^2 _i}{N_D})(e^{qV_A /kT} -1)
\\
=I_0(e^{qV_A /kT} -1)
\\
I_0 = qA(\frac{D_N}{L_N}\frac{n_i ^2}{N_A}+ \frac{D_p}{L_p}\frac{n^2 _i}{N_D})
$$

---

#### Real Diode

Reverse Diode에서 부터 차근차근 살펴보자. 

***1-1. Avalanching Process***

<img src="/images/figure/image-20221225222023574.png" alt="image-20221225222023574" style="zoom:60%;" />

Breakdown 이하의 Voltage에서 발생할 수 있다. depletion region에서 atom 들이 존재한다. ( ionization atom 들이 존재하는 것이 아님)

depletion region을 전자가 지나면서 atom과 충돌하게 되는데, 이때 충분한 $E_k$를 갖는 전자라면 atom을 ionization시키면서 electron-hole pair가 발생한다.  

$V_{BR}$ 이 시작되는 지점을 정량적으로 구해볼 수 있다. E-x 그래프에 의해 전기장이 가장 큰 곳은 E(x=0)인 곳이다. 

따라서 다음과 같이 표현가능하다.
$$
E(x=0) - \frac{qN_D}{K_S \epsilon_0}x_n = - [\frac{2q}{K_s \epsilon _0}\left(\frac{N_A N_D}{N_A + N_D} V_{BR}\right)]
\\
E(x = 0 ) \rightarrow E_{CR}, V_{Bi}+V_{BR} \rightarrow V_{BR} \text{라 가정할 수 있다.}
\\
E_{BR} \text{은 도핑 농도와 무관하므로}
\\
V_{BR} \propto \frac{N_A + N_D}{N_A N_D} 
\\
\text{따라서 도핑이 적은 dopant의 역수에 비례한다.}
\\
\therefore V_{BR} \propto \frac{1}{N_B}
$$
***1-2. Zener Process***

양자역학적 tunneling 현상에 의해 발생한다. 다이오드 내에서 tunneling 현상이 발생하기 위해서는 다음과 같은 조건이 필요하다.

1. 같은 E에 대해 한쪽은 filled states, 한쪽은 empty states가 형성되어 있어야한다.
2. potential energy barrier의 너비인 d가 반드시 얇아야 한다. $d < 100 \dot{A} = 10nm$

<img src="/images/figure/image-20221226010811237.png" alt="image-20221226010811237" style="zoom:67%;" />

Reverse Bias 일 때 depletion region이 늘어난다. 그러나, 여기서 고려해야 할 것은 depletion region이 아닌 Filled states와 Empty States의 너비이다.  이러한 너비가 발생하기 위해서는 양쪽이 higly doped인 상황에서 발생한다. 



Avalanching Process와 Zener Process는 온도에 따라 구분할 수 있다. 

Avalanching Process 는 온도가 높아짐에 따라 Scattering이 더 자주 발생하여 $V_{BR}$ 이 더 커진다.

Zener Process는 온도가 높아짐에 따라 밴드갭이 줄어들어 $V_{BR}$이 작아진다.



***2. Recombination-Generation Process***

R-G process에 의해 추가적인 current가 발생한다.

<img src="/images/figure/image-20221226012948630.png" alt="image-20221226012948630" />



Reverse Bias에서는 depletion region이 bias가 클수록 넓어진다. 

따라서, Reverse Bias에서 Bias에 따라 점점 Generation Process가 증가할 것이다.

<img src="/images/figure/image-20221226013136462.png" alt="image-20221226013136462" />

Forward Bias에서는 Recombination Process에 의해 Bias에 따라 점점 증가한다.

따라서, Reverse Bias와 마찬가지로 전류가 증가한다. 이때, log scale의 $q/2kT$ 의 기울기를 갖는다.



일반적으로 R-G process가 다음과 같은 식으로 알려져있다.

<img src="/images/figure/image-20221226012249386.png" alt="image-20221226012249386" />

따라서 적분을 통해 다음의 식을 알 수 있다.
$$
\text{Reverse Bias :} I_{R-G} = -\frac{qAn_i}{2\tau _0}W 
\\
\text{Forward Bias :} I_{R-G} = \frac{qAn_i}{2 \tau_0}W\frac{(e^{qV_A /kT} -1)}{(1+ \frac{V_{bi}-V_A}{kT/q}\frac{\sqrt{\tau _n \tau_p}}{2 \tau_0}e^{qV_A /2kT})}
$$
보통은 $I = I_{DIFF} + I_{RG}$ 로 보정을 해준다.



***3.High Level Injection***

<img src="/images/figure/image-20221226014502027.png" alt="image-20221226014502027" />

minority carrier concentration이 majority carrier concentration을 넘는 상황이 발생한다.

High Level Injection의 log scale에서의 기울기는 $q/2kT$로 알려져있다.

***4. Series Resistance***

<img src="/images/figure/image-20221226014545479.png" alt="v" />

$V=IR$ 에서 $R$이 작기 때문에 V를 무시할 수 있었지만 $I$가 커짐에 따라 $V$를 무시할 수 없게 되었다.

따라서 다음과 같이 보정해주면 된다.
$$
V_A - IR_{Series} = V_J
$$
이를 모두 정리하면 다음과 같다.

<img src="/images/figure/image-20221226015155861.png" alt="image-20221226015155861" />

---

#### Charge Control Approach

<img src="/images/figure/image-20221225173845344.png" alt="image-20221225173845344" style="zoom:80%;" />

위의 식에서 빗금친 부분이 Q를 의미한다. 이 때, 빗금친 부분은 시간과 공간에 따라 변한다. 이를 $x>x_n$인 n형에서 살펴보자 .
$$
Q_P = qA \int^ \infty _{x_n} \triangle p_n(x,t) dx
$$
앞서 구한 Continuity Equation과 Current Density 식은 다음과 같으므로 연립할 수 있다.
$$
\frac{\delta \triangle p_n}{\delta t} = D_p \frac{\delta ^2 \triangle p_n}{\delta x^2} - \frac{\triangle p_n}{\tau _p}
\\
J_P = -qD_P \frac{\delta \triangle P_n}{\delta x}
\\
\therefore \frac{\delta (q\triangle p_n)}{\delta t} = - \frac{\delta J_p}{\delta x} - \frac{q \triangle p_n}{\tau _p}
$$
이를 적분하면 최종적으로 다음의 식을 얻을 수 있다. 
$$
\frac{dQ_p}{dt} = i_{Diff} - \frac{Q_p}{\tau _p}
$$
만약 state state라면, 
$$
I_{Diff} = \frac{Q_P}{\tau _p}
$$
다음과 같은 그림의 근사로 $Q_P$를 얻을 수 있다.

<img src="/images/figure/image-20221226141958989.png" alt="image-20221226141958989" style="zoom:67%;" />
$$
Q_p \approx q (AL_p) \triangle p_n(x^{'} = 0) = qAL_P\frac{n^2 _i}{N_D}(e^{qV_A /kT}-1)
\\
I_{Diff} = \frac{Q_p}{\tau _p}= qA\frac{L_p}{\tau _p}\frac{n^2 _i}{N_D}(e^{qV_A /kT}-1)
$$

---

#### Narrow-Base Diode

Diode가 Diffusion Length보다 짧은 상황을 생각해보자.
$$
\triangle p_n(x') = A_1 e^{-x^{'}/L_P}+A_2e^{x^{'}/L_P} \text{에서} A_2\text{는 0이 아니다.} 
$$
이를 정리하면 다음과 같다.
$$
\triangle p_n(x^{'}) = \triangle p_n(0)\frac{sinh[(x^{'}_c - x^{'})/L_p]}{sinh[x^{'}_c / L_P]}
$$
만약, diode의 길이가 엄청 작다면 다음과 같이 그래프를 그릴 수 있다.

<img src="/images/figure/image-20221226142808215.png" alt="image-20221226142808215" style="zoom:50%;" />

즉, input과 ouput이 동일하다는 것이고 Recombination-Generation은 발생하지 않는다. 

이럴 경우에는 exponential한 그래프가 아닌 linerar한 기울기를 갖는 그래프가 나타난다.
