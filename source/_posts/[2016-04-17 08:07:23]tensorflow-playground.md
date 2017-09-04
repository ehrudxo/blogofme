---
title: "tensorflow-playground"
date: 2016-04-17 08:07:23
tags: github, github-trend, tech-trend 
---


![][image0]

이제 좀 식은 거 같아서 오랜만에(?) neural network 관련된 프로젝트를 공유합니다. 여러번 리뷰를 하긴 했는데 많은 분야에서 tensorflow 는 활용되고 있고 그 이후 거의 AI프로그램 플랫폼이 되어 가고 있습니다. 오늘은 tensorflow를 이용한 visualization 툴인 playground 입니다.

2016/04/17 Editor's choice

[**tensorflow/playground**  
_playground - Play with neural networks!_github.com][anchor0][][anchor1]

### 설치

일단 git clone을 통해 프로젝트를 받습니다.
> 
> $git clone [https://github.com/tensorflow/playground][anchor1]

이후 npm install을 통해 모듈 dependency 를 완성합니다.
> 
> $cd playground &&npm install

dependency는 다음과 같습니다.
> 
> "devDependencies": {  
> "typescript": "^1.8.7",  
> "typings": "^0.7.9",  
> "uglify-js": "^2.6.2",  
> "tsify": "^0.14.1",  
> "watchify": "^3.7.0",  
> "http-server": "^0.9.0"  
> },  
> "dependencies": {  
> "catw": "^1.0.1",  
> "d3": "^3.5.16",  
> "material-design-lite": "^1.1.3",  
> "seedrandom": "^2.4.2"  
> }

---

실행 시키고 나면 포스팅 상단의 이미지가 나옵니다.

이게 무엇인고? 하시는 분이 있을 거 같아서 부연설명을 드리자면, 파랑색은 positive value 를, 오렌지는 negative value를 나타냅니다. 숨겨진 레이어는 neural network를 배치해 각 점들의 집합군들을 잘 묶어 판단하게 하고 예측도 할 수 있게하는 역할을 합니다. (_이게 다 무슨 말이야!_)

먼저 hidden layer를 하나만 놓고 돌려보겠습니다.

두번째 데이타 샘플이 흥미롭네요. (_4번째 샘플은 충공깽)_

링크 거는 첫번째 동영상은 히든 레이어를 하나만 두고 작업을 해 본 케이스 입니다.

보시면 하단 좌측에서 상단 우측으로 갈라지면서 neural network가 판단을 하는 것을 보실 수 있습니다.

레이어 두개를 더 추가한 부분을 보면 약간 더 명확해 지는데요

세개의 레이어가 되니 약간 더 정교한 분류를 하기 시작합니다.

4번째 샘플인

![][image1]

이미지가 neural network 가 어떻게 동작하는지 돌려보다가 지금의 방식으로는 쉽게 그림이 완성되지 않는 다는 흥미로운 것을 발견하고는 macbook air를 바꾸면 좀 더 좋아질까 생각해 봤지만 최적화 하는 것이 레이어를 많이두는것과 input 값을 정의하는 방법이 중요하다는 것에 대한 사실에 경외감이 느껴지네요.

input 값을 sinx,siny 까지 추가해 보니 다음과 같은 정도의 결과를 확인해 볼 수 있네요.

![][image2]

사람이 봤을때 생각할 수 있는 나선형의 결과를 기대했는데 그렇게는 되지 못하더라도 대강의 이해할 만한 수준의 그림이 나오네요.

Iteration과 layer를 무작정 많이 그린다면 더 좋은 결과를 얻을 수 있겠다는 생각이 듭니다.
> 
> neural network 이 어떻게 동작하는지를 이해하는데 정말 좋은 도움을 줄 수 있는 프로젝트라고 생각됩니다.

By [Keen Dev][anchor2] on [April 16, 2016][anchor3].

Exported from [Medium][anchor4] on May 31, 2017\.


[anchor0]: https://github.com/tensorflow/playground "https://github.com/tensorflow/playground"
[anchor1]: https://github.com/tensorflow/playground
[anchor2]: https://medium.com/@keendev
[anchor3]: https://medium.com/p/9be777ba26d6
[anchor4]: https://medium.com


[image0]: /images/1*5zC5ZE-3W78FdlF_avwAkg.png
[image1]: /images/1*iaT1yp4UcJQP_Z1sglSX9A.png
[image2]: /images/1*ZabZyDPW5RY7M1ssxAg1Cw.pn