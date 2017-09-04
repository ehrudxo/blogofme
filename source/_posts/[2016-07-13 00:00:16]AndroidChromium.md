---
title: "AndroidChromium"
date: 2016-07-13 00:00:16
tags: github, github-trend, tech-trend 
---


![][image0]
> 
> 크로뮴이란 [구글][anchor0]에서 개발하는 [오픈 소스][anchor1] 크롬 프로젝트이다. 엄밀히 말하자면 [구글 크롬][anchor2] 자체는 오픈 소스가 아니고 [크로뮴(Chromium)][anchor3]이라는 오픈 소스 버전이 따로 있는데, 상표등록이 되어있는 '구글'이라는 이름과 오픈 소스로 공개할 수 없는 자잘한 것들 때문에 나눠놓은 것이다.

> 왜냐하면 크롬에 내장된 플래시 플레이어와 [PDF][anchor4]뷰어, [H.264][anchor5] [동영상][anchor6] 재생 코덱, 구글 서비스 지원, 동기화 등의 자잘한 기능엔 브라우징 정보 수집 기능도 들어있기 때문이다.

[**크로뮴 프로젝트**  
_크로미움 또는 크로미엄이라고도 한다.ChromiumChromium Projects 구글에서 개발하는 오픈 소스 크롬 프로젝트이다. 엄밀히 말하자면 구글 크롬 자체는 오픈 소스가 아니고 크로뮴(Chromium)이라..._namu.wiki][anchor7][][anchor8]

네, 크로미움 혹은 크로뮴을 Android에서 돌릴 수 있도록 한 프롲게트 입니다.

2016/07/12 Editor's Choice

[**JackyAndroid/AndroidChromium**  
_AndroidChromium - chrome browser android version of the source program,build with gradle_github.com][anchor9][][anchor10]

---

#### 이게 왜 필요할까요?

프로젝트의 주인장은 이 프로젝트를 만든게 크롬 디버깅을 위해서라고 합니다. 브라우저를 만드는 일을 하나 봅니다.

#### 우리에게는 어떤 의미가 있을까요?

[**Android Build Instructions**  
_A Linux build machine capable of building Chrome for Linux. Other (Mac/Windows) platforms are not supported for Android..._chromium.googlesource.com][anchor11][][anchor12]

크로미움 사이트에 가시면 빌드 Instruction 들이 잔뜩 나와 있는데

이 부분을 Gradle 로 빌드가 가능하게 만들어 놓은 것입니다.

native runtime을 건드리는 관계로 에뮬레이터에는

[**INSTALL\_FAILED\_NO\_MATCHING\_ABIS when install apk**  
_I tried to install my app into Android L Preview Intel Atom Virtual Device, it failed with error..._stackoverflow.com][anchor13][][anchor14]

를 뱉고는 죽어 버립니다.

삼성 GalaxyS7 에서는 기존에 깔린 앱과 충돌이 나서 진행을 할 수가 없군요.

실행을 못해서 좀 아쉽기는 하지만 굉장히 좋은 도전인거 같습니다.

By [Keen Dev][anchor15] on [July 12, 2016][anchor16].

Exported from [Medium][anchor17] on May 31, 2017\.


[anchor0]: https://namu.wiki/w/%EA%B5%AC%EA%B8%80 "구글"
[anchor1]: https://namu.wiki/w/%EC%98%A4%ED%94%88%20%EC%86%8C%EC%8A%A4 "오픈 소스"
[anchor2]: https://namu.wiki/w/%EA%B5%AC%EA%B8%80%20%ED%81%AC%EB%A1%AC "구글 크롬"
[anchor3]: http://www.chromium.org/ "http://www.chromium.org/"
[anchor4]: https://namu.wiki/w/PDF "PDF"
[anchor5]: https://namu.wiki/w/H.264 "H.264"
[anchor6]: https://namu.wiki/w/%EB%8F%99%EC%98%81%EC%83%81 "동영상"
[anchor7]: https://namu.wiki/w/%ED%81%AC%EB%A1%9C%EB%AE%B4%20%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8 "https://namu.wiki/w/%ED%81%AC%EB%A1%9C%EB%AE%B4%20%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8"
[anchor8]: https://namu.wiki/w/%ED%81%AC%EB%A1%9C%EB%AE%B4%20%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8
[anchor9]: https://github.com/JackyAndroid/AndroidChromium "https://github.com/JackyAndroid/AndroidChromium"
[anchor10]: https://github.com/JackyAndroid/AndroidChromium
[anchor11]: https://chromium.googlesource.com/chromium/src/+/master/docs/android_build_instructions.md "https://chromium.googlesource.com/chromium/src/+/master/docs/android_build_instructions.md"
[anchor12]: https://chromium.googlesource.com/chromium/src/+/master/docs/android_build_instructions.md
[anchor13]: http://stackoverflow.com/questions/24572052/install-failed-no-matching-abis-when-install-apk "http://stackoverflow.com/questions/24572052/install-failed-no-matching-abis-when-install-apk"
[anchor14]: http://stackoverflow.com/questions/24572052/install-failed-no-matching-abis-when-install-apk
[anchor15]: https://medium.com/@keendev
[anchor16]: https://medium.com/p/cafbf8df64d
[anchor17]: https://medium.com


[image0]: /images/1*W3UzAhoqV6i4U1UGi1ggXA.pn