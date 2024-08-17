---
layout: single
title: "3)Formalism for Quantum Mechanics"
typora-root-url: ../
categories : "Quantum-Mechanics"
tag : Quantum
#tag : [me, me2, me3]
toc : true
toc_sticky : true
author_profile : false
---
## Quantum Mechanics 

#### 개념잡기 

양자역학는 wave function과 operators 두가지 개념으로 구성된다.

| Quantum theory          | Mathematically                               |
| ----------------------- | -------------------------------------------- |
| wave function           | vector                                       |
| operators               | transformations                              |
| Hermitian operators     | Linear transformations                       |
| normalizable            | Hillbert space                               |
| Hermitian을 만족시킨다.  | 행렬에 transpose conjugate해도 같다.          |
| commute                 | 물리적 의미를 갖는다, 공통된 basis를 갖는다.    |

Basis : a set of ***Linearly Independent vectors*** that **spans** the space ; f(x)

span : verb. **every vector** can be written as a **linear combination** of the members.

dimension : the number of vectors **in any basis**
$$
\text{norm ~of ~the ~vector} ~:~ \parallel \alpha \parallel ~\equiv~ \sqrt{\angle \alpha \mid \alpha \rangle }
$$
unit vector : norm is 1 vector

orthogonal : inner product is zero

Linear Transform : each vector **in a vector space** --> some other vector **in a vector space**

* 이 때의 basis 공간은 같은 공간이다. 즉, 벡터가 다른 공간으로 갔지만 **표현은 기본 basis 공간**으로 하는 것.

complete : any vector can be expressed as a linear combination of any other function in Hilbert space

  

- Linear transformations 는 matrices로 NxN의 형태를 갖는다. 

그러나, 사실 양자역학에서는 차원이 무한대이기 때문에 무한대 X 무한대의 형태를 갖는다.

이때, basis 를 linear transformations 하면 다른 basis들의 식으로 표현된다.

즉, Hillbert space에서 a set of functions 들은 complete 하다.



* Matrix Element 
  $$
  (S_z)_{mn} =\left< m \mid S_z \mid n \right>
  \\
  \text{hermition operator인} ~S_z \text{를 Matrix로 나타낼 때, n vector를~} S_z\text{operator 적용을 하고 m의 basis로 표현한 것을 의미한다.}
  $$
  

- 연산자.

*Hermitian operator는 Observables들의 실수 값으로 나오게 하는 연산자를  의미한다.

질문 : Hillbert space는 opertors를 적용 후에 qusai를 나타내는 것일 까 아니면 적용 전에 나타내는 것일까?

적용 전이다! O

<img src="/images/3. Formalism for quantum mechanics/image-20220927182730682.png" alt="image-20220927182730682" />

그러나, 오해하지 말아야하는 것이 normalizable 한 basis 들의 선형 조합으로 이루어져있다. 따라서,  free particle Hamiltonian은 x에 대한 basis에 normalizable 하지 않으므로 Hillbert space가 아니다.

<img src="/images/3. Formalism for quantum mechanics/image-20221031173312589.png" alt="image-20221031173312589" style="zoom:90%;" />

다음처럼 생각할 수 있다.

양자역학에서 spectrum이란, a Operator를 적용하였을 때 나오는 eigenvalue들을 다 모아놓은 것이다.

* a Operator에 대해 eigenvalue가 나온다는 것은 eigenfunction이 eigenvalue에 대해 determinate state를 갖는다는 것이다. 이 때, eigenfunction은 discrete(eigenvalue들이 불연속적으로 많음)와 continuous(eigenvalue들이 연속적으로 개많음)를 갖을 수 있다.
* complete 하다 : Hillbert Space의 주민들(eigenfunction)로 주민들을 나타낼 수 있다.



---

#### Continuous Spectra

위에 상황이 어떻게 기술 되었는지 Continuous Spectra 상황에 대해 알아보자

1. free particle의 wave function은 다음과 같다. 

$$
f_p(x) = Ae^{\frac{ipx}{h}}
$$

이 함수는 square-integrable하지 않으므로 Hillbertspace에 있지 않다.

그러나, p가 실수의 값을 가진다고 가정하면 
$$
<f_{p'}(x)\mid f_p(x)> = \mid A \mid ^2 \int^\infty _\infty{e^{i(p-p')x/ \hbar}dx} = \mid A \mid ^2 2\pi \hbar \delta(p-p') = \delta (p-p')
$$
따라서 이를 Hillbertspace에서와 같이 해석할 수 있다. 

이를 더 해석하면 f_p(x)가 마치 p-space에서의 basis 역할을 한다고 할 수 있다. (이 때, A = 1/root(2pi hbar))

위의 식을 **Dirac orthonormality** 라고 한다.

선형 조합으로 나타낼 수 있으므로 complete하고 따라서 Hilbertspace에서와 같이 행동한다.



Debrogie Equation은 다음과 같다.
$$
\lambda = \frac{2 \pi \hbar}{p}
$$
p의 determinate states는 존재하지 않는다. 따라서, p는 Continuous Spectra(wave packet)를 의미한다.

2. free particle의 위치는 어디에 있을까?

$$
\hat x g_y(x ) = x g_y(x) : x ~\text{operator}
\\
\hat xg_y(x) = yg_y(x) : y ~\text{eigenvalue}
$$

이를 정리하면 다음과 같다. 
$$
g_y(x) = A \delta(x-y)
$$
즉, 위치에 대한 eigenfunction이 delta함수를 갖는다. 

