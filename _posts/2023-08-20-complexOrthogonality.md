---
title: "복소 직교 및 정규직교"
author: 김태원
categories: quantumInformation
tags: [quantumInformation]
---

요약: 기초선형대수학에서 다루는 직교 및 기저를 $\mathbb{C}^{\Sigma}$로 다시 나타낸다. 

참고: *The Theory of Quantum Information*, John Watrous

---

[복소 유클리드 공간](https://pangmoo-ktw.github.io/pangmoo-KTW/complexEuclideanSpaces)상의 두 벡터 $u,v$는 그 내적이 $\langle u,v\rangle=0$인 경우 <u>직교(orthogonal)</u>라고 하며 $u\perp v$라고 표기한다.
[복소 내적과 노름](https://pangmoo-ktw.github.io/pangmoo-KTW/complexInnerProducts)상의 정의에 의해 아래가 성립한다.

$$
\begin{aligned}
u\perp v &\equiv \langle u,v\rangle = 0 \\
        &\equiv \sum_{a\in\Sigma}\overline{u(a)}v(a)=0
\end{aligned}
$$

알파벳 (공이 아니며 유한한 집합) 감마 $\Gamma$로 인덱싱한 아래 같은
벡터 모음은

$$
\lbrace u_a:a\in\Gamma\rbrace \subset \mathbb{C}^{\Sigma}
$$

모든 서로 다른 $a,b\in\Gamma$에 대해 $\langle u_a\ u_b\rangle = 0$이라면 <u>직교 집합</u>이라고 부른다. 직교집합상의 $0$이 아닌 벡터들은 선형독립이다. 

직교집합의 원소가 모두 <u>단위(unit)</u> 벡터라면 <u>정규직교(orthonormal)</u> 집합이라고 부른다. 그리고 정규직교 집합이 기저를 형성하면 <u>정규직교 기저</u>라고
한다. 앞서 언급한 $\Gamma$로 인덱싱한 집합의 경우 $\Gamma$의 크기 $|\Gamma|$가 $\Sigma$의 크기 $|\Sigma|$와 같고 오직 그 경우만 $\mathbb{C}^{\Sigma}$의 정규직교 기저다. 또 $\mathbb{C}^{\Sigma}$의 <u>표준기저</u>는 모든 $a,b\in\Sigma$에 대해 아래를 만족하는 집합 $\lbrace e_a:a\in\Sigma\rbrace$으로 주어진 정규직교 기저다. 

$$
e_a(b)=\begin{cases}1\quad a=b\textrm{인 경우}\\
       0\quad a\neq0\textrm{인 경우}\end{cases}
$$
