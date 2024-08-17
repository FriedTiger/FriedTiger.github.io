---
layout: single
title: "1)OLED Introduction"
typora-root-url: ../
categories : "OLED"
tag : exciton
#tag : [me, me2, me3]
toc : true
toc_sticky : true
author_profile : false
---
## OLED

### Organics can do Anything!

#### Excited state 

Inorganic materials : **FREE** electron and hole

"Delocalized"



Organic materials : **Exciton** - strongly bound electron and hole pair 

"Localized"

"electrically neutral and mobile"

"Qusai-particle"

<img src="/images/figure/image-20230307144719733.png" alt="image-20230307144719733" />

1. Exciton의 경우에 물질내의 Bandgap E보다 더 작은 값을 갖게 된다. 

이는 다음과같다.
$$
E _{\text{Exciton Energy}} = E_{\text{Bandgap}} - E_{\text{Exicton Binding Energy}}
$$

2. Exciton의 경우에 Qusai-particle이므로 diffusion할 수 있다. 

   diffusion을 하면서 E가 작아질 수 있다.
   
   이는 Display를 만들기 위해 상당히 좋지 않다.
   
   따라서, OLED는 amorphous molecular을 통해 만든다. 
   
   **만약, Exciton 2.7eV가 diffusion 되면 1~2eV의 크기를 갖거나(IR), nonradiative를 나타낼 것이다**
   
   **OLED가 spectrum이 넓은 이유 : Condon princinple 때문에, 만약 OLED물질이 만약 Rigid하면 반치폭이 줄어들 것이다**

---



#### Small molecules vs Polymers

small molecules : 결정성을 갖을 수 있음.

즉, small molecules들이 periodically arranged하게 될 수 있다는 뜻

polymers : 결정성이 없음.



**유기반도체에서는 결정성이 없어야 한다. **

---



#### Exciton의 움직임

#### 1. Forster Resonant Energy Transfer (FRET)

분자들 사이를 움직이는 에너지로 Singlet to Singlet 의 에너지 이동을 의미한다.

먼 거리를 이동할 수 있고(~10nm) dipole-dipole interaction에 의해 움직인다.

#### 2. Dexter Energy Transfer (DET)

분자들 사이를 움직이는 에너지로 Triplet to Triplet의 에너지 이동을 의미한다.

짧은 거리만 이동할 수 있다.(~1nm) wave function의 overlap에 의해 움직인다.

---



#### Molecular binding force - Van der Waals bonds

유기 반도체 내에서 전기적으로 중성을 띠는 분자들은 chemical bond(covalent or metallic bonds)를 형성할 수 없다.

**$\pi$ bonding**은 Angular momentum값이 존재하기 때문에 spatial difference를 갖고 있고 이에 따라 $\sigma$ bonding보다 쉽게 움직일 수 있어 쉽게 polarized 된다.

이를 **Largely delocalized across the molecule** 로 표현한다.

Van der Waals bonds는 다음으로 정의 된다. 

Van der Waals force : electrostatic attraction between induced dipoles

<img src="/images/figure/image-20230321140747811.png" alt="image-20230321140747811" style="zoom:50%;" />

Van der Waals Potential은 다음의 에너지를 갖는다. 
$$
U_{\text{vdW}} \propto \frac{1}{r^6} \text{Van der Waals Potential}
\\
U_{\text{Coul}} \propto \frac{1}{r} \text{Coulomb Potential}
$$


따라서, 크기가 굉장히 작기 때문에 Van der Waals bond로 molecular crystal이 안정적으로 구성되기 위해서는 >um 이상의 두께가 필요하다.

---



#### Energy splitting in molecular orbitals

1. Energy difference가 적을수록 Energy splitting이 많이 일어난다.

<img src="/images/figure/image-20230321140906205.png" alt="image-20230321140906205" style="zoom:50%;" />

2. Spatial difference가 클수록 Energy splitting이 많이 일어난다.

<img src="/images/figure/image-20230321140946567.png" alt="image-20230321140946567" style="zoom:67%;" />

---

#### Frontier molecular orbital theory

frontier orbital theory는 HOMO와 LUMO의 개념을 통해 Molecular orbital을 이해하는 이론이다. 

가장 중요한 것은 **$\pi$ bonding** 이다.

<img src="/images/figure/image-20230321141304831.png" alt="image-20230321141304831" style="zoom:67%;" />

1. 일반적으로 $\pi$ bonding이 HOMO와 LUMO 를 결정한다. 즉, Energy band gap을 정한다.
2. $\pi$ bonding은 induced dipole을 형성하고, Van der Waals bond를 형성한다. 따라서 고체 형성에 중요한 요소이다.
