---
title: "blueocean-plugin"
date: 2016-05-29 17:23:21
tags: github, github-trend, tech-trend 
---


![][image0]원피스는 내꺼임

반가운 얼굴이죠. 여러가지 CI 빌드 툴이 Jenkins의 아성을 위협하고는 있지만, pipeline 까지 집어 넣으면서 절치부심 새로운 버전을 준비하고 있는 jenkins 입니다.

Jenkins UX가 하지만 그닥 좋지 않다고 생각한 것은 저 뿐만이 아니라 개발자들도 그랬나 봅니다. blueocean은 젠킨스의 새로운 UX를 위한 프로젝트입니다.

2016/05/28 Editor's choice

[**jenkinsci/blueocean-plugin**  
_blueocean-plugin - Blue Ocean UI app_github.com][anchor0][][anchor1]

---

#### 설치하기

최근 Npm 및 레일즈 생태계를 보면서 아 dependency가 정말 복잡해졌어. 라고 여러군데 이야기를 했었죠.

정정하겠습니다.
    
    $ mvn clean install

을 실시하면 수도 없는 mvn 빌드 artifact들이 그 모습을 드러내며 경악 시킵니다. 뭐 하지만 상당히 놀라운 사실은 retry옵션 이 있어서 그나마 낫다는 사실.

하지만, Java 생태계의 강점은 안정성(응?) 이라 어쨌든 설치가 됩니다.

#### 실행하기
    
    $ cd blueocean-plugin  
    $ mvn hpi:run

로 실행을 하면 8080 포트로 Jenkins 가 뜹니다.

처음 접속하면 모두들 눈에 익은 플러그인 설치까지 할 수 있습니다.

![][image1]기다리면

![][image2]또 기다리면

![][image3]이런 화사한 화면을

일단은 파이프 라인 대시보드만 볼 수 있습니다.

어드민 프로그램으로 Job을 하나 만들어 보면

![][image4]

![][image5]

파이프 라인 첫 화면으로 들어올 수 있습니다.

세팅을 잘 하면 아래와 같은

![][image6]

또 아래와 같은

![][image7]

화면들을 볼 수 있다는데

아직은 Pipelines 밖에 보이지 않고 진행 중에 섭다가 지속적으로 일어나다 심지어는 admin패스도 날려 버려 더 진행이 안되는군요.

---

#### 그럼에도 불구하고

이쁘다! 라는 것을 알 수 있고, 거기에만 국한 되는 것이 아니라 Pipeline에 대한 UX를 한층 높였다는 점에서 일단 점수를 주고 싶네요.

UI 프레임 워크는 React를 사용했다고 합니다. ES6, React,NPM등을 언급합니다.

---

#### JDL

Jenkins 는 확장성을 높이기 위해 Jenkins Description Language라는 것을 제안했는데 React Component 기반이라고 하는군요.

#### Modern JavaScript toolchain

Jenkins는 개발자들이 ES6, React,NPM등을 사용할 수 있도록 툴 체인을 제공한다고 하네요.

#### Client side Extension points

Extension point 를 통해 플러그인을 연결할 수 있다고 하는데 여기도 온통 React 얘기군요.

#### Server Sent Events

[**Using server-sent events**  
_Developing a web application that uses server-sent events is quite easy. You'll need a bit of code on the server to..._developer.mozilla.org][anchor2][][anchor3]

SSE는 서버에서 보내는 이벤트를 받아 UI를 업데이트 하는 스펙인데 IE 말고는 모두 지원하는군요.

젠킨스를 사용하는 사람들은 SSE가 왜 필요한지는 다들 아실테죠.

---

Pipeline 이 잘 정의되기 시작하면 Continuous Delivery를 넘어 Devops 의 완성을 향해 갈 수 있죠. 훌륭한 프로젝트의 완성을 위해 꼭 주목해야 하는 프로젝트 입니다.

By [Keen Dev][anchor4] on [May 29, 2016][anchor5].

Exported from [Medium][anchor6] on May 31, 2017\.


[anchor0]: https://github.com/jenkinsci/blueocean-plugin "https://github.com/jenkinsci/blueocean-plugin"
[anchor1]: https://github.com/jenkinsci/blueocean-plugin
[anchor2]: https://developer.mozilla.org/en-US/docs/Web/API/Server-sent_events/Using_server-sent_events "https://developer.mozilla.org/en-US/docs/Web/API/Server-sent_events/Using_server-sent_events"
[anchor3]: https://developer.mozilla.org/en-US/docs/Web/API/Server-sent_events/Using_server-sent_events
[anchor4]: https://medium.com/@keendev
[anchor5]: https://medium.com/p/4423d3f0cd31
[anchor6]: https://medium.com


[image0]: /images/1*QlzquCP6oJP1XqYLcI011w.png
[image1]: /images/1*c4sAHrcEQb6fOF04AcKT-w.png
[image2]: /images/1*gR0PDhhWDG2Mt59d6mmzYA.png
[image3]: /images/1*dTsvjG_rXfIQXBtViZssMQ.png
[image4]: /images/1*XHeiBr0fu7MuIhTE_1B_bw.png
[image5]: /images/1*IKuKtsAM0VUzdaacJd-E0w.png
[image6]: /images/1*gPROwsUOvM69MzylzlcPNw.png
[image7]: /images/1*yMv5noPz12rzM_9pY8KT7A.pn