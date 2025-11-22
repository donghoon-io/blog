---
title: "지난 3년간의 박사과정을 돌아보며"
date: 2025-11-21 00:00:00 +0900
layout: post
category: "personal"
excerpt: Translational science 연구자 3년차(?) 후기
lang: en
---

박사과정을 시작한 직후, 내 연구 분야를 논의하기 위한 첫 미팅에서 지도교수는 이렇게 물었다.

> **교수**: 너는 어떤 연구를 하고싶어?

> **나**: 저는 못생긴 디자인을 보면 화가 나요. 디자이너를 돕고 싶고, creativity support tool을 하고 싶은데, 솔직히 아무도 안 쓰는 툴은 만들고 싶지 않아요.

> **교수**: 그럼 너 혹시 translational science라고 들어봤어? 마침 이번에 Lucy가 AI2에서 유덥 교수로 임용됐는데, 코어드바이징 해달라고 하자.

그렇게 나는 순식간에 translational science 연구자가 되어버렸다.

## Translational science란?

Translational science, 한국말로 ‘중개연구’는 원래 의학에서 시작되었다. 의학 연구자들은 (케이스 스터디가 아닌 이상) 엄밀함을 갖추기 위해 필연적으로 일반화된 지식을 만들게 된다. 반면 임상가는 이러한 지식을 케이스 바이 케이스로 적용해야 하며,[^1] 이 과정에서 자연스레 **엄밀성과 관련성의 간극(rigor–relevance gap)**이 생긴다.

따라서 연구와 실재 사이를 **중개(translate)**해주는 매개체가 필요하게 된다.

그렇다면 HCI에서는 누가 이러한 ‘수행가(practitioner)’일까? 바로 디자이너다. 컴퓨터과학자나 전기공학자가 만든 기술이 실제로 사용자에게 닿기 위해서는, 결국 디자이너가 이를 가공하고 재해석해야 한다. 그러나 낮은 층위의 기술적 지식은 디자이너에게 접근하기 어렵고, 이 과정에서도 다양한 간극이 생긴다.

Colusso *et al.*[^2] 에 따르면, 연구가 실재로 변환되는 과정은 다음과 같이 구분할 수 있다:

1. **기초 연구**: 사람·기술·디자인에 대한 근본적인 이해
2. **응용 연구**: 실질적 문제를 해결하기 위한 목표 지향 연구
3. **디자인 실무**: 제품·서비스를 만드는 단계

이 과정에서, 대표적으로 다음과 같은 간극이 생긴다:

1. **기초 연구 → 응용 연구**: 정보 과부하, 기술 부족
2. **기초 연구 → 디자인 실무**: 이해의 어려움, 접근성 부족
3. **응용 연구 → 디자인 실무**: 실용성 부족
4. **디자인 실무 → 연구 (역류)**: 가끔 디자이너는 실무로부터 이론을 만들어내기도 하지만, 이건 여간 귀찮은 일이 아니다

![translationl science model](/blog/assets/images/posts/translational_science_model.png)

