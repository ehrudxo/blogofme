---
title: "security-guide-for-developers"
date: 2016-08-10 23:01:55
tags: github, github-trend, tech-trend 
---


프론트엔드 개발자를 위한 보안 가이드가 오늘 소개해 드릴 프로젝트입니다. 몇번씩이나 깃헙 수위권을 차지 했었는데요. 상당히 읽어 볼만한 내용들을 포함하고 있습니다.

2016/08/10 best Practice

[**FallibleInc/security-guide-for-developers**  
_security-guide-for-developers - Security Guide for Developers (实用性开发人员安全须知)_github.com][anchor0][][anchor1]

---

#### 배경설명

[**Fallible - Secure your startup**  
_About us We are a group of hackers passionate about improving the security posture of companies, tech startups in..._fallible.co][anchor2][][anchor3]

해커 그룹이 만든 fallible 라는 회사는

![][image0]

의 가격에 취약점에서 서비스를 지켜준다고 하는군요.

아무튼 이 회사에서 깃헙에 security가이드를 내 주고 공개해서 많은 사람들의 호응을 얻고 있는데, 문서가 다 완성되어 있지 않는데에도 스타가 1만개가 넘는군요

---

#### 체크리스트

[**FallibleInc/security-guide-for-developers**  
_security-guide-for-developers - Security Guide for Developers (实用性开发人员安全须知)_github.com][anchor4][][anchor5]

체크리스트 하나를 만들어 나가고 있는데 꽤나 볼만 합니다. 한번 이 문서를 번역해서 PU 날려주는 것도 많을 거 같습니다.

**일단 인증을 살펴볼까요?**

* HTTPS 를 꼭 쓸것
* 비밀번호 해쉬를 저장할 때는 Bcrypt를 사용할것. (salt는 Bcrypt가 알아서 해 주니 필요없음
* 로그아웃 후에는 session ID 값을 지울 것
* 패스워드 변경때는 살아있는 모든 session 을 지울 것
* OAuth2 는 state 매개변수를 무조건 가질 것
* 성공적으로 로그인하고 나서는 열려 있는 리다이렉트는 없앨 것
* 회원등록/로그인 입력값을 해석할 때 javascript와 data, CRLF 값등을 깨끗하게 유지할 것
* 쿠키는 암호화한 http 내용만 허용
* 모바일 에서 사용되는 OTP 검증 시, OTP를 생성하거나 리셋한 결과 값을 리턴하는 response에 패스워드를 보내지 말것
* 로그인 혹은 OTP검증 혹은 관련된 API사용의 횟수를 제한할 것. captcha 기반의 챌린지를 가질 것
* 이메일 링크와 SMS 로 보내진 리셋 패스워드의 난수값을 확인할 것
* 리셋 패스워드의 만기일을 설정할 것(납득할만한 기간)
* 토큰 값이 성공적으로 사용되고 나서는 삭제할 것

이것 이외도 많은 내용이 있으니 살펴볼만 한 듯합니다.

By [Keen Dev][anchor6] on [August 10, 2016][anchor7].

Exported from [Medium][anchor8] on May 31, 2017\.


[anchor0]: https://github.com/FallibleInc/security-guide-for-developers "https://github.com/FallibleInc/security-guide-for-developers"
[anchor1]: https://github.com/FallibleInc/security-guide-for-developers
[anchor2]: https://fallible.co/ "https://fallible.co/"
[anchor3]: https://fallible.co/
[anchor4]: https://github.com/FallibleInc/security-guide-for-developers/blob/master/security-checklist.md "https://github.com/FallibleInc/security-guide-for-developers/blob/master/security-checklist.md"
[anchor5]: https://github.com/FallibleInc/security-guide-for-developers/blob/master/security-checklist.md
[anchor6]: https://medium.com/@keendev
[anchor7]: https://medium.com/p/5bdef1d0feb4
[anchor8]: https://medium.com


[image0]: /images/1*xYBVRvNvwE3LKISwLYSLFQ.pn