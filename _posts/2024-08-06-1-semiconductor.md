---
layout: single
title:  "1. Crystal Structure"
typora-root-url: ../
categories : "Fundamental-of-Semicondutor"
tag : crystal
#tag : [me, me2, me3]
toc : true
toc_sticky : true
author_profile : false
.archive__item-title {
    margin-top: 0.5rem !important;
    margin-bottom: 0.5rem !important;
---

## 1.Crystal Structure

<img src="/images/2024-08-06-1-semiconductor/image-20221020173830037.png" alt="image-20221020173830037" style="zoom:50%;" />(1)

![image-20221020173846766](/images/2024-08-06-1-semiconductor/image-20221020173846766.png)(2)

다음과 같은 Crystalline (made up of atoms in an orderly array)이 있다고 생각해보자. 

(2)를 이용하여 (1)을 만드는 과정을 생각할 수 있다. 

이러한 Crystalline에서 (2)는 Basis, (1)은 Lattice에 해당된다

*Basis는 도장으로 생각하면 편하다.*

* Basis 는 1개, 2개 등등 여러개 일 수 있고 

* Lattice는 서로 직각을 이루지 않아도 좋다. 

따라서, 조금 더 구체적으로 살펴보자.



-----

#### 1개의 Basis를 잡는법 : Wigner-Seitz Cell

1. 기준이 되는 lattice point 근처에 있는 다른 lattice points에 선을 연결한다.

2. 선을 이등분하는 곳에서의 법선을 그린다.

3. 법선들이 이루는 가장 작은 공간을 만든다.

   

*Wigner-Seitz Cell 중심에 하나의 원자가 있고 나머지는 빈공간이다.*

#### 1개의 Basis를 잡는법 : Primitive cell

*Crystal structure 마다 다르다.*

Cubic	FCC	BCC

<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/7/75/Simple_cubic_crystal_lattice.svg/1024px-Simple_cubic_crystal_lattice.svg.png" alt="File:Simple cubic crystal lattice.svg - Wikimedia Commons" style="zoom:30%;" /><img src="/images/2024-08-06-1-semiconductor/image-20221020175244603.png" alt="image-20221020175244603" style="zoom:50%;" /><img src="/images/2024-08-06-1-semiconductor/\image-20221020175318349.png" alt="image-20221020175318349" style="zoom:50%;" />

식은 다음과 같다.

Cubic
$$
a_{1} = a~\hat{x}
$$

$$
a_{2} = a~\hat{y}
$$

$$
a_{3} = a~\hat{z}
$$

FCC
$$
a_{1} = \frac{1}{2} a~(\hat{y}+\hat{z})
$$

$$
a_{2} = \frac{1}{2} a~(\hat{x}+\hat{z})
$$

$$
a_{3} = \frac{1}{2} a~(\hat{x}+\hat{y})
$$

BCC
$$
a_{1} = \frac{1}{2} a~(-\hat{x}+\hat{y}+\hat{z})
$$

$$
a_{2} = \frac{1}{2} a~(\hat{x}-\hat{y}+\hat{z})
$$

$$
a_{3} = \frac{1}{2} a~(\hat{x}+\hat{y}-\hat{z})
$$



---

#### Lattice(Bravais lattice)를 구성하는 법

<img src="C:\Users\minjun\AppData\Roaming\Typora\typora-user-images\image-20221020181320440.png" alt="image-20221020181320440" style="zoom:80%;" />

#### Reciprocal Lattice를 구성하는 법

Crystalline은 원자의 배열이 discrete한 값을 갖는다. 따라서, 양자역학에서의 x,p의 관계와는 다르게 discrete spectra를 가지므로  
$$
e^{iKR}=1
$$
<img src="C:\Users\minjun\AppData\Roaming\Typora\typora-user-images\image-20221020181049820.png" alt="image-20221020181049820" style="zoom:80%;" />

다음의 성질을 갖는다.

---

#### Reciprocal Lattice의 Primitive Cell은 다음과 같다.

Cubic
$$
b_{1} = a~\hat{x}
$$

$$
b_{2} = a~\hat{y}
$$

$$
b_{3} = a~\hat{z}
$$





FCC
$$
b_{1} = \frac{2\pi}{a} ~(-\hat{x}+\hat{y}+\hat{z})
$$

$$
b_{2} = \frac{2\pi}{a} ~(\hat{x}-\hat{y}+\hat{z})
$$

$$
b_{3} = \frac{2\pi}{a} ~(\hat{x}+\hat{y}-\hat{z})
$$

BCC
$$
b_{1} = \frac{2\pi}{a} ~(\hat{y}+\hat{z})
$$

$$
b_{2} = \frac{2\pi}{a} ~(\hat{x}+\hat{z})
$$

$$
b_{3} = \frac{2\pi}{a} ~(\hat{x}+\hat{y})
$$



#### Reciprocal Lattice의 Wigner-Seitz cell은 다음과 같다.

##### --> First Brillouin Zone

<img src="/images/2024-08-06-1-semiconductor/\image-20221020182440292.png" alt="image-20221020182440292" />