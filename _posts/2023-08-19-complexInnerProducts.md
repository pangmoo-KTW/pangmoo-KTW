---
title: "복소 내적과 노름"
author: 김태원
categories: quantumInformation
tags: [quantumInformation]
---

요약 : $\mathbb{C}^n$상의 내적은 실수 유클리드 공간 $\mathbb{R}^n$과
약간 다르다.

참고: The Theory of Quantum Information, John Watrous

---

$\mathbb{C}^n$은 사실상 유한하고 공이 아닌 집합 $\Sigma$에서 $\mathbb{C}$로
사상하는 함수를 몽땅 모은 $\mathbb{C}^{\Sigma}$의 약식 표기다.
(참고: [복소 유클리드 공간](https://pangmoo-ktw.github.io/pangmoo-KTW/complexEuclideanSpaces)) 
두 벡터 $u,v\in\mathbb{C}^{\Sigma}$에 대해 내적 $\langle u,v\rangle$은 아래처럼
정의한다. 

$$
\langle u,v\rangle = \sum_{a\in\Sigma}\overline{u(a)}v(a)
$$

$\overline{u(a)}$ 위에 있는 $-$는 $u(a)$의 켤레 복소수(complex conjugate)를
나타낸다. 켤레 복소수란 복소수의 허수부에 덧셈 역원을 취한 것으로, 
$\alpha = x+iy$에 대해 $\overline{\alpha}= x-iy$ 같은 식이다. 즉 
$\mathbb{C}^{\Sigma}$상의 내적 $\langle u,v\rangle$은 가령 $|\Sigma|=2$에 대해
이런 느낌이다. 

$$
\begin{aligned}
\langle u,v \rangle &= \sum_{a\in\Sigma}\overline{u(a)}v(a) \\
        &= \overline{\begin{bmatrix}\alpha_1\\\alpha_2\end{bmatrix}}
        \begin{bmatrix}\beta_1\\\beta_2\end{bmatrix} \\
        &= \begin{bmatrix}x_1-iy_1\\x_2-iy_w\end{bmatrix}
        \begin{bmatrix}a_1+ib_1\\a_2+ib_2\end{bmatrix} \\
\end{aligned}
$$

즉 켤레 복소수가 도입된 이유는 (실수 공간처럼) 내적의 값을 $0$이상으로
보장하기 위해서다. 이 조건 말고도 위와 같은 정의는 실수 내적의 세 가지 조건을
복소 유클리드 공간에 시뮬레이션한다. 

- <u>두 번째 인자상의 선형성</u>. 
    모든 $u,v,w\in\mathbb{C}^{\Sigma}$와 $\alpha,\beta\in\mathbb{C}$에 대해 아래 
    방정식이 성립한다.

    $$
    \langle u,\alpha v+\beta w\rangle = \alpha\langle u,v\rangle 
    + \beta\langle u,w\rangle
    $$

- <u>복소 대칭</u>. 모든 $u,v\in\mathbb{C}^{\Sigma}$에 대해 아래 방정식이 
    성립한다.

    $$
    \langle u,v\rangle = \overline{\langle v,u\rangle}
    $$

- <u>양의 보장</u>. 모든 $u\in\mathbb{C}^{\Sigma}$에 대해 아래 방정식이 
    성립하며

    $$
    \langle u,u\rangle\geq0
    $$

    $u=0$인 경우 그리고 오직 그 경우만 등식으로 성립한다.

노름(norm) 혹은 크기 또한 아래처럼 정의되어

$$
\begin{aligned}
\|u\| &= \sqrt{\langle u,u\rangle} \\
    &= \sqrt{\sum_{a\in\Sigma}\overline{u(a)}u(a)} \\
    &= \sqrt{\sum_{a\in\Sigma}|u(a)|^2}
\end{aligned}
$$

아래 성질을 만족한다. 

- <u>양의 보장</u>. 노름은 $0$이상이며 벡터가 $0$인 경우만 노름이 $0$과 같다. 
- <u>양의 확장성</u>. 모든 $u\in\mathbb{C}^{\Sigma}$와 $\alpha\in\mathbb{C}$에
    대해 아래 방정식이 성립한다.  

    $$
    \|\alpha u\| = |\alpha|\|u\|
    $$

- <u>삼각 부등식</u>. 모든 $u,v\in\mathbb{C}^{\Sigma}$에 대해 아래 삼각 부등식이
    성립한다. 

    $$
    \|u+v\| \leq \|u\|+\|v\|
    $$

- <u>코시-슈바르츠 부등식</u>. 모든 $u,v\in\mathbb{C}^{\Sigma}$에 대해 아래
    부등식이 성립하며

    $$
    |\langle u,v\rangle|\leq \|u\|\|v\|
    $$

    $u$와 $v$가 선형독립인 경우만 등식으로 성립한다. 
