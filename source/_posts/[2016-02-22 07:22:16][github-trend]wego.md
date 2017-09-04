---
title: "[github-trend]wego"
date: 2016-02-22 07:22:16
tags: github, github-trend, tech-trend 
---


오늘은 간단한 프레임워크로 먼저 시작할까 합니다. Go언어로 되어 있구요. worldweatheronline.com API를 사용해서 터미널에 날씨 정보를 보여주는 프로젝트 wego 입니다.

2016/02/22 editor's choice( 90★)

설치
> 
> $go get -u github.com/schachmat/wego

이렇게 해 주면 일단 wego 가 실행이 됩니다. 하지만 실행시 에러를 뱉을 것입니다. 두가지를 해 주셔야 됩니다.

[https://developer.worldweatheronline.com/auth/register][anchor0] 에 가셔서 개발자 등록을 해서 API를 사용할 수 있는 key를 발급 받으시고

~/.wegorc 파일을 만져주시면 됩니다.
> 
> {  
> "APIKey": "API key",  
> "City": "Seoul",  
> "Numdays": 3,  
> "Imperial": false,  
> "Lang": "ko"  
> }

한국어를 사용할 수 있을까 생각하고는 ko를 집어 넣어봤습니다. City는 Seoul.

* 실행
> 
> $wego

![][image0]

훌륭합니다.

By [Keen Dev][anchor1] on [February 21, 2016][anchor2].

Exported from [Medium][anchor3] on May 31, 2017\.


[anchor0]: https://developer.worldweatheronline.com/auth/register
[anchor1]: https://medium.com/@keendev
[anchor2]: https://medium.com/p/a389e7c9f38c
[anchor3]: https://medium.com


[image0]: /images/1*9a-o2XO0RYccLVPpfmkNjw.pn