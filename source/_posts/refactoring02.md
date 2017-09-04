---
title: ES2015 리팩토링 – 2. 빠레꽁(var let const)
date: 2017-08-01 11:36:53
tags: JavaScript, Refactoring
---

JavaScript 는 언제나 쉽지만 또 언제나 어렵다.  
이런 개념을 처음 갖게 된게 아마도 변수가 내가 생각하는데로 작동하지 않던 시점이었던 것으로 기억한다.
개념이 생기기 전에 var를 변수 선언 해도 작동이 되고 생략해도 작동이 된다는 사실에 그냥 작성하다가 어느 새
나의 코드가 전역 변수가 되어 팀원 모두가 고생을 겪고, 변수 선언을 위에다 했는데 아래에서 올라오는 등의 경우의
내 머리속의 컨셉과 다르게 동작하는 경험을 겪고 나면 정말 혼란스러워 지는데 거기다 더해 지금 이글에서 언급하게
될 스코프, 호이스팅 등을 읽고나면 정말로 쉽지 않다라는 사실을 겪게 된다.  

ES2015 부터는 변수가 두가지 더 추가가 되었다. 이번엔 그 변수들을 어떻게 이해하고 언제 사용해야 할 지에 대해서 다뤄보겠다.

## JavaScript 변수 var 에 대해서

var 밖에 없었으니까 JavaScript 변수 var 에 대해서라고 제목을 정하고 들어가 보자.
몇가지 특징만 짚어 보고 넘어가겠다. JavaScript 변수에 대한 조금 더 자세한 내용은 JavaScript Definite Guide 를 추천한다.

### 1. 변수의 var 선언이 없으면 코드의 복잡성이 증가하게 된다.
일단 코드를 살펴보자.

```JavaScript
function outer(){
 function inner(){
    x=4;
  }
  inner();
  console.log("outer",x);
}
//혹은 조건문 블럭으로 진행해도 결과는 같다.
function outer(){
 if(true){
    x=4;
  }
  console.log("outer",x);
}
```
JavaScript는 나름 중첩시킨 함수 임에도 불구하고 x는 4를 출력하게 되어 있다. var 선언을 하지 않고 작성하면 기본적으로
직전의 상위 스코프의 변수를 찾게 되어 있는데 직전에도 선언이 되어 있지 않으면 하나 더 상위를 찾아 가게 된다. 이런식으로
의도하지 않은 전역 변수를 만들어 내고는 한다.

그렇다고 해서 선언 하기 전에 마구 사용해도 되느냐 하면 그것은 또 아닌 것이 x=4 위에 사용하면 undefined 를 출력하도록
되어 있다.

### 2. 호이스팅에 대해서

아래 두 코드는 위의 전역 변수에 대한 개념과 변수 스코프 끌어올림(호이스팅)에 대한 개념이 섞여 있는 예제이다.
두 코드의 차이점을 한 눈에 알아 볼 수 있을까?

- var 선언을 안 한 경우
```JavaScript
function outer(){
  x=3;
  function inner(){
    console.log("inner",x);
    x=4;
  }
  inner();
  console.log("outer",x);
}
```
- var 선언을 한 경우

```JavaScript
function outer(){
  x=3;
  function inner(){
  console.log("inner",x);
  var x=4;
  }
  inner();
  console.log("outer",x);
}
```

var 선언을 안 한 경우 경우는 ( inner =3 , outer = 4 ) 의 결과가, var 선언을 한 경우 경우는 inner는
undefined 가 outer의 경우는 3 이 떨어진다.  
왜 그럴까. var 선언을 안 한 경우 경우 결국 x의 스코프는 inner 안에서 찾을 수 없어서 outer 까지 가서 찾아 보게 된다.
호이스팅이라는 어려운 말로 적혀있지만 이 "찾아보게 된다"라는 개념으로 일단 이해하고 넘어가셔도 많은 경우에는 적용이 된다.
조금 더 확실한 의미로는 변수 선언을 끌어올림이 더 적절한 풀이가 되겠지만.
이렇게 이해하고 나면 두번째의 "var 선언을 한 경우 경우"는 오히려 더 자세히 이해가 된다.
var 선언을 한 시점에서는 스코프는 해당 함수 블럭만 찾게 될 것이고 선언이 안된 체로 사용이 되었으니 말이다.

