---
layout: single
title: "3)Carrier Action"
typora-root-url: ../
categories : "Fundamental-of-Semicondutor"
tag : carrier
#tag : [me, me2, me3]
toc : true
toc_sticky : true
author_profile : false
---
## Fundamental of semiconductor

수학적으로 정의되는 Carrier Action의 대한 방정식은 흔히 Continuity Equation으로 구성된다.

Continuity Equationd으로 표현하기 위해 여러 개념들을 이 단원에서 배우고 정의하려고 한다. 

주의해야할 점은 Carrier Action은 Thermal non-Equilibrium 상황에서 Thermal Equilibrium 상황을 만들기 위해 Carrier가 이동하는 현상을 의미한다.

equilitbrium 상황에서 전자들은 빛의 속드의 1/1000으로 움직이지만 Macroscopic 관점에서 보면 zero로 나타낸다. 따라서 우리는 Carrier를 하나의 개개인으로 보는 것이 아닌 Macroscopic 관점에서 볼 것이다.

---

#### Drift Current 

Drift Current의 개념을 배우기 전에 Current의 개념을 배워야한다. 

반도체에서 말하는 Current는 Volume Current Density를 의미한다. 

이는 다음으로 표시 된다. 
$$
J(Volume ~Current ~Density)=\frac{Current의 개념}{Volume}=\sum_i\frac{q_i\times v_i}{V}
$$
<img src="/images/3. Carrier Action/image-20230829095402323.png" alt="image-20230829095402323"  />

이를 머릿속으로 정성적으로 그림을 그릴 때는 임의의 부피 안에 charge에 대한 v벡터를 그려줄 수 있다.

이러한 개념으로 Current(I)는 정성적으로 임의의 부피를 면적에 대한 적분으로 생각 할 수 있다.

따라서 다음으로 표시 된다.
$$
I(Current) = \int J\cdot dA
$$

* 1. 조금 더 생각해보기

  J를 수열의 합의 개념이 아닌 parameter 값으로 정의 내리기 위해서는 어떻게 해야 할까?



​		전자는 Wavepacket으로 Group Velocity로 표현되는데 이의 평균의 개념으로 따라서 생각할 수 있다. 따라서 다음과 같이 표현된다.
$$
J(Volume Current Denisty) = (charge density)\times (average~of~Group ~velocity)=\rho \cdot v_{avg}
$$

* 2. 조금 더 생각해보기 

     Flux의 개념에 대해서 생각해볼 수 있다. 
     $$
     J(Volume ~number~ Density) = F(flux) = \sum_i\frac{v_i}{V}
     $$
     따라서, Flux란 Volume number density의 의미를 갖고 있는 것을 생각할 수 있다.





위의 개념으로 종합하면 다음으로 정리 된다. 
$$
J_{p\mid drift}=(charge ~density)\cdot(average~of~group~ velocity) = qpv_{avg}
$$

$$
J_{n\mid drift}=(charge ~density)\cdot(average~of~group~ velocity) = -qnv_{avg}
$$

보통 전자의 속도는 얼마나 될까? v = 10^6m/s = 1000km/s

전자의 속도는  아주 큰 전압 미만(1000V)에서는 전기장에 비례한다. 

따라서 다음으로 정리된다. 
$$
J_{p\mid drift}=qp\mu_pE
$$

$$
J_{n\mid drift}=qn\mu_n E
$$

이제 mobility의 개념에 대해서 살펴보자.
$$
\mu = mobility
$$
Mobility는 전기장과 속도에 대한 비례상수이다. Mobility는 어떻게 결정되어지는 걸까?

이를 정성적으로 생각하면 다음과  같다.

1. Ionized Impurity에 의해 영향을 받음.
2. Phonon(lattice vibration)에 의해 영향을 받음.

이제 정량적으로 생각해볼 시간이다.

mobility의 입장에서 충돌하기 까지의 평균 시간을 mean free time이라 한다. 

