---
layout: single
title: "18)Nonideal MOS"
typora-root-url: ../
categories : "Fundamental-of-Semicondutor"
tag : MOSFET
#tag : [me, me2, me3]
toc : true
toc_sticky : true
author_profile : false
---
## Fundamental of semiconductor

Ideal MOS에서는 Metal의 $\Phi_M$과 Oxide의 $\Phi_{OX}$ 가 같다고 여겨졌다. 

그러나, 실제로 Workfunction이 같을 이유가 없기 때문에 같지 않을 때의 상황을 알아봐야한다.

1<img src="/images/figure/image-20221227115225477.png" alt="image-20221227115225477" style="zoom:80%;" />                   <img src="/images/figure/image-20221227115238807.png" alt="image-20221227115238807" />

1. Work function이 다른 Metal 과 Semiconductor가 존재한다.
2. Metal과 Semiconductor를 전선으로 연결한다.
3. Carrier가 전선을 따라 이동하고 이에 따라 Vaccuum level이 shift 한다.
4. Metal과 Semiconductor 사이에 oxide를 붙인다.

---

#### 1. Gate Voltage with Fermi Level align

따라서 먼저 위에 접합 상황에 대한 식을 만들어줘야한다. 

<img src="/images/18. Non Ideal MOS/image-20240118102600402.png" alt="image-20240118102600402" style="zoom:80%;" />

참고 : $\phi$ 는 Band Bending과 등 전위 차에 대한 용어

이를 토대로 다음의 식을 알 수 있다.
$$
\begin{align}
\\
&\text{Metal Side = Semiconductor Side}
\\
&\Phi^{'}_M + q\triangle \phi_{ox} = (E_c - E_F)_{flat} - q\phi_S + \chi^{'}
\\
\\
&\text{우리가 구하려고 하는 것은 Build in potential이다.}
\\
&V_{bi} = -(\triangle \phi_{ox} + \phi_s) = \frac{1}{q}[ \Phi^{'}_{M} - \chi^{'} - (E_c - E_F)_{flat} ] \approx \frac{1}{q}[ \Phi_{M} - \chi - (E_c - E_F)_{flat} ]
\\
&\text{따라서, } ~\Phi_{M} - \chi\text{는 물질에 대한 값이고} ~(E_c - E_F)_{flat}\text{는 doping에 대한 값이다,}
\\
&\therefore V_{bi} \approx \frac{1}{q}[ \Phi_{M} - \chi - (E_c - E_F)_{flat} ] = \frac{1}{q}[\Phi_{M} - \Phi_{Semi}] = \phi_{MS}
\\
\\
&\therefore V_{bi} = \phi_{MS}
\end{align}
$$


결론적으로 Nonideal MOS에서 Ideal MOS처럼 생각하기 위해서 $V_{Bi}$ 만큼 $V_{G}$ 필요로 한다.

