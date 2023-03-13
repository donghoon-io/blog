---

title: "페이퍼에 피규어를 해상도가 깨지지 않게 넣기"
date: 2020-09-24 00:00:00 +0900
layout: post
category: "research"
excerpt: "해상도가 깨지지 않고, 글자가 선택 가능한 피규어 만들어서 내 논문에 넣기"
lang: en
tags: [research]
---

페이퍼를 쓰다 보면 피규어 (figure; 삽화)를 넣어야 하는 일이 종종 생기곤 한다. 나는 지난 페이퍼를 기준으로 8개의 피규어를 넣었고, 이번 카이는 총 5개의 피규어를 만들어서 넣었다. 물론 어떻게 하면 피규어를 통해 독자로 하여금 잘 페이퍼를 이해하게 할 것인가도 중요한 문제지만, 피규어를 '어떻게' 만드느냐도 상당히 중요한 일이다. 특히, 페이퍼 타임라인이 급박해질수록 피규어는 마치 계륵(?)같은 존재가 되어버린다.

이렇게나 많은 피규어를 만들면서, 디자인 적으로도 어떻게 해야할지 많은 것을 느꼈지만, 지난 페이퍼에서 내가 가장 크게 실수한 부분은 피규어를 vector 바탕의 pdf (ai, svg 등도 포함)으로 넣지 않았다는 것이다. 이게 왜 문제냐면, 크게 확대를 하면 피규어가 깨져보인다. 게다가, 피규어 내에도 텍스트가 많을 수 있는데 (e.g., description, 그래프의 legend), 이미지로만 되어있어 온라인에서 피규어 description을 통한 내 논문으로의 유입을 막는다.


![text-drage](/images/posts/low_res.jpg)

<p style="text-align: center; font-weight: 500; padding-top: 0 !important">Figure 1. [이전 내 논문](https://dl.acm.org/doi/10.1145/3313831.3376154). 확대를 하면 이렇게 깨져보이고, 글자도 선택이 불가능하다</p>


그런데 기존에는 몰랐지만 새 논문을 위해 literature review를 하던 도중, 다른 논문에서 피규어 내의 글자를 선택하는 것이 가능하다는 것을 알게되었다. 아래와 같이 확대를 아무리 해도 (vector 기반이기 때문에) 아주 선명하고, 심지어 텍스트를 드래그하는 것도 가능하다..! 어떻게 하는 것일까?

![text-drage](/images/posts/high_res.jpg)

<p style="text-align: center; font-weight: 500; padding-top: 0 !important">Figure 2. 이번 해부터 내가 적용하는 방식으로 만든 figure. 페이퍼를 확대해도 깨지지 않고, 심지어 텍스트를 선택하는 것도 가능하다. Horray!</p>

## 0. Prerequisite

사전지식으로, 기본적인 일러 지식이 있어야 한다.

## 1. Save figure as PDF

본인이 피규어를 디자인한 곳에서 디자인 파일을 pdf, svg, ai 등의 vector가 살아있도록 하는 형식으로 export한다. 예를 들어, 데이터를 이용하여 excel에서 figure을 만들었다면, 이를 오른쪽 클릭하여 그림으로 저장 옵션을 선택하고, 파일 형식을 pdf로 지정하여 저장한다. 후술할 illustrator 작업에서 구체적인 편집을 할테니, rough한 선에서 저장해도 상관이 없다.

![pdf-figure](/images/posts/high_res_pdf.jpg)

<p style="text-align: center; font-weight: 500; padding-top: 0 !important">Figure 3. 이렇게 이쁜(?) pdf가 생성되었다!</p>

## 2. Import PDF to illustrator

이전 단계에서 생성한 pdf 파일을 일러스트레이터에서 불러온다. 다음과 같은 화면처럼 이미지를 불러올 것이다. 요소들 중에 vector이 아닌 scalar 형식의, 확대하면 깨져보이는 이미지들이 몇개 있을 수도 있다. 그런 이미지들은, 선택하여 일러의 **추적** 옵션을 이용해 모양을 딴다. 그 다음, scalar 형식과 동일하게 색 등을 추가하여 vector 형식으로 요소를 만든다.

또한, (그래프의 경우) 엑셀에서 그래프를 그리면 대체로 legend가 이쁘지 않을 것이다. 이를 보완하기 위하여, 추세선 등은 엑셀에서 준대로 그대로 놔두고 legend의 텍스트 font-family, 크기 등을 수정한다. 이를 통해, 보다 가독성 높은 그래프를 만들어나간다.

![ai-figure](/images/posts/high_res_ai.jpg)

<p style="text-align: center; font-weight: 500; padding-top: 0 !important">Figure 4. 일러스트는 아무리 오래 배워도 써먹기 힘든 툴 중에 하나이다</p>

## 3. Save as PDF

이렇게 자잘한 부분을 수정하였다면, 해당 파일을 pdf 형식으로 저장한다. 잘은 모르겠지만, 내가 페이퍼를 쓰는 환경 (Overleaf, 그러니까 XeLatex)에서 이미지는 기본적으로 jpg, png 등의 일반적인 확장자가 아니면 pdf를 지원한다. 만약 더 알아보고 svg 등도 가능하다면 그런 형식도 괜찮다.

그 다음 figure에 jpg 불러오듯 pdf 파일을 넣고, 피규어 넣을 자리에 includegraphics를 해서 넣는다. 그러면 아래와 같이, 확대해도 깨지지 않는 (어마어마한 잠재력을 가진) 피규어가 내 논문에 쏘옥 들어가있을 것이다.

![complete](/images/posts/high_res_complete.jpg)

<p style="text-align: center; font-weight: 500; padding-top: 0 !important">Figure 5. 완성본. 참 쉽죠?!</p>