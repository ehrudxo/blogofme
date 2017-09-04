---
title: "15DaysofSwiftAnimation"
date: 2016-05-07 22:32:34
tags: github, github-trend, tech-trend 
---


![][image0]되게 많아 보입니다.네 아직 11일째

15일째 리뷰를 할 걸 그랬나요. 따끈 따끈한 프로젝트가 왔습니다. 애니메이션 때문에 mpeg to gif 앱도 몇가지를 깔게 되는군요. 아 이게 새로운 맥을 사서 가능해진 호사네요.

15days swift, 30days android 등등 시리즈들이 지속적으로 깃헙에는 올라옵니다. 오늘 소개해 드릴 프로젝트는 그 중에서 Swift의 애니메이션을 코드로 어떻게 짜는지에 대한 프로젝트 입니다.

2016/05/07 Editor's choice

[**larrynatalicio/15DaysofAnimationsinSwift**  
_15DaysofAnimationsinSwift - A project to learn animations._github.com][anchor0][][anchor1]

흠.. 개발자의 완성은? 얼....

---

#### 설치해 봅시다

설치할게 뭐 있을까 싶네요
    
    $git clone [https://github.com/larrynatalicio/15DaysofAnimationsinSwift.git][anchor2]

프로젝트를 받고 나면

![][image1]4일 남았군요.

다음과 같은 프로젝트들이 있습니다.

---

#### 실행해 봅시다

1번과 6번을 실행해 볼 예정입니다.
> 
> NavigationBarAnimation

아래와 같이 스크롤해서 내려가면 NavigationBar가 사라졌다가 다시 스크롤을 올리면 NavigationBar 가 복귀되는 간단한 프로젝트입니다.

![][image2]

XCODE를 열어서 확인해 보겠습니다. 아마도 많은 사람들이 그냥 간단하게 할 수 있을거라고 생각하시는 부분일텐데요.

![][image3]xcode

AppDelegate는 주로 앱 전체 옵션들을 정할 수 있고, ViewController를 확인해 보면 스크롤 액션에 대한 소스들을 확인할 수 있습니다.

UITableViewController 를 상속한 ViewController의 소스는 다음과 같습니다.

마지막 configureNavigationController 함수의

hideBarOnSwipe 만 false 로 바꾸면 동작하지 않는 간단한 예제 입니다.
> 
> StretchyHeaderAnimation

이 예제는 스크롤을 당기면 화면의 이미지가 줌되는 애니메이션을 보여줍니다. 일단 스크린샷을 보시면 감이 오실 거 같습니다.

![][image4]으어억 성이 커진다

성을 광화문으로 바꿔볼까요?

![][image5]광화문이다~

Supporting Files의 Asset에 kcastle.jpg 만 집어 넣고 Main.storyboard 의 이미지만 kcastle로 선택해 주면 화면은 바뀝니다.

![][image6]이렇게 말이죠.

이런 일을 하는 소스를 한번 살펴 봐야겠죠? 첫번째 예제의 경우와 똑같이 ViewController 소스를 살펴봐야합니다.

이 updateHeaderView 의 y값과 Height를 변경해 주는 것으로 애니메이션이 실행됩니다.

이 함수를 viewDidLoad와 scrollViewDidScroll 에서 호출을 해 줘서 화면이 뜨고 스크롤이 될때 값이 변하는 형태로 애니메이션을 구현했네요.

scrollViewDidScroll 은 UIScrollViewDelegate에서 가져왔네요.

Swift를 하면서 수려한 애니메이션을 구현하시고 싶었던 분들에게는 무척이나 좋은 프로젝트가 될 것 같습니다.

By [Keen Dev][anchor3] on [May 7, 2016][anchor4].

Exported from [Medium][anchor5] on May 31, 2017\.


[anchor0]: https://github.com/larrynatalicio/15DaysofAnimationsinSwift "https://github.com/larrynatalicio/15DaysofAnimationsinSwift"
[anchor1]: https://github.com/larrynatalicio/15DaysofAnimationsinSwift
[anchor2]: https://github.com/larrynatalicio/15DaysofAnimationsinSwift.git
[anchor3]: https://medium.com/@keendev
[anchor4]: https://medium.com/p/93eb0720914c
[anchor5]: https://medium.com


[image0]: /images/1*guK9C6XJVIzItV0duMMpMQ.png
[image1]: /images/1*EXdHILi3TJlajOTflinH7g.png
[image2]: /images/1*z4fftua-ygEtt9d6ZmayNw.gif
[image3]: /images/1*mqQ0dx8JS1vZuksCE96W0w.png
[image4]: /images/1*LIMr_YWmCwEdbeDbanDkzg.gif
[image5]: /images/1*tPt9iFbbIh29dvNz5zuqWA.png
[image6]: /images/1*WjP5n6a-e9saCZhO6vIKvw.gi