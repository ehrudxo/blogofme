---
title: "react-infinite-calendar"
date: 2016-06-04 00:54:26
tags: github, github-trend, tech-trend 
---


![][image0]calendar

언제나 이쁜 calendar 앱은 개발자들에게 인기가 좋습니다. 게다가 코드짜기가 더 쉽다고 하면 더할 나위 없을 거 같습니다.

React 컴포넌트로 만든 무한하게 스크롤 되는 Calendar 앱입니다.

2016/06/03 Editor's choice

[**clauderic/react-infinite-calendar**  
_react-infinite-calendar - ✨ Infinite scrolling date-picker built with React, with localization, themes, keyboard..._github.com][anchor0][][anchor1]

이런 디자인마저 잘하는 개발자 정말 부럽습니다.

---

#### 설치하기
    
    $ npm install react-infinite-calendar --save

React는 일반적으로는 npm install을 할 일이 많죠?
    
    <link rel="stylesheet" href="react-infinite-calendar/styles.css"\>  
    <script src="react-infinite-calendar/dist/umd/react-infinite-calendar.js"\></script\>

umd 스타일의 링크도 가능합니다.

#### 사용해 보기
    
    import InfiniteCalendar from 'react-infinite-calendar';  
    import 'react-infinite-calendar/styles.css';  
    .... 중략  
    var today = new Date();  
    var minDate = Number(new Date()) - (24\*60\*60\*1000) \* 7;  
      
    render(  
    <InfiniteCalendar  
    width={400}  
    height={600}  
    selectedDate={today}  
    disabledDays={\[0,6\]}  
    minDate={minDate}  
    keyboardSupport={true}  
    /\>,  
    document.getElementById('root')  
    );

와 같이 하면

![][image1]이쁘죵?

와 같은 이쁜 화면이 나타납니다.소스는 위와 같습니다.

jsFiddle 쪽은 약간 지금 설정 문제가 있는 듯 합니다.

By [Keen Dev][anchor2] on [June 3, 2016][anchor3].

Exported from [Medium][anchor4] on May 31, 2017\.


[anchor0]: https://github.com/clauderic/react-infinite-calendar "https://github.com/clauderic/react-infinite-calendar"
[anchor1]: https://github.com/clauderic/react-infinite-calendar
[anchor2]: https://medium.com/@keendev
[anchor3]: https://medium.com/p/c52aa37f005c
[anchor4]: https://medium.com


[image0]: /images/1*R9O5awF-PH8OBHcM6ZDYmg.jpeg
[image1]: /images/1*i1eK6Q-DT4h9AAIanSRwkw.pn