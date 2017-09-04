---
title: "webpack-dashboard"
date: 2016-08-16 06:28:21
tags: github, github-trend, tech-trend 
---


webpack 을 쓰면서 콘솔창이 시끄럽다고 생각했던 것은 저만이 아니었나 봅니다.

![][image0]

위에 보는 형태 처럼 깔끔하게 cli 대시보드로 만들어 줄 수 있는 프로젝트가 등장했네요.

2016/08/16 Editor's choice

[**FormidableLabs/webpack-dashboard**  
_webpack-dashboard - A CLI dashboard for webpack dev server_github.com][anchor0][][anchor1]

---

#### 설치하기

간단하게 npm을 이용하면 됩니다.
    
    $npm install webpack-dashboard --- save-dev

#### 사용하기

webpack을 사용할 때에 보통 config 파일과 실행파일(dev-server 쪽)을 나눠서 진행할 경우가 많은데, config 쪽에 적용해 줘야 할 부분과 실행 파일쪽에 적용해 줘야 하는 부분으로 나눠서 설명하겠습니다.

첫번째 server.js 쪽 소스 예제가 실행에 관련된 부분, 부번째가 config.js 관련된 샘플이라고 보시면 됩니다.

저렇게 실행시키고
    
    $node server

명령어로 실행을 시켜주고 나면

![][image1]

와 같은 그림이 뜹니다.

심심하니 에러를 의도적으로 만들어 보겠습니다.

![][image2]

프로그레스 바가 뜨더니 에러를 로그에 뱉어 주는 군요.

모듈과 Asset에 대한 내용도 자세히 표시 되어 있습니다.

깔끔하게 webpack상태를 모니터링 하기에는 좋은 방법으로 보여집니다.

By [Keen Dev][anchor2] on [August 15, 2016][anchor3].

Exported from [Medium][anchor4] on May 31, 2017\.


[anchor0]: https://github.com/FormidableLabs/webpack-dashboard "https://github.com/FormidableLabs/webpack-dashboard"
[anchor1]: https://github.com/FormidableLabs/webpack-dashboard
[anchor2]: https://medium.com/@keendev
[anchor3]: https://medium.com/p/cb3fa0038c15
[anchor4]: https://medium.com


[image0]: /images/1*8xix5ooHs0F38maUj4XmNQ.png
[image1]: /images/1*O4_HxR8l8W272aQF9NhFIQ.png
[image2]: /images/1*1WlVCuqJt5abKCa3qwxPnw.gi