---
title: "[React-Native] image 늘리기"
date: 2016-03-16 06:39:29
tags: github, github-trend, tech-trend 
---


![][image0]hard to stretch

React Native 는 여러가지 새로운 개념들 (예를 들어 flex)를 많이 적용하는데, 이미지 width : 100% 같은 형태를 주려고 하면 생각보다 잘 되지 않는다.

![][image1]

이렇게 나오거나 지나치게 꽉 채워서 나오지만, 실제 어플리케이션을 짜려고 하면, width는 화면 사이즈에 맞춰 늘리고 height는 동일한 크기로 셋팅하고 싶을 때가 많다. 이럴 경우는 어쩌면 좋을까?

### Dimension과 resizeMode를 적절히 활용

다음은 소스다.
    
    var {height, width} = Dimensions.get('window');

이 부분에 주의 하자. Dimension은 기본적으로 React에 포함되어 있는 모듈이므로 사용하는데 무리가 없음.

이후 style 에 width는 지정한 width로 height는 개발자가 원하는 데로 줄 수 있다.

그리고 React Image Component 에는 resizeMode가 존재한다.

![][image2]

stretch모드로 두면 높이와 넓이를 따로 지정할 수 있는데, 기본적으로 Dimension 만 알아둬도 웹앱을 제작하는데에는 어려움이 없을 것으로 보인다.

이렇게 작업을 하고 나면

![][image3]

원하는 레이아웃이 나온다.

By [Keen Dev][anchor0] on [March 15, 2016][anchor1].

Exported from [Medium][anchor2] on May 31, 2017\.


[anchor0]: https://medium.com/@keendev
[anchor1]: https://medium.com/p/b562da8ed665
[anchor2]: https://medium.com


[image0]: /images/1*8g_8leaDJr9jC0kCHYjISg.png
[image1]: /images/1*rDdJNacr54VdZSaY2f8ffQ.png
[image2]: /images/1*2tID_iqXkL8E8uGozf86Kg.png
[image3]: /images/1*zYLaqNyy8YCKR7S8e4614w.pn