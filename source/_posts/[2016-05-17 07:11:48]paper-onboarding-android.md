---
title: "paper-onboarding-android"
date: 2016-05-17 07:11:48
tags: github, github-trend, tech-trend 
---


![][image0]

OnBoarding은 앱이 시작될때 사용자로 하여금 액션을 유도하게 해서 더 흥미를 느끼게 하는 일종의 게이미피케이션 입니다. Raymotion이라는 그룹은 아름다운 모바일 UI 컴포넌트를 많이 만들어 내는데, 이번엔 온보딩용 프로젝트를 내 놓았습니다.

2016/05/17 Editor's choice

[**Ramotion/paper-onboarding-android**  
_paper-onboarding-android - PaperOnboarding is a material design slider_github.com][anchor0][][anchor1]

---

#### 설치하기

설치는 gradle 기준으로 설명하겠습니다.

아래의 dependency를 build.gradle에 추가해 주면 됩니다.
    
    dependencies {

    ....  
    compile 'com.ramotion.paperonboarding:paper-onboarding:1.0.0'

    ....  
    }

샘플을 돌리려면 image 들을 카피해 주면 됩니다.

![][image1]리소스 파일을 복사-붙여넣기!

#### 실행하기

이번엔 소스를 한번 살펴 볼까요?

onCreate 메쏘드에 setOnChangeListenser를 셋팅해 주면 됩니다.

저렇게 Swipe 액션에 대해서 정의를 해 주면 인터페이스는 정의가 되었고

각각의 카드는 ArrayList로 추가만 해주면 됩니다.

이러게 하고 실행을 하면 이런 형태로 땋! 하고 실행됩니다.

![][image2]새로운 에뮬은 좋은데 메모리는 많이 먹네요

온보딩을 이쁘게 꾸미고 싶으신 분들에게는 굉장히 유용한 프로젝트임에 틀림없습니다.

By [Keen Dev][anchor2] on [May 16, 2016][anchor3].

Exported from [Medium][anchor4] on May 31, 2017\.


[anchor0]: https://github.com/Ramotion/paper-onboarding-android "https://github.com/Ramotion/paper-onboarding-android"
[anchor1]: https://github.com/Ramotion/paper-onboarding-android
[anchor2]: https://medium.com/@keendev
[anchor3]: https://medium.com/p/963c3f477a73
[anchor4]: https://medium.com


[image0]: /images/1*nYk1tHLDQDMTWBdOpQu6ig.gif
[image1]: /images/1*ZAF446pnL4Fa9Pir_3p-vw.png
[image2]: /images/1*ksw5wG9BkvLRm8653vqZCQ.gi