이는 다음으로서 표현할 수 있다. 
$$
(평균 충돌까지의 걸리는 시간확률)=\frac{dt}{<t>}
$$

$$
mobility = \frac{<t>}{m^*}
$$

Ionized impurity에 의해서도 생각해보자, 

Ionized impurity에 의한 상황은 Scattering이다. 

Scattering은 에너지 손실 없이 전자의 움직임(a general freedom movement of electron)이 ionized impurity에 의해 randomized direction을 갖는 것을 의미한다. 

전자의 속도는 thermal velocity이고 이는 온도가 올라갈수록 전자의 속도가 올라간다. 

따라서 정리하면 Ionized impurity가 mobilty에 영향을 미치는 변수는 다음과 같다.

1. 온도가 높을수록 scattering이 더 잘되어 ionized impurity 영향 커짐.
2. impurity 농도가 높을수록 ionized impurity 영향 커짐.

Phonon(Lattice Vibration)에 대해서도 생각해보자. 

온도가 커질수록 Lattice Vibration 영향 커짐. 



이를 모두 종합해 보면 다음과 같다.

mobility의 역수를 저항 이라고 생각할 수 있고 저항의 직렬 연결로 생각할 수 있다. 이를 정량적으로 나태보자.
$$
\frac{1}{<t_{total}>} = \frac{1}{<t_{ionized ~impurity}>}+\frac{1}{<t_{phonon}>}
$$
온도에 대해 더 생각해 볼 수 있다.

온도가 높아지면 두 측면에 대해서 모두 mobility가 안좋아진다. 

그러나 온도가 많이 높을 때는 phonon에 대한 영향력이 더 크다. 



마지막으로 Volume drfit current denstiy는 conductivity로 나타낼 수 있다. 
$$
(7에 ~따르면)~J_{p\mid drift}=qp\mu_pE
$$

$$
(8에 ~따르면)~J_{n\mid drift}=qp\mu_nE
$$

$$
(13과~14를~합치면)= J_{drift}=qp\mu_pE+qp\mu_nE=\sigma E
$$

따라서 전류의 mechanism이 drift라면,   Conductivity = (charge)X(number density)X(mobility)로 생각할 수 있다.



---

#### Diffusion Current

Diffusion Current를 배우기 전에 Energy Band의 Banding에 대해서 살펴보아야한다.

정성적으로 같은 물질에 대해먼저 생각해보자. 

전기장이 한쪽에 가해져 있는 상황을 생각해보자.

 이는 슈레딩거 방정식의 포텐셜 에너지에 에너지 적으로 constant E가 up-shift(평행이동) 되어있다고 생각할 수 있다. 

따라서, -의 전기장에 대한 에너지를 받는 곳 --> depletion region에서 시작하여

CB와 VB 모두 같은 에너지 만큼 upshift 되어있다.

Energy Band가 불연속적으로 연결될 이유는 없다. 

따라서, Band Bending이 일어난다. 



이제 이를 정량적으로 파악해보자. 

E(Total Electron Energy)는 편의상 E(electron potential Energy)를 선으로 그릴 수 있다. E = E_p + E_k로 나타낼 수 있다. (점)= (벡터)+(선)
$$
E_{{potential E}\mid electron} = - q\cdot V{(potential ~E)}
$$
따라서, V는 E를 뒤집은 형태이다. 

맥스웰 방정식에 의하면 다음과 같다. 
$$
\epsilon = -\triangledown \cdot V
$$


이를 (16)과 결합하면 다음과 같다.
$$
\epsilon = \frac{1}{q}\triangledown \cdot E
$$
맥스웰 방정식에 의하면 다음과 같다. 
$$
\triangledown \cdot \epsilon = \frac{\rho}{\epsilon_0}
$$


따라서 이를 (18)과 결합하면 다음과 같다. 
$$
\rho = \frac{\epsilon_0}{q}\frac{dE^2}{d^2x}
$$


