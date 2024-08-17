---
layout: single
title: "6)Band Theory"
typora-root-url: ../
categories : "Solid State Physics"
tag : band
#tag : [me, me2, me3]
toc : true
toc_sticky : true
author_profile : false
---
## Solid State Physics

Electrons in periodic 1D crystal에 대해 배울 것이다.

Modeling : 

1D crystal - a linear chain of atomic orbitals.
$$
\begin{align}
&\vert \psi \rangle = \sum_n \phi _n \vert n \rangle
\\
&\text{Wavefunction = Linear Combination of Atomic Orbitals(LCAO)}
\\
\end{align}
$$
<img src="/images/7. Band theory/image-20240503161710036.png" alt="image-20240503161710036" />

위의 상황에 대한 Schrodinger's equation에 대한 증명은 다음과 같다.
$$
\begin{align}
&H=K + \sum_j V_j ~(V_j : \text{j번째 원자로 인한 Potential at r})
\\
&n^{th}, m^{th} : \text{n번째, m번째 atom을 의미함.}
\\
&\vert \psi \rangle = \sum _n \phi_n \vert n \rangle
\\
&H \vert \psi \rangle = E\vert \psi \rangle
\\
\\
&\text{이를 통해 식을 전개하면 다음과 같다.}
\\
&\langle\psi^* \vert H \vert \psi \rangle = E \langle \psi^* \vert \psi \rangle 
\\
&(?)
\\
&\sum_m\langle n \vert H \vert  m \rangle \phi_m = E \phi_n
\\
&\langle n \vert H \vert m \rangle = H_{nm}
\end{align}
$$
이를 통해 다음을 알 수 있다.
$$
\begin{align}
&H\vert m \rangle &&=(K+V_m) \vert m \rangle + \sum_{j \neq m } V_j \vert m \rangle
\\
&\langle n  \vert H\vert m \rangle &&= (K+V_m) \langle n  \vert  m \rangle + \sum_{j \neq m } \langle n \vert V_j \vert m \rangle
\\
&H_{nm} &&= \epsilon_{atomic} ~\delta_{nm} + \sum_{j \neq m } \langle n \vert V_j \vert m \rangle
\\
&\epsilon_{atomic} &&: \text{m번째 원자의 고유 에너지}
\\
&\sum_{j \neq m } \langle n \vert V_j \vert m \rangle &&: \text{m번째 원자가 j번째 원자와 interaction 후에 n번째 원자로 hopping}
\\
&\sum_{j \neq m } \langle n \vert V_j \vert m \rangle &&= ~V_0 ~~n=m\text{일 때}
\\
& ~ &&=-t ~~n=m \pm 1\text{일 때}, t\text{는 hopping을 나타내는 term으로 얼마나 원자들끼리 가까이 있는지를 나타낸다.}
\\
& ~ &&=0~~ \text{otherwise}
\\
\\
&\therefore H_{nm} &&= \delta _{n,m}(\epsilon_{atomic} - V_0) - t(\delta_{n+1,m} + \delta_{n-1,m})
\end{align}
$$
이를 그림으로 나타내면 다음과 같다.

<img src="/images/7. Band theory/image-20240507081633105.png" alt="image-20240507081633105" style="zoom:67%;" />
$$
\begin{align}
\\
&\phi_n = \frac{e^{-jkna}}{\sqrt{N}}, \sum_m H_{nm}\phi_m = E \phi_n \text{을 통해 계산한다.}
\\
&\text{Dispersion relation : } E = \epsilon _0 - 2t~cos(ka)
\end{align}
$$
이를 그래프로 나타내보자.

<img src="/images/7. Band theory/image-20240507083115776.png" alt="image-20240507083115776" style="zoom:67%;" />

- N state의 평균 E 는 $E_o$ 이다.
- **Binding Energy** = $E - N\epsilon _0 = \triangle E$이다.   $E$는 실제 에너지 크기를 의미하는 듯.

---

 #### Electron band structure의 의미

**Monovalent atomic crystal**

Crystal이 N개의 unit cell로 구성이 되어 있고, unit cell에는 1개의 원자와 전자가 들어가있다고 생각해보자.

전자는 fermion이므로 2개의 스핀 상태를 갖을 수 있다. 따라서, Band의 절반만 채워진다.

<img src="/images/7. Band theory/image-20240507101648054.png" alt="image-20240507101648054" style="zoom:67%;" />

만약 전기장을 가하게 되면, 전자의 운동량을 증가하는 방향이므로 shift가 된다. 따라서, wave packet의 관점에서 전자는 이동하게 된다.

<img src="/images/7. Band theory/image-20240507101916098.png" alt="image-20240507101916098" style="zoom:67%;" />

**Divalent atomic crystal**

unit cell에 1개 원자와 2개의 전자가 들어있다. 전자는 모두 Band를 채운 상태이므로, wave packet의 관점에서 전자 이동은 존재하지 않는다. 따라서, 전기장에 대해 전자가 흐르지 않고 insulator처럼 작동한다.



이런한 것들을 모두 정리하면 다음과 같이 물질을 분류할 수 있다. 

<img src="/images/7. Band theory/image-20240507102124900.png" alt="image-20240507102124900" />