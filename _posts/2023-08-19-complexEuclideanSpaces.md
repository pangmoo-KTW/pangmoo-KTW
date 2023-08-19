---
title: "복소 유클리드 공간"
author: 김태원
categories: QuantumInformation
tags: [QuantumInformation]
---

요약: 양자정보이론에서 사용하는 벡터공간 $\mathbb{C}^n$의 정체는 무엇인가?

참고: *The Theory of Quantum Information*, John Watrous

---

양자정보이론의 첫 관문은 이렇게 생겼다.

$$
\mathbb{C}^n
$$

사실 $\mathbb{C}^n$은 아래와 동치인 약식 표기다.

$$
\mathbb{C}^{\Sigma}
$$

그런데 이게 도대체 무엇인가? 

우선 $^{\Sigma}$가 거슬린다. $\Sigma$는 <u>알파벳(alphabet)</u>이라는 집합이다.
알파벳이 꼭 시그마 $\Sigma$일 필요는 없고, 감마 $\Gamma$ 등 아무 그리스어
대문자로 나타낼 수도 있다. 알파벳은 <u>기호(symbols)</u>를 원소로 지니는
유한하고 공이 아닌 집합이다. 신기한 말이 많이 나오는데, 정말 그냥 유한하고
공이 아니면 그만인 아무 집합이다. 이를테면 아래는 이진 알파벳이다.

$$
\lbrace0,1\rbrace
$$

그리고 $\mathbb{C}^{\Sigma}$은 이와 같은 알파벳 $\Sigma$에서 $\mathbb{C}$로의
함수 $c:\Sigma\rightarrow\mathbb{C}$를 전부 모은 집합이다. 이렇게 만든 집합
$\mathbb{C}^{\Sigma}$는 알파벳의 크기 $|\Sigma|$만큼의 차원을 지니는 벡터공간을
일으킨다. 덧셈과 (스칼라) 곱셈만 정의되면 된다. 

- 벡터 $u,v\in\mathbb{C}^{\Sigma}$에 대해 $u+v\in\mathbb{C}^{\Sigma}$는 아래
방정식으로 정의된다.

    $$
    \forall a\in\Sigma, (u+v)(a)=u(a)+v(a)
    $$

- 벡터 $u\in\mathbb{C}^{\Sigma}$와 스칼라 $\alpha\in\mathbb{C}$에 대해 벡터 
$\alpha u\in\mathbb{C}^{\Sigma}$는 아래 방정식으로 정의된다. 

    $$
    \forall a\in\Sigma, (\alpha u)(a) = \alpha u(a)
    $$

(여기서 $u(a)$의 값은 $a$로 인덱스가 부여된 $u$의 성분(entry)을 나타낸다.
$u\in\mathbb{C}^{\Sigma}$가 벡터로서 함수라는 사실을 환기하라)

그리하여 덧셈 및 스칼라 곱셈이 정의된 $\mathbb{C}^{\Sigma}$를 <u>복소 유클리드 
공간(Complex Euclidean Space)</u>이라고 부른다. (여기에 무한의 개념을 도입해
더 일반화하면 힐베르트 공간이라고 부른다)

그런데 복소유클리드공간 $\mathbb{C}^{\Sigma}$가 $\mathbb{C}^n$와 동치인 이유는
무엇인가? 우선 알파벳 $\Sigma$가 유한하며 공이 아닌 집합이라는 사실을 돌이킨다.
이때 임의의 양의 정수 $n$이 알파벳의 크기 $|\Sigma|$와 같다면, $\lbrace 1,
\ldots,n\rbrace$상의 각 원소를 $\Sigma$상의 각 기호에 사상하는 함수가
아래처럼 존재할 수 있겠다.

$$
f:\lbrace1,\ldots,n\rbrace \longrightarrow \Sigma
$$

여기서 $\mathbb{C}^{\Sigma}$상의 임의의 벡터-함수 $u$의 각 성분을 $k\in\lbrace1,\ldots,
n\rbrace$에 대해 $\mathbb{C}^{\lbrace1,\ldots,n\rbrace}$상의 $u(f(k))$로 
일대일대응할 수 있다. 또한 $\mathbb{C}^{\lbrace1,\ldots,n\rbrace}$는 사실상 
$\mathbb{C}^n$이다. 따라서 복소유클리드공간 $\mathbb{C}^{\Sigma}$를 
$\mathbb{C}^n$으로 간단하게 나타낼 수 있다. 

다만 이 일대일대응이 와닿지 않을 수 있으니 예를 들면, 아래 같은 알파벳이 있다고
하자.

$$
\begin{aligned}
\Sigma&=\lbrace0,1\rbrace^2\\
        &=\lbrace00,01,10,11\rbrace
\end{aligned}
$$

이러한 $\Sigma$에서 $\mathbb{C}$로의 함수를 전부 모은 복소유클리드공간
$\mathbb{C}^{\Sigma}$상의 벡터-함수 $u$를 아래처럼 $\mathbb{C}^{n=4}$상의 벡터에
일대일대응한다.

$$
u=\begin{bmatrix}
\alpha_1\\ \alpha_2\\\alpha_3\\\alpha_4
\end{bmatrix}\mapsto
\begin{bmatrix}
u(f(1)) \\ u(f(2)) \\ u(f(3)) \\ u(f(4))
\end{bmatrix}
$$


$$
f:\lbrace1,2,3,4\rbrace\rightarrow\lbrace00,01,10,11\rbrace
$$

따라서 이처럼 복소유클리드공간 $\mathbb{C}^{\Sigma}$를 $\mathbb{C}^n$으로
축약하여 나타낼 수 있다. 

