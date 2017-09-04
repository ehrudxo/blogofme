---
title: "megaboilerplate"
date: 2016-06-09 19:00:21
tags: github, github-trend, tech-trend 
---


![][image0]끝판왕

끝판왕이라는 말은 매우 진부하죠. 이젠?

넘치고 넘치는 웹 개발 boilerplate 뭘 써야 될지 궁금하셨을 텐데요. 이런 고민을 한방에 종결시켜 줄 가능성이 보이는 프로젝트가 나타났습니다.

[**sahat/megaboilerplate**  
_megaboilerplate - Handcrafted starter projects, optimized for simplicity and ease of use._github.com][anchor0][][anchor1]

#### 왜 일케 호들갑이셩

그죠. 좀 호들갑이 심했습니다. 한번 보고 생각해 보자고 일단 움짤을 만들어 봤습니다.

![][image1]

네, 저렇게 내가 쓰고 싶은 레이어별 프레임워크들을 선택하고 나니 megaboilerplate-app이라는 이름의 압축파일이 땋하고 떨어지고, 압축을 풀고 atom으로 열어보니

![][image2]

어머, 친절하게 웹 팩 설정도 왠걸 완벽하게 나오네요.

며칠전에 나온 reactpack을 리뷰할까 하다가 이걸 먼저 리뷰하게 됩니다.

[**olahol/reactpack**  
_reactpack - :package: build your react apps with one command and one \`npm i\`._github.com][anchor2][][anchor3]

---

#### 실행
    
    $npm install

을 통해 dependency 가 걸려있는 라이브러리들을 내려받고는
    
    $node server

를 실행시키면 에러가 납니다. lodash는 공통적으로 package.json파일에 누락되어 있네요.

.env파일의 database만 설정해 주고 다시
    
    $node server

![][image3]기대보다 좋아요!

만들어진 소스 진입점은
    
    import 'whatwg-fetch';  
    import React from 'react';  
    import ReactDOM from 'react-dom';  
    import { Provider } from 'react-redux'  
    import { Router, browserHistory } from 'react-router';  
    import configureStore from './store/configureStore';  
    import getRoutes from './routes';

    const store = configureStore(window.INITIAL\_STATE);

    ReactDOM.render(  
    <Provider store={store}\>  
    <Router history={browserHistory} routes={getRoutes(store)}/\>  
    </Provider\>,  
    document.getElementById('app')  
    );

redux, router,fetch등 React 가 minimal로 가져야 할 것들을 훌륭하게 갖고 있습니다.

서버쪽 라우팅은 아래와 같이 express 가 지원.

![][image4]

node DB모듈은 knex를 쓰고 있습니다.
    
    var config = require('../knexfile');  
    var knex = require('knex')(config);  
    var bookshelf = require('bookshelf')(knex);

    bookshelf.plugin('virtuals');

    knex.migrate.latest();

    module.exports = bookshelf;

---

mega라는 말을 쓰길래 덕후거나 허풍이 심한 프로젝트 아닐까 하고 의심의 눈을 가지고 프로젝트를 들여다 보니 이거 정말 볼매였습니다.

lodash 관련해서는 PU 날리기 좋은 타이밍인데요!

By [Keen Dev][anchor4] on [June 9, 2016][anchor5].

Exported from [Medium][anchor6] on May 31, 2017\.


[anchor0]: https://github.com/sahat/megaboilerplate "https://github.com/sahat/megaboilerplate"
[anchor1]: https://github.com/sahat/megaboilerplate
[anchor2]: https://github.com/olahol/reactpack "https://github.com/olahol/reactpack"
[anchor3]: https://github.com/olahol/reactpack
[anchor4]: https://medium.com/@keendev
[anchor5]: https://medium.com/p/135f6bd1fd28
[anchor6]: https://medium.com


[image0]: /images/1*9hd2zEsMImq0JR263UgPEA.png
[image1]: /images/1*JoTk4L5vzKYAmEbFqiANWQ.gif
[image2]: /images/1*jcu4CVJF9mz3-Np4nb_W2g.png
[image3]: /images/1*FLuS2KGtdgcB6uOILeq3PA.png
[image4]: /images/1*_kAzHMkVfSZdT9ZCZEumBg.pn