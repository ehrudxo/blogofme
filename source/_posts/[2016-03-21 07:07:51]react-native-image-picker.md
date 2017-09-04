---
title: "react-native-image-picker"
date: 2016-03-21 07:07:51
tags: github, github-trend, tech-trend 
---


![][image0]

모바일 앱에서 Image-Picker는 필수라고 볼수 있죠. React-native에서 이미지를 어떻게 참조할지 알고 싶다면 이 프로젝트가 좋은 아이디어를 줄 것입니다.

2016/03/21 Editor's choice

[**marcshilling/react-native-image-picker**  
_react-native-image-picker - A React Native module that allows you to use native UI to select media from the device..._github.com][anchor0][][anchor1]

native 이미지 피커를 이용해서 작업을 합니다.

### 설치
    
    $npm install react-native-image-picker@latest --- save  
    $rnpm link

rnpm link를 이용하면 dependency 문제는 대부분 해결을 해 주기 때문에 위 프로젝트 readme의 설정은 건드리지 않아도 됩니다.

하지만, 이 프로젝트는 android의 경우는 권한을 줘야 하는 부분이 있기 때문에 한가지 작업만 더 하겠습니다. AndroidMenifest.xml파일만 다음의 부분을 추가해 주세요.

소스예제

와 같이 적용했더니 아래와 같이 이미지를 고를 수 있게 나옵니다.

![][image1]

By [Keen Dev][anchor2] on [March 20, 2016][anchor3].

Exported from [Medium][anchor4] on May 31, 2017\.


[anchor0]: https://github.com/marcshilling/react-native-image-picker "https://github.com/marcshilling/react-native-image-picker"
[anchor1]: https://github.com/marcshilling/react-native-image-picker
[anchor2]: https://medium.com/@keendev
[anchor3]: https://medium.com/p/4455a9ff79bd
[anchor4]: https://medium.com


[image0]: /images/1*ss-g_QiUDZHnPdUckYvyaw.png
[image1]: /images/1*UJbe_2RSmGQlg2ODMJ2Kgw.pn