위와 같은 논리로 wavepacket에 대해 위치에 대한 값을 갖는다.

---

#### Generalized statisical interpretation

1. Discrete Spectra
   $$
   c_n = \langle f_n \mid \psi \rangle 
   \\ \text{발견될 ~확률} = \mid c_n \mid ^2
   $$

2. Continuous Spectra
   $$
   c_z = \langle f_z \mid \psi \rangle
   \\ \text{발견될 ~확률} = \mid c(z)\mid^2 dz
   $$
   이를 푸리에 변환과 연계하여 생각할 수 있고 이는 다음과 같다.

$$
\phi (p, t) = \frac{1}{\sqrt{2 \pi \hbar}}\int^{\infty}_{-\infty}e^{-ipx\hbar}\mathbf{\psi} (x,t)dx ~ (\text{in~momentum~space}) 
\\\psi (x, t) = \frac{1}{\sqrt{2 \pi \hbar}}\int^{\infty}_{-\infty}e^{ipx\hbar}\mathbf{\phi} (p,t)dx ~ (\text{in~position~space})
$$

----

#### Uncertainty Priciple

$$
\sigma ^2 = \langle (\hat A - \langle A \rangle )\psi \mid (\hat A - \langle A \rangle )\psi> = \langle f\mid f \rangle 
$$



Schwarz inequality에 의해
$$
\sigma _A ^2 \sigma _B ^2 \geq (\frac{1}{2i}\langle [\hat A, \hat B] \rangle )^2
$$
따라서, commute 하지 않으면 일정 값보다 크거나 같아야한다. --> incompatible observables.

incompatible observables : 공통된 eigenfunction들을 가지지 못한다.

commute 하다면 eigenvalue에 대해 다른 공간에서의 eigenfunction을 가질 수 있다.



#### Position-momentum uncertainty principle

$$
\triangle x \triangle p \geq \frac{\hbar}{2}
$$



위치와 운동량은 commute하지 않는다.

위치와 운동량의 불확정성 원리를 살펴보면, 위치를 측정하면 운동량은 무한대의 함수를 가질거고, 운동량(sin)을 측적하면 무한대의 위치를 가질 것이다.

** Uncertainty Principle이 최소값이 되게하는 p에 의한 psi와 x에 의한 psi가 평행을 이룬다는 것이고 이는 계산결과, gaussian function을 갖는다.



#### Energy-time uncertainty principle


$$
\triangle t \triangle E \geq \frac{\hbar}{2}
$$
에너지 시간 불확정성의 원리는 위치-운동량 불확정성 원리와는 다르다. 

Q라는 observable과 ^Q의 operator를 생각해보자.
$$
\frac{d \langle Q \rangle }{dt} = \frac{d \langle \psi \mid \hat Q \psi \rangle }{dt}
\\ i \hbar \frac{\partial  \psi}{\partial t} = \hat H \psi
$$
이를 정리하면 다음과 같다.
$$
\frac{d \langle Q \rangle }{dt} = \frac{i}{\hbar} \langle [\hat H, \hat Q] \rangle  + \langle \frac{\partial \hat Q}{\partial t}\rangle 
$$
이를 슈바르츠 부등식을 적용하면,
$$
\frac{\sigma_Q}{\mid\frac{d<Q>}{dt}\mid}\sigma _H \geq \frac{\hbar}{2}\mid\frac{d<Q>}{dt}\mid ( \text{Q는~ 모든 ~어떠한~ 물리량} )
$$
다음과 같이 생각할 수 있다.
$$
\triangle t \equiv \frac{\sigma_Q}{\mid\frac{d<Q>}{dt}\mid} ( \triangle \text{t는~ Q의~물리량이~표준편차로~변하는데~걸리는~시간})
$$

---

#### Dirac Notation

$$
bra ~:~ <\alpha \mid ~,~ ket ~:~ \mid \beta >
$$

ket이 vector인 것은 자명하다.

bra의 의미는 어떤것을 의미할까? --> **linear function**을 의미한다 : ket을 **복소수로 Linear mapping** 하는 것을 의미한다.

선형대수로 생각하면 다음과 같다.

ket : column, bra : 복소수 raw

따라서, ket은 basis에 대한 vector, bra는 또 다른 vector basis에 대한 공간으로 생각할 수 있다. 

<img src="/images/3. Formalism for quantum mechanics/image-20221109112253972.png" alt="image-20221109112253972" style="zoom:67%;" />

이를 다음과 같이 생각 할 수 있고, 따라서 이를 Dual Space라 한다.

BraKet의 의미 : 내적

KetBra의 의미 : 연산자 ( 이유: 벡터를 오른쪽에 곱하면 벡터가 나옴)



#### Dirac Notation을 통한 Basis transform ####

$$
\vert S(t) \rangle = \int dx\vert x\rangle \langle x\vert S(t)\rangle = \int \Psi(x,t)\vert x \rangle dx
\\ \vert S(t) \rangle = \int dx\vert n\rangle \langle n\vert S(t)\rangle = \sum c_n(t) \vert n \rangle
$$

이를 정리하면 다음과 같다.
$$
\Psi(x) = \langle x \vert S(t) \rangle = \sum c_n(t) \langle x \vert n \rangle = \sum c_n \psi_n(x,t)
$$

---

#### 정리 ####

$$
\langle x \vert \hat x\vert S(t) \rangle
\\ \langle p \vert \hat x \vert S(t) \rangle
$$

이 어떻게 표현되는지 알면 정리가 된 것이다.
