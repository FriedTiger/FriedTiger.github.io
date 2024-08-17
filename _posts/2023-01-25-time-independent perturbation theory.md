---
layout: single
title: "7)Time independent perturbation theory"
typora-root-url: ../
categories : "Quantum-Mechanics"
tag : Quantum
#tag : [me, me2, me3]
toc : true
toc_sticky : true
author_profile : false
---
## Quantum Mechanics 

지금까지 배운 Time-Independent Schredinger Equation 식은 다음과 같다.
$$
\hat H^0 \mid \psi \rangle = E^0_n \mid \psi \rangle
$$
Real한 상황에서는 복잡한 Hamiltonian이 적용된다. 따라서, hamiltonian을 unperturbed + perturbed로 나타내자.
$$
H = H_0 ~+ V
\\
V= \lambda W,~ \lambda (scale~ factor) \text{는 1보다 매우 작고} ~ W \text{는 } H_0 \text{와 비슷한 scale을 갖는다.}
\\
\\
H \mid \psi \rangle = E_n \mid \psi \rangle ~~~~ ---(1)
$$
다음과 같이 가정할 수 있다. 
$$
E_n = E^0 _n + \lambda E^1_n + \lambda ^2 E^2 _n + \cdot \cdot \cdot
\\
\mid \psi \rangle = \mid \psi ^0 _n\rangle + \lambda \mid \psi ^1 _n\rangle + \lambda ^2\mid \psi ^2 _n\rangle + \cdot\cdot\cdot \text{이를 통해 다음을 나타낼 수 있다.}
\\
\mid \psi \rangle = \mid \psi ^0 _n\rangle + \lambda \sum_i c_i\mid \psi ^0 _i\rangle + \lambda ^2 \sum_j\mid \psi ^0 _j\rangle + \cdot\cdot\cdot \\
\text{perturbation으로 인한 1st order~ 무한대 order에 대한 phi를 unperturbation 함수들의 집함으로 표현하는 것이다.}\\
\psi^0 _i \text{는 complete set이므로 모든 것들을 basis인~} \sum_i \psi^0_i \text{의 조합으로 나타낼 수 있다.}
$$
이를 (1)식에 대입하면 다음과 같다.
$$
(H_0 + \lambda W) \left[\mid \psi ^0 _n\rangle + \lambda \sum_i c_i\mid \psi ^0 _i\rangle + \lambda ^2 \sum_j\mid \psi ^0 _j\rangle + \cdot\cdot\cdot\right]
\\
= (E^0 _n + \lambda E^1_n + \lambda ^2 E^2 _n + \cdot \cdot \cdot)\left[\mid \psi ^0 _n\rangle + \lambda \sum_i c_i\mid \psi ^0 _i\rangle + \lambda ^2 \sum_j\mid \psi ^0 _j\rangle + \cdot\cdot\cdot\right]
$$
이를 lambda에 대한 order로 정리할 수 있다.
$$
0th : H_0 \mid \psi \rangle = E^0_n \mid \psi \rangle
\\
1st : W \mid \psi ^0 _n \rangle + \sum c_i H_0 \vert \psi ^0 _i \rangle = E^0_n \sum c_i \mid \psi^0 _i \rangle +E^1_n \vert\psi ^0 _n\rangle
\\
\\
\text{1st order를 통해 다음을 알 수 있다.}
\\
E^1_n = \langle \psi^0_n\vert W \vert \psi^0_n\rangle
\\
\therefore E_n = E^0_n + \langle \psi^0_n \vert V \vert \psi^0_n \rangle
\\
\\
c_m = \frac{\langle\psi^0_m \vert W \vert \psi^0_n \rangle}{E^0_n - E^0_m}
\\
\therefore \vert \psi_n \rangle = \vert \psi^0_n\rangle+\sum_{m \neq n} \vert \psi^0_m \rangle \frac{\langle \psi^0 _m \vert V \vert \psi^0_n \rangle}{E^0_n -E^0_m}
\\
\\
\text{2nd order는 다음과 같다.}
\\
E_n = E^0_n + \langle \psi^0_n \vert V \vert \psi^0_n \rangle + \sum_{m \neq n} \frac{\vert \langle \psi^0 _m \vert V \vert \psi^0_n \rangle \vert ^2 }{E^0_n - E^0_m}
\\
= E^0_n + \left[  \langle \psi^0_n \vert V \vert \psi^0_m \rangle + \sum _{m \neq n} \frac{\vert \psi^0 _m \vert V \vert \psi^0_n \rangle }{E^0_n - E^0_m }\right]\langle \psi^0_m \vert V \vert \psi^0_n \rangle
$$

#### Degeneracy Perturbation





---

#### The Relativistic Correction

Hamiltonian은 다음과 같이 표기된다. 
$$
\hat {H} = \hat {T} + \hat {V}
\\
\hat {T} = \frac{p^2}{2m} = - \frac{\hbar ^2}{2m} \triangledown ^2
\\
\text{상대성 관점에 의해}
\\
T = \frac{p^2}{2m} - \frac{p^4}{8m^3 c^2}+ \cdot \cdot \cdot/
$$
ex) 수소 원자 

따라서 다음과 같은 perturbation이 발생한다.
$$
E^1_r = - \frac{(E_n)^2}{2mc^2} \left[ \frac{4n}{l+1/2} - 3 \right]
$$

---

#### Spin Orbit Coupling

$$
H = - \mu \cdot B
\\
\text{B는 전자 입장에서 원자핵이 궤도운동을 하고 이에 따라 전자에 자기장이 발생한다.}
\\
\mu : \text{magnetic dipole moment}
$$

ex) 수소 원자

따라서 다음과 같은 perturbation이 발생한다.
$$
E_{nj} = - \frac{13.6eV}{n^2} \left[ 1 + \frac{\alpha ^2}{n^2} \left(\frac{n}{j+1/2} - \frac{3}{4} \right)\right]
$$

---

#### Zeeman Effect

#### Stark Effect