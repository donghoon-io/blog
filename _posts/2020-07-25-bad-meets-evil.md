---

title: "개발자와 디자이너가 협업하기"
date: 2020-07-25 11:00:00 +0900
slug: bad-meets-evil
layout: post
category: "development"
excerpt: "남북경협보다 어려운 개발자-디자이너 협업"
lang: en
tags: [design, dev, collaboration]
---

지난 2020년 봄학기, 나는 디자인 사고와 커뮤니케이션이라는 수업을 수강하였다. 어느정도 디자인에 대한 로망이 있었던 것도 한 몫 했겠지만, 그보다 더 큰 목적은 따로 있었다. 바로 '개발자 입장에서 디자이너를 더 잘 이해하기 위해서'였다.

## 달라도 너무 다른 디자이너와 개발자

어떤 프로젝트를 진행할 때, 구성원은 개발자, 디자이너, 그리고 기획자로 구분하는 것이 일반적이다. 개발자는 말 그대로 코더이고, 디자이너는 (당연하게도) 심미적/기능적인 설계를 하는 사람이다. 가끔 '데이터 애널리스트' 등의 거추장스러운 말로 나머지 사람들을 구분짓기도 하지만, 경험적으로 이런 역할들은 큰 방향성을 제시하는 데에 (기획) 목적이 있기 때문에 나머지 사람들을 통째로 '기획자'라고 부르곤 한다.

그런데, 각 구성원은 달라도 너무 다른 것 같다. 아무래도 각각의 역할을 가진 사람들이 꽤나 다른 목적을 추구하기 때문에 (디자이너: 심미성 및 기능성, 개발자: 구현, 기획: 사용 전반), 서로를 이해하기 어려운 상황이 자주 생기는 것 같다. 당연히 나는 개발자라 개발자의 입장을 더 잘 공감하는 편이다. 특히나, 안드로이드나 iOS는 각각의 디자인 철학을 바탕으로 한 디자인 가이드라인을 제시하는데, 이러한 constraint와 디자이너의 철학이 가끔 충돌할 땐 개발자는 상당히 곤란해진다 (도날드 노먼이 말한 그 constraint 맞다).

![evil-designer](/images/posts/bad-meets-evil-1.jpg)

<p style="text-align: center; font-weight: 500; padding-top: 0 !important">Figure 1. 가끔 디자이너는 iOS 개발자에게 머터리얼 디자인을 강요하곤 한다</p>

그런데 가끔 금융 앱을 보거나 크로스-플랫폼 툴을 이용해서 개발된 앱을 보면, 디자이너가 불쌍해지기도 한다. 디자이너는 하나의 요소, 하나의 컬러 손수 비교해가며 맞춰놨는데, 이렇게 개발자가 귀차니즘 때문에 막 적용하는 경우가 생기기 때문이다. 마치 iOS 개발자가 밤을 새가면서 native 앱을 개발했는데, 안드로이드 외주를 추가로 주는게 더 비싸서 리액트 네이티브 개발자에게 iOS까지 동시에 맡겨서 iOS 네이티브 앱이 쓸모 없어진 느낌일 것이다..

![evil-developer](/images/posts/bad-meets-evil-2.jpg)

<p style="text-align: center; font-weight: 500; padding-top: 0 !important">Figure 2. 가끔 개발자는 색깔을 구별하지 못하곤 한다</p>

## 개발자-디자이너 협업을 위한 툴이 있을까?

있다. Zeplin이나 Figma와 같은 디자인 프로토타이핑 툴에는 대부분 개발자가 쉽게 코드화할 수 있도록 해당 요소를 코드로 변환해주는 툴이 있다. 이를 통해, 색상, 폰트 크기, 간격 등 개발자가 놓치기 쉬운 부분을 정량화하여 교환할 수 있다.

![zeplin-extension](/images/posts/bad-meets-evil-3.png)

<p style="text-align: center; font-weight: 500; padding-top: 0 !important">Figure 3. 제플린의 각 요소를 클릭하면 기본적인 컬러, 폰트 등을 export 할 수 있는 extension이 존재한다</p>

하지만 이것도 정말 제한적인게, 오히려 디자인을 하면 예상과 다르게 나오는 경우가 너무 많다. 그리고 나같은 개발자는 코드보단 스토리보드에서 constraint 맞춰가며 매뉴얼하게 디자인을 하는 것을 선호한다. 왜냐하면 최근들어 iOS 디바이스 레이아웃이 수도 없이 많아져서 코드로만 디자인을 적용하면 분명 만족하지 못하는 경우가 생기기 때문이다. 근데 이럴 경우에는 위의 제플린 익스텐션이 딱히 쓸모가 없어진다..

## 그러면 답은 뭘까?

서론에서도 얘기했지만, 결국 상대방에 대해 좀 더 공부하는 것과 같은 방식으로 '둘다 이해를 잘 하는 수'밖에 없는 것 같다. 너무 비관적인 해결책이지만, 개발자는 디자인을 배워가며 디자이너의 니즈를 이해하고, 디자이너는 개발자가 받아들이기 힘든 부분을 파악하는 것이 궁극적인 해결책이기 때문이다.

사실 디자이너들이 협업이 너무 답답해서 직접 개발을 배워보려고 하는 걸 많이 봤다. 그럴 때마다 추천하는 [강의](https://www.inflearn.com/course/stanford-ios-%ED%95%9C%EA%B8%80%EC%9E%90%EB%A7%89-%EA%B0%95%EC%9D%98)가 있는데, 너무 쉽게 가르쳐서 이해가 쏙쏙 잘 되고 iOS 개발 자체가 디자인과 너무 연관되어 있어서 적극 추천한다 (앱개발 특성상 프로덕트도 바로바로 나오는 편이고). 반대로 개발자들도 [D3.js](https://d3js.org/), [plotly](https://plotly.com/), 아니면 [Tableau](https://www.tableau.com/)로라도 간단한 시각화라도 해보면서 상대방의 고충을 깨달아 가는게 궁극적이면서도 훈훈한(?) 해결책이라고 생각한다.