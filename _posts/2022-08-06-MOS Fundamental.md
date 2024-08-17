---
layout: single
title: "16)MOS Fundamental"
typora-root-url: ../
categories : "Fundamental-of-Semicondutor"
tag : diode
#tag : [me, me2, me3]
toc : true
toc_sticky : true
author_profile : false
---
## Fundamental of semiconductor

Ideal MOS는 다음을 따른다.

1. Metallic gate는 충분히 두껍다.
2. Oxide는 완벽한 Insulator이다.
3. Oxide와 Oxide-Semiconductor interface는 어떠한 charge center가 없다. 따라서, Oxide의 전기장은 일정하다.
4. $\Phi_M$ 와 $\Phi_S$ 는 같다고 가정하자.

----

쉽게 설명하기 위하여 Block charge diagram을 생각하자.

1) **Metal에 Forward Bias를 걸었을 때**

<img src="/images/figure/image-20221227010138599.png" alt="image-20221227010138599" style="zoom:80%;" />

- Metal 에 손잡이가 달렸다고 가정하고, 아래로 끌어내리자

- 1) Fermi Level allign을 시켜야하지만 charge가 넘어갈 수 없으므로 불가능하다.
  2) Vaccum level shift를 시켜줘야한다. Vaccum level은 항상 연속이므로 연속적으로 그려준다.
  3) Vaccum level은 한번 미분한 상황(전기장)을 보면 불연속인 것을 알 수 있다.  따라서, 전기장에 대한 미분은 delta function인 것을 알 수 있다.
  4) 따라서, 계면에 charge가 존재한다는 것을 알 수 있다.

  

2. **Metal에 Backward Bias를 걸었을 때**

<img src="/images/figure/image-20221227010247282.png" alt="image-20221227010247282" style="zoom:80%;" />

- n-type에서 $N_D^+$ 가 depletion region으로 width를 가진다.



3. **Metal에 더 큰 Backward Bias를 걸었을 때**

<img src="/images/figure/image-20221227010404560.png" alt="image-20221227010404560" style="zoom:80%;" />

만약, Depletion region이 계속 넓어지다 보면, Band Bending이 더 심해질 것이다.

Band Bending이 심해짐에 따라
$$
E_{\text{surface}} - E_F = E_F - E_{0,\text{bulk}}
$$
를 만족시키는 $V_G$가 발생한다. 이를 $V_{\text{threshold}}$라 하고, Onset of inversion이라 명명한다.

Inversion이 Onset되면 depletion region은 더이상 넓어지지 않고 generation hole들이 accumulation 된다.

---

#### Quantitative analysis

$$
\begin{align}
\\
&\phi(x) = \frac{1}{q}\left[E_i (bulk) - E_i(x)\right], \text{즉 } \phi\text{는 band bending과 관련된 식. Vacuum level shift를 의미}
\\
&\phi_S = \frac{1}{q}\left[E_i (bulk) - E_i(surface)\right] \text{~surface에 charge가 얼만큼 있어서 vacuum level shift가 일어났냐.}
\\
&\phi_F = \frac{1}{q}\left[E_i (bulk) - E_F\right] \text{~ Doping이 얼만큼 되어있나}
\\
\end{align}
$$

즉 아래 그림에서 이를 다시 확인할 수 있다.

<img src="/images/16. MOS Fundamentals/image-20240103094201614.png" alt="image-20240103094201614" style="zoom:80%;" />



따라서 이를 도핑 농도에 따라 표현하면 다음과 같다.
$$
\phi_F = ~~~ \frac{kT}{q}ln(N_A / n_i) \text{ in p-type semiconductor}
\\
\phi_F =  -\frac{kT}{q}ln(N_A / n_i) \text{ in n-type semiconductor}
$$
식들의 정리를 통해 Inversion의 Onset이 되는 시작점은 다음과 같다.
$$
\begin{align}
&\phi_S = 2 \phi _F \text{ ~ at the depletion-inversion transition point}
\\
&\phi_S \geq 2\phi_F \text{일 때 inversion이 시작된다.}
\\
&\text{Inversion의 실질적 의미 : MOSFET에 적용하기 위하여 inversion을 정의내림}
\end{align}
$$
이를 Accumulation(정전압) --> Depletion(역전압) --> Inversion(역전압)에서의 charge distribution을 다음 그림으로 나타낼 수 있다.

