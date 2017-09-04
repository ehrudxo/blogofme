---
title: "React-Native-Desktop"
date: 2016-03-31 09:31:46
tags: github, github-trend, tech-trend 
---


![][image0]

이번엔 또 뭐야.라고 하실지 모르겠습니다. React는 뭐고 React Native는 뭐고 이번엔 또 React Native Desktop 이라니...

2016/03/31 Best project (2640 ★)

[**ptmt/react-native-desktop**  
_react-native-desktop - React Native for OS X_github.com][anchor0][][anchor1]

하루에 2640 스타라니... 덜덜.

그래서 한번 정리해 보겠습니다.

![][image1]

이번에 나온 React-Native-Desktop은 OSX의 Native컴포넌트들을 만듭니다.

네이밍은 이렇게 정리가 되는 거 같습니다. Native 가 붙는 것은 iOS나 Android, OSX등의 바이너리로 컴파일이 되는 것으로. Desktop은 OSX, Windows 환경으로..

React-Desktop은 React Web 컴포넌트를 각 Native 처럼 스타일을 바꿔서 Desktop 애플리케이션을 쓰는 것처럼 만들어 줬다면 ( Electron이 가능케함) React-Native-Desktop은 Facebook의 React-Native가 Android 와 iOS의 Native 컴포넌트를 다루는 방식을 따라 갔네요.

### 설치
    
    npm install react-native-desktop-cli -g  
    react-native-desktop init MyProject  
    cd MyProject  
    open osx/MyProject.xcodeproj

설치 방법 조차도 React-Native와 흡사 동일합니다.

실행

처음 실행시켜 보면 만들어 내는 프로젝트 형태도 같습니다.

![][image2]

Welcome to React Native Desktop!을 편집해서 프로젝트를 돌려 보도록 하겠습니다.

React packager가 일단 똑같이 뜹니다.(React-native 처럼)

![][image3]

Build Successful이 뜬 다음에 Localhost port를 할당하는 메세지가 완전 재미있게 올라옵니다.

![][image4]맨 아래 보이시나요?

정말 이렇게 뜰 줄은 몰랐는데, 재치가 번뜩이네요.

그 이후에

![][image5]

와 같은 메세지가 뜹니다.

### **인사이트**

이제 React 문법만 알면 Native 애플리케이션을 정말 손쉽게 만들 수 있겠다는 생각이 듭니다. Android 와 iOS와 같은 컴포넌트 이름을 공유하는 React-Native 의 장점을 생각하면 데스크탑 애플리케이션 개발도 이제는 개발 속도가 정말 빨라지겠네요.

남은건 이제 windows Native 인가요? 흠. 요즘 MS 행보를 봐서는 MS에서 만들어 줄지도..

![][image6]과연?

By [Keen Dev][anchor2] on [March 31, 2016][anchor3].

Exported from [Medium][anchor4] on May 31, 2017\.


[anchor0]: https://github.com/ptmt/react-native-desktop "https://github.com/ptmt/react-native-desktop"
[anchor1]: https://github.com/ptmt/react-native-desktop
[anchor2]: https://medium.com/@keendev
[anchor3]: https://medium.com/p/c90acdcdb529
[anchor4]: https://medium.com


[image0]: /images/1*Re3jc57_Njm2t1c1eDgVzA.png
[image1]: /images/1*n_SHE9JAr0Ja3K-LjI0xEA.png
[image2]: /images/1*uq-5LCHQaCdmuG6sSC6YdA.png
[image3]: /images/1*DbBePfyMV0cuTEi7SIDTiQ.png
[image4]: /images/1*E2ylGSDP8qZS3l16ovcPZQ.png
[image5]: /images/1*wYyhkz9mwnCaziNf59AOJQ.png
[image6]: /images/1*hn_9XnUznCXDjvtBmvyENg.pn