코딩 인터뷰에나 나올 만한 이 문제는 우리가 일반적으로 JavaScript를 처음 접할 때의 난해함으로 다가온다.
블럭이 스코프를 결정하지 않는다니. 기상 천외한 언어라고 볼 수 있다.
하지만 이렇게 함으로써 브라우저 상에서 사람들이 처음 HTML 스펙과 적절히 섞을 수 있도록 사용 되었고(script 태그가 여기 저기서 얼마나 많이 import 되고 있는지 생각해 보라.) 이 호이스팅과 전역변수를 활용한 팁들도 생겨나기 시작했다.

하지만 지금의 상황은 자바스크립트의 코드베이스가 예전과는 상상도 할 수 없을만큼 커져버렸다.
전역변수를 사용한다는 것은 점점 죄악시 되어가고 있고, 좋은 패턴도 아니다.

### 3. 비동기 함수에서의 변수 사용

아래의 코드를 살펴보면 비동기 함수의 경우는 변수가 내가 원하는 시점과 원하는 바가 다르게 나올 때가 있다는 것을 파악할 수 있다.
```JavaScript
var numbers = [1,2,3,];

for (var i = 0; i < numbers.length; i++) {
  setTimeout(function () {
    console.log(numbers[i]);
  }, 0);
}
//결과는 undefined가 세번 나온다.
```
물론 저런 코드가 프로젝트에서 사용되어질 리는 없지만 setTimeout이 아니라 AJAX 호출이라고 생각해 보자.  
JavaScript가 눈에 익은 사람은 저 코드가 굉장히 당연하게 느껴지겠지만 콜백함수라던지 받아서 실행해야 하는 경우라면
코드에 대한 명확한 스펙을 알고 있더라도 실수할 수 있는 여지는 많아진다.

## let, const 에 대한 오해

이해도 하기 전에 오해를 이야기 하니 무슨 이야기인가 싶을 수도 있겠으나 ES2015 의 스펙이 나오면서 let 과 const 가 어떤 전역변수와 지역변수를 해결하는 전가의 보도처럼 이야기 되는 경우가 있어서 그런것 만은 아니라는 이야기를 먼저 하고 싶다.

여전히 ES2015에도 변수를 선언하지 않고 작업을 하면 함수 스코프를 따라 체이닝 작업(찾아보게 된다)을 통해 변수에 값을 할당하게 된다. 이것은 바꿀 수도 없고 바꿔서도 안된다고 보인다.
하지만 아래 코드를 보자. 위의 var로 선언한 코드에서 let 으로만 선언했을 뿐이다.
```JavaScript
function outer(){
  x=3;
  function inner(){
  console.log("inner",x);
  let x=4;
  }
  inner();
  console.log("outer",x);
}
```
두가지의 결과가 다르게 나는데 var로 선언을 할 경우는 undefined 라는 값이 나오고( 에러가 아니다!)
let의 경우는 에러를 내뱉게 된다. (명시적인 에러를 뱉는 것과 undefined를 처리하는 것은 개발 차원에서 다뤄야 할 수준이 달라진다)

### let은 무엇이 다를까

앞서 언급했던 선언을 하지 않고 사용을 하면 에러가 나도록 설계가 되어 있다는 점이 일단 이야기가 되어지고 두번째는 반복문 안에서 비동기 동작이 다르게 작동한다.  

이 부분도 코드를 먼저 보자. 먼저 소개한 코드에서 var를 let으로 바꿨을 뿐이다.
```JavaScript
var numbers = [1,2,3,];

for (let i = 0; i < numbers.length; i++) {
  setTimeout(function () {
    console.log(numbers[i]);
  }, 0);
}
```
개인적으로 이 부분은 조금 더 헷갈리게 된 것 같다. 비동기의 경우 var처럼 처리 되던것을 기본으로 생각해오던 JavaScript 개발자들에게는 오히려 혼란스럽게 다가올 수 있을 것으로 보이지만 이제는 비동기 때 변수가 따로놀지 않는 상황을 let으로 작성하면 만들 수 있다는 점에서 의미가 있을 거 같다.

### const는 무엇이 다를까
다른 언어와 마찬가지로  const의 경우는 다시 할당하지 않는 상수의 역할을 한다. const 의 경우는 재할당 하려고 하면 에러가 난다.
let 과 비교하면 값을 재할당 할 수 없는 것 딱 한가지 말고는 다를 바가 없다.