<p class="caption">Translational Science Model in HCI (CHI '19)</p>

나는 이 간극을 닫는 일을 하는 연구자가 되기로 하였다.

## 내 접근법

다른 연구자들도 그렇듯, 한 사람이 한 분야의 모든 연구를 전부 다룰 수는 없다. 내가 집중한 영역은 다음과 같다 (내가 1저자로 진행한 연구들만 포함한다):

### 1. **기초 연구 → 디자인 실무**

#### 1-(i) 논문 포맷을 바꿔버리기

![alt text](/blog/assets/images/posts/paper2card.jpg)
<p class="caption">Paper2card (CHI '24)</p>

많은 디자이너에게 논문은 불필요한 서론과 너무 전문적인 설명으로 가득 찬 낯선 세계다. 대신에, HCI에선 디자이너들이 ‘카드’ 형식으로 정보를 교환하는 오랜 전통이 있다. 그래서 나는 논문을 디자이너에게 익숙한 카드 기반 구조로 재편해보려 했다.

2024년에 소개된 Paper2Card[^3] 연구에서, 내가 개발한 시스템은 논문의 핵심 주장과 디자인 가이드라인을 뽑아내 디자이너가 “필요한 정보만 빠르게 소비하도록” 도와준다. 이를 통해 연구자와 실무자 사이에 놓인 ‘형식’의 장벽을 없애려고 했다. 이는 단순한 요약을 넘어, “논문을 어떻게 재구성해야 실무가 실제로 쓸 수 있을까?”라는 질문에 대한 첫 구조적 시도였다.

![alt text](/blog/assets/images/posts/papertok.jpg)
<p class="caption">PaperTok (in submission)</p>

HCI 내 디자이너들에게 카드가 어떠한 '메타포'로 작용한다면, 영상은 디자이너가 아니더라도 많이 소비되는 인기있는 미디엄이다. 그러나 영상 제작은 연구자에게 너무 어려웠다. 그래서 나는 AI가 논문 내용을 분석해 대중 친화적 스크립트 + 텍스트-투-비디오 스토리보드를 자동 생성하는 시스템인 PaperTok[^4]을 만들었다.

PaperTok은 “AI가 대신 만든 콘텐츠”가 아니라, 연구자가 ‘감독’처럼 AI가 만든 초안을 다듬는 새로운 협업 구조를 제시한다. 평가 결과, PaperTok으로 만든 영상은 기존 PDF-to-video 방식보다 훨씬 몰입도가 높았다. (비록 디자이너에게만 국한된 연구는 아니었지만) 이 연구는 학술 지식이 새로운 매체로 진화하여 디자이너에게 도움이 될 방식을 제시하며, AI가 연구 커뮤니케이션의 미래에서 어떤 역할을 해야 하는지 질문을 던진다.


#### 1-(ii) 논문을 디자인 툴 (e.g., 피그마)과 합체시켜(?) 버리기

![alt text](/blog/assets/images/posts/refine.jpg)


<p class="caption">ReFinE (in submission)</p>

나는 궁극적으로, 이러한 연구 지식이 따로 노는게 아니라 마치 플러그인처럼 디자인 도구 속에서 (e.g., Figma) 살아 움직이길 원했다. 그래서 나는 HCI 논문들을 Figma에 통합해, 특정 UI 화면을 클릭하면 해당 문맥에 맞는 디자인 가이드라인을 자동으로 찾고 변환하여 제안해주는 ReFinE[^5]를 만들었다. 디자이너는 더 이상 논문을 ‘찾을 필요’가 없고, 툴 속에서 연구가 먼저 다가오도록 하는 것이 목표였다.

![alt text](/blog/assets/images/posts/postermate.jpg)

<p class="caption">PosterMate (UIST '25)</p>

연구는 ‘학술 연구’에만 국한되는 것이 아니다. 기업들 또한 수많은 리포트 혹은 마케팅 문서를 만들고, 이를 내부적으로 소비한다. 이 또한 연구라고 할 수 있다. 하지만, 이 또한 논문과 똑같은 문제점 (변환의 어려움)을 겪는다.

이를 위해, 나는 PosterMate[^6]라는 시스템을 만들었다. PosterMate는 기업 리포트를 바탕으로 소비자를 구성하고, 소비자들을 마치 살아 움직이는 ‘페르소나’ 형식으로 만들어 페르소나의 시각을 시뮬레이션해 디자인 의사결정을 더 설득력 있게 만드는 툴이다. AI와 디자이너가 함께 기업 내부의 연구 결과를 바탕으로 ‘다양한 관객’을 모의해 디자인을 다듬는 것이다.

### 2. **응용 연구 → 디자인 실무**

#### 2-(i) 논문을 개인의 상황에 맞게 contextualize하기

![alt text](/blog/assets/images/posts/paper2personalization.jpg)

<p class="caption">What About My Design Context? (DIS '25)</p>

이 툴을 우리 과 디자이너 친구에게 보여주니, 그 친구가 이렇게 물었다: “그래서 이 툴이 내가 지금 하는 프로젝트에는 어떤 도움이 되는데?”

이 필연적인 ‘문맥의 간극’을 해소하기 위해, 나는 LLM을 활용해 연구 내용을 디자이너 개인의 컨텍스트에 맞게 자동으로 개인화하는 시스템을 만들었다.

실험 결과, 디자이너들은 이런 개인화된 내용이 기존 연구 내용보다 훨씬 더 관련성 있고, 실현 가능하고, 동기부여가 된다고 평가했다. 즉, AI가 “연구의 언어를 실무의 언어로 번역하는 도구”가 될 수 있다는 것을 보여준 것이다.

### 3. **디자인 실무 → 연구 (역류)**

#### 3-(i) Microtheory 만들기 돕기

![alt text](/blog/assets/images/posts/cpd.jpg)

<p class="caption">AI-assisted Causal Pathway Diagram (CHI '24)</p>

Colusso *et al.*이 제시했듯, 이론은 디자인 실무에서 새롭게 태어나기도 한다. 그래서 우리는[^7] 디자이너가 스스로 본인의 상황에서 디자인 이론을 만들고, AI가 그 구조를 보완하며, 디자인 팀이 문제를 더 깊게 이해하도록 돕는 시스템을 만들었다. 이 연구는 “AI가 창의성을 억누르는 것이 아니라, 오히려 구조적 사고를 강화하고 확장할 수 있다”는 가능성을 보여줬다는 측면에서 의의가 큰 연구였다.

## 느낀점

### 내 연구분야가 생겼다는 기쁨

돌아보면, 나는 늘 흥미가 끌리는 대로 연구를 해왔다. 접근성 연구, 멘탈헬스, 챗봇 등 그때그때 의미 있어 보이는 주제를 따라갔지만, 정작 “너의 연구 분야가 뭐야?”라는 질문 앞에서는 늘 망설였다. 퍼즐 조각들이 흩어진 듯했고, 나는 무엇을 하는 연구자인지 스스로도 확신하지 못했다.

그런데 translational science를 만나고 나서부터 그 조각들이 서서히 맞춰지기 시작했다. 비로소 나를 설명하는 언어가 생긴 것이다. 논문은 왜 실무로 가지 않는가? 디자이너는 왜 연구를 활용하기 어려운가? 왜 연구와 현실은 여전히 서로를 이해하지 못하는가? 나는 오래전부터 이 질문들을 쫓아왔다는 걸, 뒤늦게 깨달았다. 내가 했던 모든 연구의 공통된 축은 바로 “연구가 현실로 흘러가는 과정”이었다.

며칠 전, 지도교수와 내가 했던 대화가 생각난다:

> **나**: 요즘 아무나 LLM 연구 하니까 불안해요. HCI 연구자들에게 ‘연구 주제’란게 과연 존재하긴 하는 걸까요?

> **교수**: 너는 LLM 연구자가 아니야. 너는 10년 전에도 crowdsourcing 연구자가 아니었을꺼야. 너는 translational science 연구자야. 무슨 말인지 알겠어?

### 일관성의 소중함

박사과정을 하면서 느낀 점은 바로 의미있는 연구를 추구하는 것의 중요성이다. 내가 종종 유덥의 슈퍼스타 [재욱](https://jaewook-lee.com/)이랑 우스갯소리로 하는 얘기가 있다:

> 우리 학부 때보다 내는 논문 개수가 절반이 줄어들었어ㅋㅋ

사실이다. 우리 둘 다 학부 때는 미친 듯이 논문을 쏟아냈고, 그게 좋은 일이라고만 생각했다. 생각해보면 지금도 논문을 다작<sup>多作</sup>하려고 하면 할 수 있을 것 같다. 하지만 지금은 유명한 지도교수 이름에 먹칠하지 않으려 좀 더 신중하게 논문을 내고 있고, 이에 자연스럽게 개수가 줄어들어 버렸다.

물론 논문을 많이 쓰든, 적게 쓰더라도 의미 있게 쓰든 그건 각자의 선택이다. 다만 내 개인적인 경험으로는, 적더라도 일관성 있게 내는 것이 오히려 자신의 가치를 높이는 데 더 도움이 됐다. 실제로 지금은 예전처럼 다작하지는 않지만, 회사 면접을 하거나 톡을 갈 때 내 연구를 더 자신 있게 이야기할 수 있고, 이에 다른 사람들도 예전보다 내 연구의 가치를 더 높게 본다는 걸 확실히 느낀다.



### (번외) PDF의 문제점

논문을 읽는 데는 획일화된 PDF 형식이 편하다. 하지만 읽는 것 말고 활용을 하려는 순간, PDF는 연구자와 디자이너 모두에게 가장 큰 장벽이 된다. PDF는 ‘보여주는’ 데 최적화된 형식이지, 프로세싱 하는 데에는 최악의 형식이기 때문이다. 연구를 카드로 바꾸고, 디자인 툴로 옮기고, 실무 맥락에 맞춰 재구성하는 모든 과정에서 가장 먼저 부딪히는 벽이 바로 PDF였다.

결국 우리는 컴퓨터 비전으로 PDF를 분해하고, 그걸 다시 XML 구조로 복원하는 우회로를 선택해야 했다. ACM DL이 XML 제출을 의무화한 지 꽤 되었지만, 현실에서 모든 논문이 XML로 제공되는 것도 아니고, ACM 바깥으로 나가면 그마저도 소용이 없다. 마치 연구를 더 잘 쓰고, 더 잘 나누고, 더 잘 활용할 수 있는 수많은 방법들이 PDF라는 단단한 벽 앞에서 멈춰 서는 느낌이다.

그래서 언젠가 논문이 PDF라는 껍질에서 벗어나 처음부터 ‘활용 가능성’을 전제로 만들어지는 시대가 오기를 기대한다.

---
**Reference**

[^1]: Shin, D., Chen, T. Y., Hsieh, G., & Wang, L. L. (2025). What About My Design Context?: Exploring the Use of Generative AI to Support Customization of Translational Research Artifacts. In *Proceedings of the 2025 ACM Designing Interactive Systems Conference*.

[^2]: Colusso, L., Jones, R., Munson, S. A., & Hsieh, G. (2019). A Translational Science Model for HCI. In *Proceedings of the 2019 CHI Conference on Human Factors in Computing Systems*.

[^3]: Cristobal, M. R.\*, Byeon, H.\*, Chen, T.\*, Shang, R.\*, Shin, D.\*, Zhong, R.\*, Zhou, T.\*, & Hsieh, G. (2026). PaperTok: Exploring the Use of Generative AI for Creating Short-form Videos for Research Communication. (\* equal contribution)

[^4]: Shin, D., Wang, L. L., & Hsieh, G. (2024). From Paper to Card: Transforming Design Implications with Generative AI. In *Proceedings of the 2024 CHI Conference on Human Factors in Computing Systems*.

[^5]: Shin, D., Guo, B., Lee, J., Wang, L. L., & Hsieh, G. (2025). ReFinE: Streamlining UI Mockup Iteration with Research Findings.

[^6]: Shin, D., Lee, D., Hsieh, G., & Chan, G. Y. Y. (2025). PosterMate: Audience-driven Collaborative Persona Agents for Poster Design. In *Proceedings of the 38th Annual ACM Symposium on User Interface Software and Technology*.

[^7]: Zhong, R.\*, Shin, D.\*, Meza, R., Klasnja, P., Colusso, L., & Hsieh, G. (2024). AI-Assisted Causal Pathway Diagram for Human-Centered Design. In *Proceedings of the 2024 CHI Conference on Human Factors in Computing Systems*. (\* equal contribution)