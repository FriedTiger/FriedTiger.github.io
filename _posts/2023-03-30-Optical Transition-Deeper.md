---
layout: single
title: "5)Optical transition - Advanced"
typora-root-url: ../
categories : "OLED"
tag : exciton
#tag : [me, me2, me3]
toc : true
toc_sticky : true
author_profile : false
---
## OLED

#### Born-Oppenheimer approximation

1) nuclei는 무겁기 때문에 위치를 fix하고 Electronic wavefunction과 $E_e$를 구한다.
2) $E_e$ 를 활용하여 Vibrational wavefunction에 대해 구한다. 

이를 수식적으로 나타내면 다음과 같다. 
$$
\text{Schrodinger Equation}
\\
[\underline{T_e + T_n} + \underline{V_{ne}(\bold{r}, \bold{R}) + V_{ee}(\bold{r})+V_{nn}(\bold{R})}]\Psi_{total}(\bold{r},\bold{R})= E(\bold{R})\Psi_{total}(\bold{r}, \bold{R})
$$

$$
\text{Born-Oppenheimer approximation}
\\
[T_e + V_{ne}(\bold{r}, \bold{R})+V_{ee}(\bold{r})]\psi_e(\bold{r}, \bold{R}) = E_e (\bold{R}) \psi_e(\bold{r}, \bold{R}) \rightleftharpoons \text{Electronic wavefunction (for electrons)}
\\
[-\sum_i \frac{\hbar^2}{2M_i}\triangledown^2_R + E_e(R)+V_{mn}(\bold{\bold{R}})]\psi_n(\bold{R}) = E_n\psi_n(\bold{R}) \rightleftharpoons \text{Virbrational wavefunction (for nulcei)}
$$

위 식에서 전자의 spin과 관련이 있는 항은 $V_{ee}$ 이다. 

$V_{ee}$ 는 operator이므로 $\hat{V_{ee}}$ 으로 표시할 수 있고 다음의 spin 상태일 떄 에너지를 구할 수 있다.
$$
\text{Singlet : } E_{ee,S} = \langle \psi_{e, S} \vert \hat{V}_{ee} \vert \psi_{e,S} \rangle = J +K 
\\
\text{Triplet : } E_{ee,T} = \langle \psi_{e, T} \vert \hat{V}_{ee} \vert \psi_{e,T} \rangle = J - K 
$$

$$
\therefore \text{위 식을 정리하고 spin에 대해 나타내면 다음과 같다.}\\
J = \langle \uparrow \downarrow \vert \frac{1}{4 \pi \epsilon _{12}} \vert \uparrow \downarrow \rangle \rightleftharpoons \text{Coulomb integral}
\\
K = \langle \uparrow \downarrow \vert \frac{1}{4 \pi \epsilon r_{12}} \vert \downarrow \uparrow \rangle \rightleftharpoons \text{Exchange Integral}
$$

$\triangle E_{ST} = 2K$

Standard organic material : 0.7 - 1(eV)

Phosphorescent organometallic complex : 0.2 - 0.3(eV)

TADF molecule : 0.05 - 0.1 (eV) 

---

#### Bimolecular annihilation

정의 : Excited donor's Exciton --> Excited acceptor's Exciton

A,B 의 Exciton이 있다고 생각해보자.

1.A의 Exciton이 B의 Exicton으로 빛 방출 없이 Exicton을 전달할 수 있다.

2.그렇다면 B의 Exciton은 **"HOT Exicted State"** 이 된다.

3.HOT exicted state exciton은 lowest excited state level로 내려간다. 
$$
\text{Singlet Exciton annihilation}
\\
\begin{align}
&SSA ~~:~~S_1 + S_1 \rightarrow S_n + S_0 (n \geq 1) \rightarrow S_1 + S_0
\\
&- \text{singlet은 exciton lifetime이 짧아 SSA 잘 안일어남}
\\
&STA ~~:~~S_1 + T_1 \rightarrow T_n + S_0 (n \geq 1) \rightarrow T_1 + S_0
\\
&- \text{Exciton quencing의 주 원인. EQE, lifetime 감소에 영향을 미침} 
\\
&SPA ~~:~~S_1 + P_1 \rightarrow P_n + S_0 (n \geq 1) \rightarrow P_1 + S_0
\end{align}
$$

$$
\text{Triplet Exciton annihilation}
\\
\begin{align} 
&TTA ~~:~~T_1 + T_1 \rightarrow (TT)^* + S_0 \rightarrow S_n + S_0 ~~or~~ T_n + S_0 ~~or~~ Q_n + S_0 \\
& -S^* : \text{효율 상승에 도움이 됨.} \\
& -T^* : \text{lifetime에 영향을 미침.} \\
& -Q^* : \text{일어나기 거의 힘듬.}
\\
&TTA ~~:~~T_1 + P_1 \rightarrow P_n + S_0  \rightarrow P_1 + S_0
\end{align}
$$

생성된 Hot excited state의 exciton은 다음 그림처럼 2가지로 전이될 수 있다.

1. **Dissociation **

   Dissociation limit($T_1$ 과 $T_2$ 의 특정 vibrational E 이상)을 넘어가면 분자가 2개의 분자로 쪼개어진다. --> 영구적인 효율 저하

   **내 생각 : Triplet은 서로 밀어내는 교환자가 작용하여 Exicton 사이의 거리가 더 멀어 Singlet보다 끊어지기 쉽다.** 

2.  **Pre-dissociation** 

   Dissociation limit에 해당되는 에너지가 되기 전 (pre-) 에도 dissociation이 발생할 수 있다. 이는 실험적으로 검증되었다.-이재상교수
   
   이는 기존에 존재하단 small molecular 또는 다른 분자와의 exciton 충돌로 인해 발생하는 것으로 생각할 수 있다.

<img src="/images/figure/image-20230528214611222.png" />