이는 Metal과 Semiconductor workfunction 차이에 읜한 것이다.
$$
\triangle V_G = (V_G - V_G^{'} )=V_{bi} = \phi_{MS}
$$


이는 C-V Measurement에서는  평행이동으로 생각하면 좋다.

<img src="/images/figure/image-20221227122945535.png" alt="image-20221227122945535" style="zoom:80%;" />

---

#### 2. Quantitative charges in oxide

<img src="/images/figure/image-20221227123241712.png" alt="image-20221227123241712" style="zoom:80%;" />

실제로는 위의 그림과 같이 Oxide 내부에 수많은 charge들이 존재하여 Ideal MOS와 다른 양상을 갖는다.

Oxide 내부의 charge가 존재하여 Poission equation을 구성하고 Boundary condition은 다음의 상황을 생각해야한다.

* interface trap도 고려해야하므로 $0\leq x \leq x_0 $의 정의역을 생각할 수 있다.

<img src="/images/18. Non Ideal MOS/image-20240118221306437.png" alt="image-20240118221306437" style="zoom:50%;" />
$$
\begin{align}
&\text{Poission equation in oxide :}
\\
&\frac{E_{ox}}{dx} = \frac{\rho _{ox}(x)}{K_{ox} \epsilon _0}
\\
\\
&\text{Boundary condition :}
\\
&\text{상미분방정식이므로 1개만 필요하다.}~ E(x=x_0) = E_{x_0}
\\
\\
&\text{x에 대해 적분하면 다음과 같다.}
\\
&E_{x_0} -E_{x} = \frac{1}{K_{ox}\epsilon _0}\int^{x_0}_x \rho_{ox}dx'
\\
&\text{x에 대해} 0 \to x_0\text{까지 적분하면 다음과 같다.}
\\
&x_0E_{x_0} - \triangle\phi_{ox} = \frac{1}{K_{ox}\epsilon _0}\int^{x_0}_{0} \int^{x_0}_x \rho_{ox}dx'dx
\\
\\
&\text{부분적분 공식을 쓰면 다음과 같다.}
\\
&\text{Let} \int^{x_0}_x \rho_{ox}dx' = f(x)
\\
&x_0E_{x_0} - \triangle\phi_{ox} = \frac{1}{K_{ox}\epsilon _0}\int^{x_0}_{0} f(x)dx = \frac{1}{K_{ox}\epsilon _0}\int^{x_0}_{0} x^{'}f(x)dx
\\
&x_0E_{x_0} - \triangle\phi_{ox} = \frac{1}{K_{ox}\epsilon_0}[x_0f(x_0)-\int^{x_0}_0x f(x)^{'}dx] = -\frac{1}{K_{ox}\epsilon_0}\int^{x_0}_0x f(x)^{'}dx = \frac{1}{K_{ox}\epsilon_0}\int^{x_0}_0x \rho_{ox}dx
\\
\\
&\therefore \triangle\phi_{ox} = x_0E_{x_0} -\frac{1}{K_{ox}\epsilon_0}\int^{x_0}_0x \rho_{ox}dx
\\
&\text{interface charge가 }\rho_{ox}\text{에 포함된다고 가정하자}
\\
&\therefore \triangle\phi_{ox} = x_0\frac{K_{semi}}{K_{oxide}}E_{semi} -\frac{1}{K_{ox}\epsilon_0}\int^{x_0}_0x \rho_{ox}dx
\\
\\
&V_G = \triangle\phi_{ox} + \phi_s
\\
&\therefore \triangle V_G = -\frac{1}{K_{ox}\epsilon_0}\int^{x_0}_0x \rho_{ox}dx
\\
&\text{물리적의미 : Boundary condition과 가까운 charge가 voltage 변화에 큰 영향을 미친다.}
\end{align}
$$
---

#### Oxide Charges의 종류

**1. Mobile Charges **

Na+ 가 대표적인 이유이다.

<img src="/images/18. Non Ideal MOS/image-20240128114950371.png" alt="image-20240128114950371" style="zoom:67%;" />

Charge 분포에 따른 그림은 다음과 같다.

<img src="/images/18. Non Ideal MOS/image-20240128115659161.png" alt="image-20240128115659161" style="zoom:40%;" /><img src="/images/18. Non Ideal MOS/image-20240128115719721.png" alt="image-20240128115719721" style="zoom:40%;" /><img src="/images/18. Non Ideal MOS/image-20240128115747912.png" alt="image-20240128115747912" style="zoom:40%;" />



**2. Fixed Charge**

Oxide와 Semiconductor 계면에 고정된 전하가 존재한다.

원인은 : excess ionic sillicon으로 규명된다.

해결 방법:  

1) Si [111]이 아닌 Si [100]을 사용한다.
1) Ar or N2에서 Annealing한다.

$$
\triangle V_G\text{(fixed charge)} = -\frac{Q_F}{C_O}
$$

**3. Interfacial Charge**

| 전자기준                        | Occupied States | Unoccupied States |
| ------------------------------- | --------------- | ----------------- |
| Donor like interfacial traps    | 0               | +e                |
| Acceptor like interfacial traps | -e              | 0                 |

상황 : Donor like interfacial traps은 다음과 같다.

<img src="/images/18. Non Ideal MOS/image-20240128121258866.png" alt="image-20240128121258866" style="zoom:50%;" />

소자에서 보통 Donor like interfacial traps과 Acceptor like interfacial traps을 동시에 갖는다. 

즉, **Fermi Level 위치에 따라 다른 상태를 나타낸다.**
$$
\begin{align}
&\text{책 : }
\\
&\text{In actual MOS devices the interfacial traps in the upper half of the band gaps are believed to be acceptor-like in nature}
\end{align}
$$

<img src="/images/18. Non Ideal MOS/image-20240128121435576.png" alt="image-20240128121435576" style="zoom:67%;" />

이를 모식도로 나타내면 다음과 같다.

<img src="/images/18. Non Ideal MOS/image-20240128123016377.png" alt="image-20240128123016377" style="zoom:50%;" />
$$
\begin{align}
&\triangle V_G(\text{interfacial traps}) = -\frac{Q_{IT}(\phi_s)}{C_0}
\\
&\phi_s\text{에 대한 함수임을 나타낸다.}
\end{align}
$$

**4. Radaiation Effect**

방사능에 의한 charge seperation

---

#### 정리

$$
\begin{align}
&\triangle V_G = (V_G - V^{'}_G) \vert _{same ~\phi _s}=\phi_{MS} - \frac{Q_F}{C_0} - \frac{Q_M \gamma _M}{C_0} - \frac{Q_{IT}(\phi_S)}{C_0}
\\
&\gamma_M \equiv \frac{\int^{x_0}_0 x\rho_{ion}(x)dx}{x_0\int^{x_0}_{0}\rho_{ion}(x)dx}
\end{align}
$$

Mos에서의 근사
$$
\begin{align}
&\triangle V_G = (V_G - V^{'}_G) \vert _{same ~\phi _s}=\phi_{MS} - \frac{Q_F}{C_0} - \frac{Q_M \gamma _M}{C_0} - \frac{Q_{IT}(2\phi_F)}{C_0}
\\
&V_{FB} = V_G\vert_{\phi _s = 0} = \phi_{MS} - \frac{Q_F}{C_0} - \frac{Q_M \gamma _M}{C_0} - \frac{Q_{IT}(0)}{C_0}
\\
&\text{따라서 이를 종합하면 다음과 같이 근사하여 나타낼 수 있다.}
\\
&V_T = V^{'}_T +V_{FB} 
\end {align}
$$