Diffusion Current의 정확한 정의는 Random Thermal Vibration이다.

온도라는 개념은 항상 정의되기 때문에 Diffusion Current는 Thermal inequality가 있거나 number density inequality가 있는 상황에서 항상 생각해봐야한다. 

즉 Diffusion Current를 Flux의 개념으로 생각할 수 있다. Diffusion은 속도에 대한 개념보다는 농도차에 대한 개념으로 서술해야한다. 



속도는 어떠한 온도에서 재료마다 다른 값이므로, Diffusion coefficient로 표현이 된다.

따라서 다음으로 표현된다.
$$
\sum_i\frac{v_i}{V}=Flux = J_{p\mid diff}=-qD_p\triangledown p
\\J_{n\mid diff} = qD_n\triangledown n
$$
로 표현가능하다.

---

#### Einstein Relationship

가장 먼저 생각해야 할 점은 온도 T에 대해서 물질이 평형 상태에 있을 때, Fermi E는 공간에 대한 함수가 아니라는 것이다. 

즉, 상수의 값을 띤다. 이는 FermiE가 두 매질사이의 열전달 같은 통계학적인 Random action의 입자 전달 현상을 나타내는 크기로, Chemical potential 역할을 하고 이는 Net에서는 0으로 보이기 때문에 공간에 대한 함수가 아니다.



이를 식으로 정리하면 다음과 같은 Einstein Relationship을 갖는다. 
$$
\frac{D_N}{\mu_n}=\frac{kT}{q}
\\ \frac{D_p}{\mu_p}=\frac{kT}{q}
$$

* rhymed으로 외우자

사실 non-Equilibrium일 때도 성립하지만 생략한다.

- mobility가 크면 diffusion coefficient도 크다.

* 활용 가능성 : Mobility를 알고 있으면 Non-degenerate Semiconductor에서 Diffusion coefficient를 구할 수 있다.

---

#### Recombination-Generation

Recombination : 전자와 홀이 만나 사라지는 것

Generation : 전자와 홀이 생성되는 것 



Recombination와 Generation에 따라 추가적인 에너지가 방출되거나 흡수된다. 

따라서, 에너지의 출입을 따지는 것이 중요하고 운동량도 보존되어야한다.



Recombination 종류

Recombination

1. Band to Band Recombination ( 큰 에너지를 방출, 빛을 말함.)

   - Direct Semiconductor에서의 경우

     가시광선의 전자기파 : 2pi/500 nm, First-Brillouin zone pi/a = pi/1nm이므로 방출되는 전자기파의 운동량이 상당히 작다.

     따라서, First-Brilluoin zone에서 k의 변화가 거의 없는 상황에서 Recombination이 발생한다.

     

     InDirect Semiconductor에서의 경우

     전자의 k 값이 홀의 k 값보다 무척 크므로, k를 잃어버리면서 recombination을 한다. 따라서 빛과 phonon이 나온다.

     이는 phonon에게 전달된다. phonon은 어떻게 k를 받는지는 아직 알지 못하겠다, 그러나, 간격이 무척 작은 것은 예상할 수 있다.

2. R-G center Recombination

   - Lattice defect 또는 impurity에 의해 결합한다. 이 때, 열에너지를 방출한다.(에너지가 작기 때문)

3. Auger Recombination

   ​	- 전자와 전자가 충돌이 일어나고 충돌하면서 생기는 E차이는 photon으로 방출되는 것이 아닌 thermalize 된다.

Generation 종류

1. Band to Band Recombination ( 큰 에너지)

   열적 에너지 또는 빛을 흡수할 때 일어난다.

2. R-G center Recombination

   - 열적 에너지를 흡수할 때 ( 에너제가 작을 때) Lattice decfect 또는 impurity state 에 의해 결합한다. 