1) Accumulation (정전압). $\phi _S < 0$ in p-type semiconductor

<img src="/images/figure/image-20221227014247138.png" alt="image-20221227014247138" style="zoom:67%;" />

2. Depletion & onset of inversion (역전압) $0<\phi _S < 2 \phi _F$ in p-type semiconductor

    					<img src="/images/16. MOS Fundamentals/image-20221227014310867.png" alt="image-20221227014310867" style="zoom:80%;" /> 					<img src="/images/figure/image-20221227014359840.png" alt="image-20221227014359840" style="zoom:67%;" /> 

3. heavily Inversion(역전압) $\phi _S > 2 \phi _F$

   <img src="/images/figure/image-20221227014422299.png" alt="image-20221227014422299" style="zoom:67%;" />

3번째 그림에서 depletion inversion이 시작된다. minority carrier의 inversion을 $\delta$-function으로 나타낸다고 생각하자.

depletion inversion 시작 점에서는 $N_A ^{-}$ 와 surface에서의 minority carrier가 같은 농도를 갖는다는 것을 알 수 있다. 



Block Charge Diagrams을 통한 Stand depletion approximation을 가정하여 식을 전개해보자.
$$
\frac{dE}{dx} = \frac{\rho}{K_S \epsilon _0} = -\frac{qN_A ^ -}{K_S \epsilon _0} ~~~(0 \leq x \leq W)
\\
E(x) = \frac{qN_A ^ -}{K_S \epsilon _0} (W-x)
\\
\phi(x) = \frac{qN_A ^ -}{2K_S \epsilon _0}(W-x)^2
$$
즉, W(Depletion width)와 $\phi_S$ 가 서로 얽혀있다는 것을 알 수 있다.
$$
\phi_S = \frac{qN_A}{2K_S \epsilon _0}W^2
\\
W = \left[\frac{2K_S \epsilon _0}{qN_A} \phi_s\right]^{1/2}
$$
<img src="/images/16. MOS Fundamentals/image-20240103101925849.png" alt="image-20240103101925849" style="zoom:80%;" />

---

#### Gate Voltage Relationship

$$
\begin{align}
&V_G = \triangle \phi_{semi} + \triangle \phi_{ox} 
\\
&\text{전압과 관련된 것은 Qusai-Fermi Level이고, 이는 다시 Vacuum level shift에 영향을 미친다.}
\\
&\text{따라서, semiconductor와 oxdie가 전압을 소비한다는 것을 의미한다.}
\end{align}
$$
전압에 대해서 미분방정식을 푼다는 것은 Boundary Condition을 통해 풀 수 있다. 이 때, 전자기학에서 배운 $\vec{D_1} -\vec{D_2} = \rho_{free}$ 식이 사용된다.

계면에 $\rho_{free}$가 없는 상황이므로 $\vec{D_1} = \vec{D_2}$ 이다. 즉, $\frac{\vec{E}_{\text{ox}}}{\epsilon _{\text{ox}}} = \frac{\vec{E}_{\text{semi}}}{\epsilon _{\text{semi}}}$ 

<img src="/images/16. MOS Fundamentals/image-20240103142026786.png" alt="image-20240103142026786" style="zoom:67%;" />
$$
\begin{align}
&\text{Exact Solution} : delta-depletion solution
\\
&V_G = \triangle \phi_{ox} +\triangle \phi_{semi}   = t_o \frac{K_S}{K_O}E_s + \triangle \phi_{semi} =\frac{K_S}{K_O}t_o \sqrt{\frac{2qN_A}{K_S \epsilon _0}\phi_s} + \phi_s ~~( 0 \leq \phi _S \leq 2 \phi _F)
\\
&\text{Voltage가 oxide가 더 많이 먹네. 이를 그래프로 표현하면 다음과 같다.}
\\
\end{align}
$$

