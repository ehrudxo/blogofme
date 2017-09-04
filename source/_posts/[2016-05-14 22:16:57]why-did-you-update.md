---
title: "why-did-you-update"
date: 2016-05-14 22:16:57
tags: github, github-trend, tech-trend 
---


![][image0]blog.atom.io

reflow는 같은 리소스를 또 호출하는 것을 이야기하고, repaint는 다시 redering하는 것을 이야기 합니다. 아무리 페이지를 가볍게 만들어도 reflow와 repaint를 자주 반복한다면 페이지 성능에 문제가 있겠죠?

이런 관점에서 React 의 값들에 대해서 update가 일어나는 것을 파악해서 알려주는 프로젝트가 있습니다. update 가 일어났는데도 값은 바뀌지 않으면 왜 바뀌지 않았나요? reflow,repaint 아닌가요? 라고 묻습니다.

2016/05/14 Editor's choice

[**garbles/why-did-you-update**  
_why-did-you-update - :boom: Puts your console on blast when React is making unnecessary updates._github.com][anchor0][][anchor1]

---

#### 설치하기
    
    $npm install why-did-you-update --save

네, 언제나 그렇듯이.

#### 실행해 봅시다.

그냥 React는 당연히 잘 실행을 할 듯 싶어서 작업중이던 React-Native 프로젝트에 한번 넣어 보았습니다.

그러고 나서 실행을 시켜 보았습니다.

![][image1]

Facebook 로그인 모듈에서 미친듯한 data의 update 가 일어나는군요.

( 아무래도 이 부분은 모듈의 문제라기 보다는 react-native 에서 state가 변하는 방식이 react와는 다르게 일어나는 듯 싶네요)

어쨌든 데이타 변화를 감지해서 같은 값의 경우 값을 로깅을 해 주네요.

By [Keen Dev][anchor2] on [May 14, 2016][anchor3].

Exported from [Medium][anchor4] on May 31, 2017\.


[anchor0]: https://github.com/garbles/why-did-you-update "https://github.com/garbles/why-did-you-update"
[anchor1]: https://github.com/garbles/why-did-you-update
[anchor2]: https://medium.com/@keendev
[anchor3]: https://medium.com/p/6e04509a94ce
[anchor4]: https://medium.com


[image0]: /images/1*3UZG5P7HY8lupP_BUWPfEg.png
[image1]: /images/1*XDkvreehzAJMQPuQiSONDA.pn