---
title: "angular-styleguide"
date: 2016-04-11 07:01:18
tags: github, github-trend, tech-trend 
---


![][image0]

모든 언어를 배울 때 그 언어의 철학을 배우고 경험에서 얻은 실수를 피하는 방법들을 빨리 나의 것으로 만드는 방법이 있습니다. ( 공부에 왕도가 어딨어! )

바로 style guide 를 참조하는 것입니다. 실제로 airbnb 의 스타일 가이드는 30K 이상의 star를 받았습니다.

여기 angular의 스타일 가이드를 정리해 놓은 프로젝트가 있습니다.

2016/04/11 editor's choice

[**johnpapa/angular-styleguide**  
_There are multiple versions of Angular, and thus there are multiple versions of the guide. Choose your guide..._github.com][anchor0][][anchor1]

angular1,angular2 모두 정리가 되어 있고 angular2는 draft 중이라고 합니다.

---

#### angular란?

![][image1]

Javascript web framework 중에 하나로 google이 만들어 2015년 내내 최고의 화제가 된 프로젝트입니다. 그 전에 수 많은 프로젝트가 있었지만 angular가 가지고 나온 client-side의 MVC패턴만큼 정교한 프로젝트는 드문 마스터 피스. 비슷한 프로젝트로는 ember.js 가 있으며 backbone.js, underscore.js 같은 프로젝트가 영향을 주었다고 보여집니다.

이후 facebook에서 만든 react와 함께 개발자 커뮤니티를 양분중입니다.

angular2 가 조만간 나올 생각이며 추종자들에게는 angular2 가 나오면 모든 논란을 종식 시킬 것이다. ( 어떤 프레임워크가 최고냐!) 라는 기대를 한 몸에 받고 있지만, 필자의 생각에는 angular1과의 호환성 문제로 충공깽스런 사태도 나올 수 있어 보입니다.(이미 그런 조짐이!)

---

#### 스타일가이드란?
> 
> A **style guide** (or **manual of style**) is a set of standards for the writing and design of documents, either for general use or for a specific publication, organization, or field. (It is often called a **style sheet**, though that term has other meanings.)

... wiki

위키에 따르면 글을 작성하는데 있어서 표준 같은 역할을 하고 있습니다. 모든 개발 프로젝트에는 이 스타일가이드가 필요합니다. 이 스타일 가이드가 주는 이점은 다음과 같습니다.

1. 코드의 가독성 --- 같은 스타일을 따르는 코드를 볼 때면 어떻게 동작하는 지, 또한 어떻게 고쳐야 할지 등을 손 쉽게 정리할 수 있습니다.
2. 유지보수 용이성
3. 커뮤니케이션
4. 잦은 실수로 부터의 탈출
5. 각 언어별 syntax에 대한 빠른 이해

특별히 github에 올라오는 많은 프로젝트들은 훌륭한 표준들을 갖고 있으니 관심을 가지고 보시면 개인의 improvement에 큰 도움이 될 듯합니다.

---

#### angular style guide

양이 많으니 하나의 예를 들어볼까 합니다.

angular에는 directive 라는 녀석이 있습니다. 커스텀 태그 같은 역할을 하는 녀석인데 일단 봅시다.

![][image2]
> 
> directive는 파일별로 하나만 만들어야 함

> 이유1: 하나의 파일에 모든 directive들을 집어 넣기는 간단하지만 그러고 나면 앱간, 모듈간 공유하기가 어렵다

> 이유2: 유지보수가 정말 어렵다!

정도 쯤 될 거 같습니다!

많은 선행 개발자들의 노하우를 하나의 문서를 정독함으로써 얻을 수 있다면 저라면 꼭 즐겨찾기 해 두겠습니다!

![][image3]

다른 글이지만 angular style guide 에 대해 잘 소개해 둔 블로그를 소개합니다.

[**\[번역\] AngularJS 스타일 가이드 소개**  
_이 글은 Francesco Iovine의 An Introduction to AngularJS Style Guides 를 한국어로 번역한 것입니다. 오역 제보나 더 나은 번역 제안은 언제나 감사합니다! 스타일 가이..._hyunseob.github.io][anchor2][][anchor3]

By [Keen Dev][anchor4] on [April 10, 2016][anchor5].

Exported from [Medium][anchor6] on May 31, 2017\.


[anchor0]: https://github.com/johnpapa/angular-styleguide "https://github.com/johnpapa/angular-styleguide"
[anchor1]: https://github.com/johnpapa/angular-styleguide
[anchor2]: http://hyunseob.github.io/2016/04/10/introduction-to-angularjs-style-guide/ "http://hyunseob.github.io/2016/04/10/introduction-to-angularjs-style-guide/"
[anchor3]: http://hyunseob.github.io/2016/04/10/introduction-to-angularjs-style-guide/
[anchor4]: https://medium.com/@keendev
[anchor5]: https://medium.com/p/ee6152a8ed60
[anchor6]: https://medium.com


[image0]: /images/1*icnJ3FoW27Gm53Qc2lN_Cg.png
[image1]: /images/1*fcHxv_kCyn6ry1OTh_OKcw.png
[image2]: /images/1*FdfCsmlfk-CVVRU1ZmZlgg.png
[image3]: /images/1*EP9dMQlegaHPFei0lD1mLg.pn