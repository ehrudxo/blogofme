---
title: "AnimatedSVGView"
date: 2016-06-16 08:34:59
tags: github, github-trend, tech-trend 
---


SVG라는 포맷은 여러모로 많이 쓰이는 벡터포맷입니다. Canvas가 나오기 전까지는 DOM위에 그릴 수 있는 Vecotr 포맷으로 가장 유용한 역할을 하고 있었고, HTML5 Canvas가 나온 이후에도 브라우저 지원등의 이유로 여전히 사랑을 받고 있습니다.

이미지를 SVG로 바꿔주는 여러가지 시도들도 있었죠.

2016/06/16 Editor's choice

오늘은 Android에서 SVG를 보여주는 프로젝트입니다.

[**jaredrummler/AnimatedSvgView**  
_AnimatedSvgView - Animated SVG Drawing for Android_github.com][anchor0][][anchor1]

---

그런데, 그냥 보여 주는 것은 아닙니다.

SVG는 기본적으로 drawing하는 점,선, 면들의 xml집합체로 되어 있는데, 그 집합체들을 약간의 시간을 두고 이쁘게 그릴 수 있도록 해 주고 있습니다.

![][image0]

보시면 아시겠지만, 그려지는 순서대로 파티클이 뿌려지는 효과 처럼 그려지면서 완성이 됩니다.

[**jaredrummler/AnimatedSvgView**  
_AnimatedSvgView - Animated SVG Drawing for Android_github.com][anchor2][][anchor3]

데모로 그려주는 소스는 위의 링크에서 찾아 볼수 있구요.

아래와 같은 형태를 하고 있습니다.
    
    _DEVPOOLS_(  
    new String\[\]{  
    "M110,830,l0,-710,710,0,710,0,0,710,0,710,-710,0,-710,0,0,-710z m1360,0,l0,-650,-650,0,-650,0,0,650,0,650,650,0,650,0,0,-650z",  
    "M314,832,c-30,-20,-19,-82,15,-82,29,0,46,36,32,66,-11,24,-27,30,-47,16z",  
    "M1320,826,c-15,-19,-9,-56,12,-69,34,-22,66,41,36,71,-16,16,-33,15,-48,-2z",  
    "M657,692,c-9,-13,20,-83,45,-109,12,-14,35,-31,50,-39,35,-18,119,-18,162,0,42,18,85,73,93,120,5,33,4,36,-20,36,-20,0,-28,-7,-37,-34,-23,-72,-102,-105,-172,-72,-34,17,-68,61,-68,90,0,16,-44,23,-53,8z"  
    },new int\[\]{  
    Color._BLACK_,  
    Color._RED_,  
    Color._RED_,  
    Color._RED  
    _},  
    1630,1650  
    ),

쉽게 말씀드리면

첫번째 면수로는 Path의 배열 두번째는 그 Path의 색, 넓이, 높이 순으로 입력하면 같은 모양으로 그리게 됩니다.

DEVPOOLS 로고를 입력해 보았습니다.

![][image1]

훌륭하게 그려지는 군요

By [Keen Dev][anchor4] on [June 15, 2016][anchor5].

Exported from [Medium][anchor6] on May 31, 2017\.


[anchor0]: https://github.com/jaredrummler/AnimatedSvgView "https://github.com/jaredrummler/AnimatedSvgView"
[anchor1]: https://github.com/jaredrummler/AnimatedSvgView
[anchor2]: https://github.com/jaredrummler/AnimatedSvgView/blob/master/demo/src/main/java/com/jrummyapps/android/animatedsvgview/demo/SVG.java "https://github.com/jaredrummler/AnimatedSvgView/blob/master/demo/src/main/java/com/jrummyapps/android/animatedsvgview/demo/SVG.java"
[anchor3]: https://github.com/jaredrummler/AnimatedSvgView/blob/master/demo/src/main/java/com/jrummyapps/android/animatedsvgview/demo/SVG.java
[anchor4]: https://medium.com/@keendev
[anchor5]: https://medium.com/p/c261a4dd9771
[anchor6]: https://medium.com


[image0]: /images/1*OeABEdHx0BYxfkgvX0PENg.gif
[image1]: /images/1*wD_VfSBTFnvcy1kWpDsEzA.gi