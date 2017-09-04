---
title: "Scrollable-GraphView"
date: 2016-06-07 10:55:11
tags: github, github-trend, tech-trend 
---


![][image0][https://github.com/philackm/Scrollable-GraphView][anchor0]

Graph 및 통계용 프레임워크들은 꾸준하게 깃헙에 올라옵니다. 주로 웹쪽에서는 상업용 차트를 대신할 용도로 많이 찾지만 오늘 소개해 드릴 Scrollable-GraphView는 Swift 용 라이브러리 입니다.

2016/06/07 Editor's choice

[**philackm/Scrollable-GraphView**  
_Scrollable-GraphView - An adaptive scrollable graph view for iOS to visualise simple discrete datasets. Written in..._github.com][anchor1][][anchor0]

---

#### 설치하기
    
    $git clone [https://github.com/kylef/swiftenv.git][anchor2]

#### 실행하기

graphview\_example 폴더에 들어가면 Xcode프로젝트가 있습니다.

![][image1]

실행 시켜보면

![][image2]스크롤!

그림과 같은 스크롤이 가능한 graph가 나타납니다.

#### 소스 보기

소스는 의외로 간단합니다.

[**philackm/Scrollable-GraphView**  
_Scrollable-GraphView - An adaptive scrollable graph view for iOS to visualise simple discrete datasets. Written in..._github.com][anchor3][][anchor4]

하나의 클래스 안에 모든게 다 담겨져 있네요

public으로 공개된(우리가 사용할 수 있는) 메쏘드는

![][image3]

잔뜩 많네요.

무려 1200줄...ㄷ ㄷ

private 메쏘드인 BarDrawingLayer를 살펴보면 CGRect, CGFloat등 Core Graphics를 잘 활용해서 Bar를 구현했음을 볼 수 있네요.

[**CGGeometry Reference**  
_Describes structures and functions for manipulating points, rectangles, and sizes._developer.apple.com][anchor5][][anchor6]

[**About Drawing and Printing in iOS**  
_This document covers three related subjects: Drawing custom UI views. Custom UI views allow you to draw content that..._developer.apple.com][anchor7][][anchor8]

두 링크를 보면 이해하시는데 도움이 되지 않을까 링크 걸어두었습니다.

By [Keen Dev][anchor9] on [June 7, 2016][anchor10].

Exported from [Medium][anchor11] on May 31, 2017\.


[anchor0]: https://github.com/philackm/Scrollable-GraphView
[anchor1]: https://github.com/philackm/Scrollable-GraphView "https://github.com/philackm/Scrollable-GraphView"
[anchor2]: https://github.com/kylef/swiftenv.git
[anchor3]: https://github.com/philackm/Scrollable-GraphView/blob/master/Classes/ScrollableGraphView.swift "https://github.com/philackm/Scrollable-GraphView/blob/master/Classes/ScrollableGraphView.swift"
[anchor4]: https://github.com/philackm/Scrollable-GraphView/blob/master/Classes/ScrollableGraphView.swift
[anchor5]: https://developer.apple.com/library/ios/documentation/GraphicsImaging/Reference/CGGeometry/#//apple_ref/c/tdef/CGRect "https://developer.apple.com/library/ios/documentation/GraphicsImaging/Reference/CGGeometry/#//apple_ref/c/tdef/CGRect"
[anchor6]: https://developer.apple.com/library/ios/documentation/GraphicsImaging/Reference/CGGeometry/#//apple_ref/c/tdef/CGRect
[anchor7]: https://developer.apple.com/library/ios/documentation/2DDrawing/Conceptual/DrawingPrintingiOS/Introduction/Introduction.html#//apple_ref/doc/uid/TP40010156 "https://developer.apple.com/library/ios/documentation/2DDrawing/Conceptual/DrawingPrintingiOS/Introduction/Introduction.html#//apple_ref/doc/uid/TP40010156"
[anchor8]: https://developer.apple.com/library/ios/documentation/2DDrawing/Conceptual/DrawingPrintingiOS/Introduction/Introduction.html#//apple_ref/doc/uid/TP40010156
[anchor9]: https://medium.com/@keendev
[anchor10]: https://medium.com/p/4d44e284903c
[anchor11]: https://medium.com


[image0]: /images/1*3khbUSUoUedOZqSBGNXcqw.jpeg
[image1]: /images/1*XcmFc-R_8rw9njGEpq1drQ.png
[image2]: /images/1*B0_YRbmjuB0Zht5y_FWMsQ.gif
[image3]: /images/1*4TtZTH4WajqmNG5r9OkL1w.pn