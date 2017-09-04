---
title: "You-Dont-Need-Javascript"
date: 2016-07-07 12:04:00
tags: github, github-trend, tech-trend 
---


![][image0]

개인적으로 좋아하는 형태의 프레임워크 중 하나입니다.

번역하면 제목도 " javascript 필요 없어요" 정도가 적당할 거 같은데 보통은 jaavascript로 구현을 하는 작업 몇가지들을 CSS만으로 구현했습니다.

2016/07/07 Today's best

[**NamPNQ/You-Dont-Need-Javascript**  
_You-Dont-Need-Javascript - Css is powerful, you can do a lot of things without js._github.com][anchor0][][anchor1]

### Accordion / Toggle

아코디언/토글 UI 의 JSfiddle은 다음과 같습니다. Javascript는 없다고 당황하지 마시고 다른 탭을 눌러주세요.

아코디언의 기본적인 구현 방식은 일단 input type 을 Radio 로 두고 체크가 되었을 때 display를 바꿔주는 방식으로 구현이 되어 있습니다.
    
    .accordion \[type=radio\], .accordion \[type=checkbox\] {  
    display:none;  
    }

    .horizontal \[type=radio\]:checked ~ label ~ .content {   
    visibility:visible;  
    width:442px;  
    padding:0 10px;  
    border:1px solid \#542437;  
    border-left:0;   
    }

### Carousel

회전 목마 UI 입니다.

이벤트를 걸게 되는 부분은 위의 예제와 같이 input 엘리먼트에 :checked~ 를 걸게 되어 있군요.
    
    .carousel-open:checked + .carousel-item {  
    position: static;  
    opacity: 100;  
    }

    \#carousel-1:checked ~ .control-1,  
    \#carousel-2:checked ~ .control-2,  
    \#carousel-3:checked ~ .control-3 {  
    display: block;  
    }

---

또 여러가지 재미있는 예제들이 있습니다만 가장 제 눈을 끈 것은 뭐니뭐니해도 Modal 이었습니다.

### Modal/Popup

모달 컨테이너 클래스의 CSS입니다
    
    .modal-container {  
    background: rgba(black, .75);  
    opacity: 0;  
    color: white;  
    width: 100%;  
    height: 100%;  
    position: fixed;  
    top: 0;  
    left: 0;  
    visibility: hidden;  
    transition: opacity .5s, visibility 0s linear .6s;  
    z-index: 2;  
    .modal-toggler:checked + & {  
    opacity: 1;  
    visibility: visible;  
    transition: opacity .5s;  
    }  
    }

By [Keen Dev][anchor2] on [July 7, 2016][anchor3].

Exported from [Medium][anchor4] on May 31, 2017\.


[anchor0]: https://github.com/NamPNQ/You-Dont-Need-Javascript "https://github.com/NamPNQ/You-Dont-Need-Javascript"
[anchor1]: https://github.com/NamPNQ/You-Dont-Need-Javascript
[anchor2]: https://medium.com/@keendev
[anchor3]: https://medium.com/p/1679585da29
[anchor4]: https://medium.com


[image0]: /images/1*9LIWyzV7CGvquHKTMEtfcQ.jpe