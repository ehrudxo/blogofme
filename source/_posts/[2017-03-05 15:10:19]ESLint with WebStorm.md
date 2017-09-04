---
title: "ESLint with WebStorm"
date: 2017-03-05 15:10:19
tags: github, github-trend, tech-trend 
---


원본 투고 글 : [http://devpools.kr/2017/02/16/javascript-eslint-webstorm/][anchor0]

IntelliJ 의 웹 버전인 WebStorm을 사용할 때 ESLint를 사용하는 방법을 알아보겠습니다. 프로젝트에도 적용할 수 있겠지만 에디터에서 자동으로 문제가 있는 (혹은 버그를 생산하는) 코드를 미리 찾아 볼 수 있습니다.

### ESLint

"Linting"이라는 행위는 버그가 날 수 있을 만한 코드를 찾아서 체크를 해 주는일을 의미합니다.
> 
> In [computer programming][anchor1], **lint** is a Unix utility that flags some [suspicious and non-portable constructs][anchor2] (likely to be bugs) in [C language][anchor3][source code][anchor4]; generically, lint or a **linter** is any tool that flags suspicious usage in software written in any [computer language][anchor5]. The term **lint-like behavior** is sometimes applied to the process of flagging suspicious language usage. Lint-like tools generally perform [static analysis][anchor6] of source code. --- 위키피디아 [Lint][anchor7]

JavaScript 에서 이 Lint라는 의미를 처음 얘기한 사람은 Douglas crockford 였고 그는 JsLint라는 툴을 만들어 냅니다. JavaScript Definite Guide 같은 책에서도 내용을 언급하고 있습니다.

[**JSLint: The JavaScript Code Quality Tool**  
_JSLint, The JavaScript Code Quality Tool. This file allows JSLint to be run from a web browser. It can accept a source..._www.jslint.com][anchor8][][anchor9]

하지만 최근의 대부분의 JavaScript 커뮤니티에서 사용하는 Lint 툴은 ESLint 툴입니다.

Nicholas Jakas에 의해 2013년에 나온 이 툴은 현재 여러 툴들에서 플러그인으로 사용되고 있습니다.

[**ESLint - Pluggable JavaScript linter**  
_A pluggable and configurable linter tool for identifying and reporting on patterns in JavaScript. Maintain your code..._eslint.org][anchor10][][anchor11]

"JSX" 지원하는 것에 대해서 언급이 첫페이지에 있습니다. React 와 JSX는 다르다고 하는군요. 아무래도 Pluggable한 아키텍처로 이루어져 있기에 오리지날인 JSLint에 비해 많이 쓰이는 거라고 보여집니다.

### webstorm

웹스톰은 IntelliJ를 만든 Jetbrains에서 만든 웹 개발자용 IDE 입니다. 이클립스가 약간은 범용에 가깝다고 하면 이 웹 스톰은 JavaScript 최근 트렌드 및 개발 환경에 대한 이해가 큰 IDE 입니다. Node 모듈에 대한 이해도 가지고 있고 npm 을 기본적으로 작동시킬 수 있습니다. 유료 IDE기는 하지만 IntelliJ에 적응된 개발자들은 이webstorm의 여러가지 기능에 대해서 많이 만족하고 쓰고 있습니다. 최근 팝잇에 올라온 IntelliJ에 관한 글을 읽어보면 많은 인사이트들을 얻을 수 있습니다.

[**인텔리J 활용 꿀팁 42가지 정리 | Popit**  
_인텔리J가 유료 IDE이다 보니 사용하면서 기능들을 최대한 활용하지 않는다면 손해라는 생각이 들었습니다. 그래서 인터넷을 찾아보다 발견한 인텔리J 42가지 팁 소개 동영상를 보고 정리한 글입니다. 해당 동영상은 ..._www.popit.kr][anchor12][][anchor13]

### WebStrom + ESLint

이 WebStorm에서 ESLint를 설정하는 방법은 다음과 같습니다.

preference -\> Languges & Framework -\> ESLint

![][image0]

두가지를 셋팅해 주셔야 하는데 하나는 Node 를 지정하는 것이고 또 다른 하나는 ESLint 폴더를 지정해 주는 것입니다. Node 는 각자의 환경을 정하면 될 것입니다.

ESLint 폴더를 지정할 때는
    
    $ npm list -g|more

옵션을 통해서 어디에 설치를 했는지 확인해 주시면 됩니다.

확인이 되셨으면
    
    `$ npm install -g eslint`

[**eslint/eslint**  
_eslint - A fully pluggable tool for identifying and reporting on patterns in JavaScript._github.com][anchor14][][anchor15]

이후 몇가지 모듈을 더 설치해야 합니다.
    
    $npm install eslint-plugin-react eslint-plugin-jsx-a11y eslint-plugin-import -g

실행해 주고 나서 WebStorm을 다시 작동시키면 아래와 같은 좋은 예를 볼 수 있습니다.

![][image1]

By [Keen Dev][anchor16] on [March 5, 2017][anchor17].

Exported from [Medium][anchor18] on May 31, 2017\.


[anchor0]: http://devpools.kr/2017/02/16/javascript-eslint-webstorm/
[anchor1]: https://en.wikipedia.org/wiki/Computer_programming "Computer programming"
[anchor2]: https://en.wikipedia.org/wiki/C_%28programming_language%29#Language_tools "C (programming language)"
[anchor3]: https://en.wikipedia.org/wiki/C_%28programming_language%29 "C (programming language)"
[anchor4]: https://en.wikipedia.org/wiki/Source_code "Source code"
[anchor5]: https://en.wikipedia.org/wiki/Computer_language "Computer language"
[anchor6]: https://en.wikipedia.org/wiki/Static_code_analysis "Static code analysis"
[anchor7]: https://en.wikipedia.org/wiki/Lint_%28software%29
[anchor8]: http://www.jslint.com/ "http://www.jslint.com/"
[anchor9]: http://www.jslint.com/
[anchor10]: http://eslint.org/ "http://eslint.org/"
[anchor11]: http://eslint.org/
[anchor12]: http://www.popit.kr/%EC%9D%B8%ED%85%94%EB%A6%ACj-%ED%99%9C%EC%9A%A9-%EA%BF%80%ED%8C%81-42%EA%B0%80%EC%A7%80-%EC%A0%95%EB%A6%AC/ "http://www.popit.kr/%EC%9D%B8%ED%85%94%EB%A6%ACj-%ED%99%9C%EC%9A%A9-%EA%BF%80%ED%8C%81-42%EA%B0%80%EC%A7%80-%EC%A0%95%EB%A6%AC/"
[anchor13]: http://www.popit.kr/%EC%9D%B8%ED%85%94%EB%A6%ACj-%ED%99%9C%EC%9A%A9-%EA%BF%80%ED%8C%81-42%EA%B0%80%EC%A7%80-%EC%A0%95%EB%A6%AC/
[anchor14]: https://github.com/eslint/eslint "https://github.com/eslint/eslint"
[anchor15]: https://github.com/eslint/eslint
[anchor16]: https://medium.com/@keendev
[anchor17]: https://medium.com/p/bf9d418993b2
[anchor18]: https://medium.com


[image0]: /images/0*qBlmLC3cTz8oJ-Jf.
[image1]: /images/0*IJ_x1kEFxnkgv5PQ