3. Carrier generation via impact ionization

   - 전기장이 강하게 걸린 경우에만 진행된다.

     이는 k 값이 중요하게 작용을 하는데, k값이 작을 경우에는 Scattering 혹은 impurity에 의해 작동하지 못한다.

     전자의 에너지 및 운동량을 잃어버리고 잃어버린 만큼 정공이 생성되며 ionization 된다.



대부분의 Recombination or Generation 진행 시 에너지 출입으로 대부분이 열의 형태로 나타나는 것을 알 수 있다.

따라서, 열의 관련된 것을 더 살펴볼 필요가 있다.



상황 : 

- Indirect Thermal Recombination-Generation ( R-G center에서 일어나는 것)

* Indirect Semiconductor 와는 다른 개념으로 생각해야 한다.
* Low-level injection 

Low Level injection이란 **주입된 minority carrier이 기존의 평형에서의 majority carrier보다 매우 적을 때를 의미한다. : 거의 모든 상황임.**
$$
\triangledown n << p_0
$$
 Minority Carrier Recombination 변화에 대해 다음과 같이 생각할 수 있다.
$$
\frac{\delta p}{\delta t }\mid_R = -c_pN_T p
$$
Minority Carrier는 Majoirty Carrier와 하려고 할 것이다. Indirect 상황이므로 채워진 R-G Center가 N_T와 같다고 하면,

Minority Carrier는 -N_T에 비례하고, -홀의 농도에 비례할 것이다.

Minority Carrier Generation 변화는 다음과 같이 생각할 수 있다.
$$
\frac{\delta p}{\delta t}\mid_G = c_p N_T p_0
$$
Minority Carrier Generation은 정성적으로 생각 하자면, n-type에서 Valence band 아래에 있는 전자가 Trap site로 에너지를 받고 전이되는 것을 의미한다. 

이는 Trap site에 빈방의 갯수와 비례하는데, 빈방의 갯수는 평형상태와 거의 같다고 생각하자. 따라서 평형상태를 생각해보면 된다.

equilibrium일 때의 G는 R 과 같으므로 
$$
\frac{\delta p}{\delta t }\mid _G =\frac{\delta p}{\delta t}\mid_{G_0}=-\frac{\delta p}{\delta t} \mid _{R_0} = c_p N_T p_0
$$


따라서 이를 더하면 다음과 같다.
$$
\frac{\delta p}{\delta t}\mid_{indirect~thermal~R-G} = -c_pN_T(p-p_0)=- \frac{\triangle p}{\tau_p}
\\\frac{\delta n}{\delta t}\mid_{indirect~thermal~R-G} = -c_nN_T(n-n_0)= - \frac{\triangle n}{\tau_n}
$$
이를 정성적으로 생각해보자. Trap site가 많으면 라이프타임이 짧다는 것을 의미한다. 이는, Si을 굉장히 불순물이 없게 제작하면, minority carrier의 lifetime이 굉장히 크다는 것을 의미한다.즉, 다이오드 처럼 스위칭 소자를 만들기 위해서는 lifetime이 짧아야한다.( 전류를 껐을 때 빠르게 꺼져야하므로.) 따라서 불순물을 도핑해야한다. 

---

#### Continuity Equation

$$
\frac{\delta n}{\delta t}=\frac{\delta n}{\delta t}\mid _{drift}+\frac{\delta n }{\delta t}\mid_{diff}+\frac{\delta n }{\delta t}\mid_{thermal~R-G}+\frac{\delta n}{\delta t}\mid_{other~processes~(light,~ etc.)}
\\
\frac{\delta p}{\delta t}=\frac{\delta p}{\delta t}\mid _{drift}+\frac{\delta p }{\delta t}\mid_{diff}+\frac{\delta p }{\delta t}\mid_{thermal~R-G}+\frac{\delta p}{\delta t}\mid_{other~processes~(light,~ etc.)}
$$

