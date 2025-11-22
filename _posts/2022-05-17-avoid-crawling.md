---
title: "내 웹사이트에 있는 이메일 크롤링 방지하기"
date: 2022-05-17 00:00:00 +0900
layout: post
category: "personal"
excerpt: "미션: 로봇의 레이더를 피하라"
lang: en
tags: [self-help group, coursework]
---

지난 해부터, 내 서울대 메일에 스팸메일이 많이 오기 시작했다. 이게 내 논문에서 크롤링 된건지, 아니면 내 웹사이트에 있는 서울대 주소로 메일을 쏘는건진 모르겠지만.. 어쨌든 계속 predatory journal이나 URGENT로 시작하는 스팸 메일이 많이 와서 여간 귀찮았던게 아니었다.

이에, 많은 연구자들이 이메일 주소를 `<a>` 태그를 쓰지 않고, `AAA at BBB dot CCC` 형식으로 적곤 하는걸 발견했다. 하지만, 이런 방식으로 이메일을 걸어버리면 딱히 가독성도 좋지 않고, `mailto:AAA@BBB.CCC` 형식의 하이퍼링크를 사용하는 것도 불가능해진다.

어떻게 하면 봇을 우회하면서도 이메일을 걸어놓을 수 있을까 고민하던 차에, Stack Overflow [^1]에서 좋은 방법을 하나 발견해서 공유한다:

**CSS 파일**
```css
.cryptedmail:after {
    content: attr(data-name) "@" attr(data-domain) "." attr(data-tld); 
}
```

**HTML 파일**
```html
<a href="#" class="cryptedmail"
    data-name="id" /* 이메일 아이디 적기 */
    data-domain="snu" /* 이메일 도메인 적기 */
    data-tld="ac.kr" /* 이메일 tld 적기 */
    onclick="window.location.href = 'mailto:' + this.dataset.name + '@' + this.dataset.domain + '.' + this.dataset.tld; return false;">
    <i class="fas fa-envelopes" style="margin-right: .3rem;"></i>
</a>
```

이렇게 표현하면, `id@snu.ac.kr`와 같은 형식을 가진 이메일 주소를 하이퍼링크까지 살리면서 크롤링은 불가능하게 첨부할 수 있다고 한다.

---
**Reference**

[^1]: Making email address safe from bots on a webpage. [https://stackoverflow.com/a/41566570](https://stackoverflow.com/a/41566570)
