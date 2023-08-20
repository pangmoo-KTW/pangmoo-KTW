---
title: "복소 유클리드 공간상의 직접합"
author: 김태원
categories: quantumInformation
tags: [quantumInformation]
---

요약 : 벡터의 직접합 또한 벡터이기 때문에 벡터의 성질을 만족한다. 

참고: *The Theory of Quantum Information*, John Watrous 

---

[복소 유클리드 공간](https://pangmoo-ktw.github.io/pangmoo-KTW/complexEuclideanSpaces)이 $n$개 있다고 하자. 즉 아래 같은 것들이 존재한다. 

$$
\mathcal{X}_1=\mathbb{C}^{\Sigma_1},\ldots,\mathcal{X}_n=\mathcal{C}^{\Sigma_n}
$$

$\mathcal{X}_1,\ldots,\mathcal{X}_n$의 <u>직접합(direct sum)</u>은 아래 같은 복소유클리드공간으로

$$
\mathcal{X}_1\oplus\cdots\oplus\mathcal{X_n} = \mathbb{C}^{\Sigma_1\sqcup\cdots\sqcup\Sigma_n}
$$

여기서 $\Sigma_1\sqcup\cdots\sqcup\Sigma_n$는 아래처럼 정의되는 알파벳 $\Sigma_1,\ldots,\Sigma_n$의 <u>분리 합집합(disjoint union)</u>을 나타낸다.

$$
\Sigma_1\sqcup\cdots\sqcup\Sigma_n = 
\bigcup_{k\in\lbrace1,\ldots,n\rbrace}\lbrace (k,a):a\in\Sigma_k\rbrace
$$

(쉽게 말해 곱집합의 합집합으로, 분리합집합의 원소 $(k,a)$ 속 $k$는 $a$가 알파벳 $\Sigma_k$에 있었다는 사실을 알려준다) 

한편 벡터 $u_1\in\mathcal{X}_1,\ldots,u_n\in\mathcal{X}_n$에 대해 아래 같은 직접합은 

$$
u_1\oplus\cdots\oplus u_n\in\mathcal{X}_1\oplus\cdots\oplus\mathcal{X}_n
$$

각 $k\in\lbrace,\ldots,n\rbrace$와 $a\in\Sigma_k$에 대해 아래 같은 벡터를 나타낸다. 

$$
(u_1\oplus\cdots\oplus u_n)(k,a)=u_k(a)
$$

열벡터로 본다면 $u_1\oplus\cdots\oplus u_n$은 $\lvert\Sigma_1\rvert + \cdots + \lvert\Sigma_n\rvert$ 차원을 지니는 아래 벡터와 같겠다. 

$$
\begin{bmatrix}
u_1 \\ \vdots \\ u_n
\end{bmatrix}
$$

그리고 이 또한 벡터이기 때문에 모든 $u_1,v_1\in\mathcal{X}_1,\ldots,u_n,v_n\in\mathcal{X}_n$과 $\alpha\in\mathbb{C}$에 대해 아래 같은 성질을 만족한다.

$$
\begin{aligned}
& u_1\oplus\cdots\oplus u_n +v_1\oplus\cdots\oplus v_n
\\ =& (u_1+v_1)\oplus\cdots\oplus(u_n+v_n) \\ \\
&\alpha(u_1\oplus\cdots\oplus u_n) \\
=& (\alpha u_1)\oplus\cdots\oplus(\alpha u_n) \\\\
&\langle u_1\oplus\cdots\oplus u_n, v_1\oplus\cdots\oplus v_n\rangle \\
=& \langle u_1,v_1\rangle + \cdots + \langle u_n, v_n \rangle
\end{aligned}
$$