## 이제는 무조건 let, const다. 외워라.
브라우저는 지속적으로 발전하고 있고 그에 따른 성능도 올라가지만 한가지 확실한 것은 표준 스펙에 대한 성능은 언제나 일순위라는 것이다.
그 과정에서 let, const 는 기존의 var를 완전히 대체할 수 있는 뉴 스탠다드다. 현재는 var 가 아주 조금 (그것도 아주 조금) 성능적인 우위를 점하고 있지만 장기적으로 let, const 와의 성능은 거의 차이가 없어질 것으로 (오히려 더 나아질 것으로) 예상된다.

실제 진행한 것을 블로그에 포스팅한 사례도 속속 나오고 있다.

성능 비교 : [https://gomugom.github.io/let-vs-var-performance-compare/](https://gomugom.github.io/let-vs-var-performance-compare/)

내용을 한 부분만 인용하면
>불과 1년 전 var와 let의 성능비교 테스트에 대한 블로그 포스팅을 읽은 적이 있는데, 당시에는 var가 let보다 압도적으로 빠르게 연산을 수행했던 것으로 기억한다. 그 1년 사이 둘의 성능은 같아졌다. 그만큼 최적화가 이루어져왔었기 때문이다. 그렇다면 앞서 확인했던 외부스코프에 대한 접근 성능 역시 점차 최적화가 될 것이라 기대한다.

이 블로그 포스팅도 2017년 1월의 일이니 지금은 더 빨라졌을 것으로 보인다.

그리고 앞서 언급되어 있었던 부분 중의 하나인 에어비앤비의 사례에서도 보듯이 엔지니어링에서 표준을 따라 작업을 하는 것이 현재의 성능을 쫓아가는 것 보다 장기적으로 이득인 점도 간과할 수는 없다.

## 프로젝트 리팩토링

이제는 standup 프로젝트를 한번 들여다 보자. ( github 페이지에 접속해서 standup 검색을 하거나 아래 URL을 클릭해서 들어가 보자. )

https://github.com/ehrudxo/standup

주소를 복사해서 git clone 명령을 통해 사용하고 있는 로칼 PC에 복사한 후에 가장 마지막 작업인 day7 을 체크아웃 받아 보자.

```bash
$git clone https://github.com/ehrudxo/standup & cd standup & git chekcout day7
```

이후 editor 를 구동시킨 후에 탐색기를 열고 프로젝트에서 var를 검색해 보자. 다음 8개의 파일이 var로 이루어져 있다.

```
REAMDE.md
src/__tests__/CloudDao.js
src/actions/Article.js
src/config.js
src/Editor.js
src/FileUtil.js
src/FirebaseDao.js
src/Login.js 
```

이 중 README.md 파일은 다른 파일을 설명하면서 만든 파일이므로 나머지 파일을 바꾸고 리팩토링 해 보자. 먼저 FileUtil.js를 살펴보면 
storageRef 와 ulpoadTask 가 var 로 지정되어 있다. 그런데, storageRef 를 살펴보니 다른데서 사용하고 있지 않다.  uploadTask만 재사용 되므로 storageRef는 삭제하고 uploadTask는 다시 값이 할당되지 않으므로 const로 변경 해보자.

이번에는 src/actions/Article.js 를 살펴 보자. 이번에는 독자들을 위해 코드 스니펫을 가지고 와서 확인해 보도록 한다.
```JavaScript
export function getArticles(articles){
  var items = [];
  articles.forEach(function(article){
    var item = article.val();
    item['key'] = article.key;
    items.push(item);
  })
  if(items && items.length>0){
    return{
      type : ALL,
      articles : items.reverse()
    }
  }
}
```
여기서 items 는 push 명령어를 통해서 지속적으로 변경이 되니까 let으로 지정을 해야 할 것 같지만 참조형은 변경이 가능하므로 const 를 사용한다.
그리고 item 도 다시 할당하지 않으므로 모두 const 로 변경한다.
```JavaScript
export function getArticles(articles){
  const items = [];
  articles.forEach(function(article){
    const item = article.val();
    item['key'] = article.key;
    items.push(item);
  })
  if(items && items.length>0){
    return{
      type : ALL,
      articles : items.reverse()
    }
  }
}
```
이 후 나머지는 독자들이 변경해 보도록 하자.
그리고 제대로 동작하는지 확인하려면 다음의 명령어를 실행해 보자.
```bash
$npm install & npm start
```