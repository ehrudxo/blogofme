---
title: "[github-trend]Draft.js"
date: 2016-02-24 06:46:07
tags: github, github-trend, tech-trend 
---


Facebook개발자들은 오픈소스 할만할 거 같다는 생각이 듭니다. 하루만에 2614개의 별이라니.. 덜덜.

React 기반의 RichText 에디터를 공개했습니다.

2016/02/24 Today's best ( 2614★)

![][image0]1등

1\. 설치 및 실행
    
    git clone https://github.com/facebook/draft-js.git  
    cd draft-js  
    npm install  
    npm run build

git clone을 받고 나면 npm 으로 설치를 하고 빌드를 돌리고 나면 dist 폴더에
> 
> Draft.css Draft.js Draft.min.js

세 파일을 생성해 줍니다.

2\. 샘플(Example)

Example 폴더에는 몇가지 예제 파일들이 있습니다.
> 
> color link rich tweet  
> entity plaintext tex

rich 를 확인해 보겠습니다.
> 
> <Editor  
> blockStyleFn={getBlockStyle}  
> customStyleMap={styleMap}  
> editorState={editorState}  
> handleKeyCommand={this.handleKeyCommand}  
> onChange={this.onChange}  
> placeholder="Tell a story..."  
> ref="editor"  
> spellCheck={true}  
> /\>

의외로 싱겁습니다. JSX는 Editor 태그를 통해서 결정하게 됩니다.

3\. 인사이트

RichText 에디터를 어떤 걸 쓸까 다들 많이 고민할 거 같습니다. 이미 나와 있는 것들도 많고, 하지만 라이센스 문제부분들을 생각하고 React 를 그대로 쓰는 입장에서는 반길 만한 프로젝트라고 보여집니다.

흥미로운 것은 React기본 컴포넌트에 Draft 가 들어가지 않은 점이구요. 앞으로 기대가 되는 것은 Image 업로드 부분을 어떻게 처리할지, 자신들의 Facebook 페이지에 이걸 적용할지 등등 입니다.

By [Keen Dev][anchor0] on [February 23, 2016][anchor1].

Exported from [Medium][anchor2] on May 31, 2017\.


[anchor0]: https://medium.com/@keendev
[anchor1]: https://medium.com/p/e84a955a470
[anchor2]: https://medium.com


[image0]: /images/1*OKLhwK4NgCUmzTU6wGuRkQ.pn