이를 다시 정리하면 다음과 같다.
$$
\frac{\delta n}{\delta t}=\frac{1}{q} \triangledown \cdot \mathbf{J_N}+\frac{\delta n }{\delta t}\mid_{thermal~R-G}+\frac{\delta n}{\delta t}\mid_{other~processes~(light,~ etc.)}
\\
\frac{\delta p}{\delta t}=-\frac{1}{q} \triangledown \cdot \mathbf{J_P}+\frac{\delta p }{\delta t}\mid_{thermal~R-G}+\frac{\delta p}{\delta t}\mid_{other~processes~(light,~ etc.)}
$$


Continuity Equation 식이 가장 중요한데, 이를 Miniority Carrier 입장에서 살펴보려고 한다.

왜냐하면, R-G recombination은 Minority Carrier 수의 밀접한 관련이 있기 때문인다.

가정 

1. 전기장은 0에 가깝다. ( Diffusion이 dominated 하다.)

2. equilibrium minority carrier concentration은 위치에 대한 값이 아니다. 
3. Low-Level injection이다.

이를 정리하면 다음과 같다. 
$$
\frac{\delta \triangle n_p}{\delta t} = D_n \frac{\delta^2 \triangle n_p}{\delta x^2}-\frac{\triangle n_p}{\tau_n}+G_L
\\
\frac{\delta \triangle p_n}{\delta t} = D_p \frac{\delta^2 \triangle p_n}{\delta x^2}-\frac{\triangle p_n}{\tau_p}+G_L
$$

---

#### Diffusion Lengths 

Generation이 없는 상황에서 Minority Carrier는 얼만큼 확산할까?
$$
L_N = \sqrt{D_N \tau_n}
$$
로 정의된다. 이는 다음과 같은 식에서 산출되었다.
$$
<x> = \frac{\int^{\infty}_{0} x\triangle n_p(x)dx}{\int ^{\infty}_{0} \triangle n_p(x)dx} = L_N
$$

---

#### Qusai-Fermi Level

$$
n \equiv n_i e^\frac{F_N - E_i}{kT}
\\
p \equiv n_i e^{-\frac{F_p - E_i}{kT}}
$$

Low injection 상황에서 Majority Carrier의 변화는 적고, Minority Carrier 변화는 많다.

따라서, **Majority Carrier의 Qusai-Fermi Level은 거의 그대로고, Minority Carrier의 Qusai-Fermi Level은 크게 변한다.**
$$
\begin{align}
\\
1.~ n&= n_i exp(F_N - E_i)(/kT)
)\\
p&=n_iexp(-)(F_P - E_i)(/kT)
\\
\therefore np&=n_i^2exp(F_N-F_P)(/kT) 
\\
&\text{qusai-Fermi level 변화에 따라} ~np\text{값이} ~n_i^2\text{보다 커지거나 작아진다.}
\\
\end{align}
$$


Qusai-Fermi Level 식을 통해 새롭게 Volume Current Density를 나타내려한다. 
$$
J_p = q \mu_p p\epsilon - qD_p\triangledown p
$$

$$
\triangledown p =(\frac{n_i}{kT})e^{\frac{E_i-F_p}{kT}}{(\triangledown E_i-\triangledown F_p)}=(\frac{qp}{kT})\epsilon-(\frac{p}{kT})\triangledown F_p
$$

이를 위에 대입하면 다음과 같다. 
$$
J_p = q\mu_pp\epsilon - qD_p[(\frac{qp}{kT})\epsilon -(\frac{p}{kT})\triangledown F_p]
\\
J_p = \mu_p p \triangledown F_p
$$


이를 전자와 정공에 대해 정리하면 다음과 같다.
$$
J_p = \mu_p p \triangledown F_p
\\
J_N = \mu_n n \triangledown F_N
$$

* 여기서 주의해야할 점은 Volume Current Density 식 안에 농도와 Quasi-Fermi Level 변화가 같이 있다는 것이다. 즉, 농도가 Qusai-Fermi Level 변화의 Scale 보다 크므로 이에 주의해야한다.