<img src="/images/16. MOS Fundamentals/image-20240103160714343.png" alt="image-20240103160714343" style="zoom:67%;" />


---

#### C-V Measurement

<img src="/images/figure/image-20221227082609717.png" alt="image-20221227082609717" style="zoom:80%;" />

(a) $V_G > 0$ Majority Carrier의 Accumulation
$$
\begin{align}
&C = C_{oxi} = K_{oxi} ~\epsilon_o \frac{A}{t_{oxi}} = \text{constant}
\end{align}
$$


(b) $V_G < 0$ Majority Carrier의 Depletion
$$
\begin{align}
&\text{Capacitance가 직렬로 연결이 될 때}
\\
&Y = G +iwC\text{이므로}
\\
&\text{저항으로 생각하였을 때} \frac{1}{C} = \frac{1}{C_{Oxi}} + \frac{1}{C_{semi}}
\end{align}
$$

따라서, $C_{Oxi}$와 $C_{semi}$로 나누어서 생각해봐야한다.
$$
\begin{align}
&C_{oxi} = \frac{K_O \epsilon _ 0 A_G}{x_0} = \text{constant}
\\
&C_\text{S} = \frac{K_S \epsilon _0 A_G}{W} = \text{depend on width} 
\end{align}
$$
$\triangle V_{A.C}$ 에 따라 width가 바뀐다. $V_G$ 가 커짐에 따라 $W$ 가 넓어진다. 따라서, $C_S$가 감소하여 $C$가 감소한다.



(c) Low frequency, $V_G < V_T$ inversion 일때

minority carriers가 generated 되거나 annihilated 되는데에 시간이 걸린다. 예상 : $\frac{1}{\tau_{\text{lifetime}}}$

minority carriers는 delta function 형태로 존재하기 때문에 depletion에 비해 width가 줄고, $W = x_0$ 형태로 일정하게 된다.

따라서 C가 증가하다가 일정해진다.



(d) High frequency, $V_G < V_T$ inversion 일때 

high frequency에서는 Minority Carrier가 generation or annihilated되지 못한다. 

Majority Carrier가 옆으로 움직이면서 W가 커진다. 즉, C가 작아진다 그러나, W가 크게 변하지 않으므로 거의 일정하다.  



(a)(b)(c)(d)를 종합하면 다음의 그래프를 얻을 수 있다.

<img src="/images/figure/image-20221227084400213.png" alt="image-20221227084400213" style="zoom:80%;" />

다음의 상황에 대해서 살펴보자

<img src="/images/figure/image-20221227091341270.png" alt="image-20221227091341270" style="zoom:80%;" />

Majority Carrier가 Capacitance에 영향을 미치는 상황이다.

Inversion 되기 위한 $V_G$(빨간점) 를 살펴보자. 

$E_i -E_F$ 가 큰 상황에서 Inversion 되기 위한 $V_G$ 가 커진다. 

따라서, 위에 있는 그래프가 도핑이 더 큰 소자이다.



또 다른 상황을 살펴보자.

<img src="/images/figure/image-20221227092017327.png" alt="image-20221227092017327" style="zoom:67%;" />

oxide 두께를 바꾼 상황이고, low frequency & High frequency 상황이다.

이다. Oxide에서 전압을 소비하므로, $V_G$가 크다는 것은 Oxide가 두꺼워 Semiconductor에서 소비되는 전압이 작다는 것을 의미한다. 

따라서 oxide 두께가 두꺼울 때 $V_G$ 가 크다.

---

#### Practical Observations

$V_G$ 를 sweep하는 속도도 중요하다.

$V_G$를 sweep 하면서 Majority Carrier의 움직임 및 Minority Carrier의 생성 소멸이 변함에 따라 depletion region이 점차 증가해야하는데 

sweep 해버리면 Minority Carrier가 이를 따라가지 못하고 Majority Carrier가 반응해버린다.

따라서, width가 더 커지고 Capacitance가 작아진다.

즉, sweep rate(scan rate), amplitude, frequency 모두 중요하다.
