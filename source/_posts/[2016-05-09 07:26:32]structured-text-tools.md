---
title: "structured-text-tools"
date: 2016-05-09 07:26:32
tags: github, github-trend, tech-trend 
---


![][image0]

jo라는 프로젝트를 리뷰한 적이 있습니다. json을 만들어 주는 프로젝트인데 command line툴을 활용하는 것이었습니다. 예를 들자면
    
    $ jo -p name=jo n=17 parser=false

라고 명령어를 치면
    
    {  
    "name": "jo",  
    "n": 17,  
    "parser": false  
    }

형태의 json 이 만들어 지는 거죠.

이런 일들을 해 주는 오픈소스 command line tools 들을 모아 둔 프로젝트입니다. json 이외에도 structured-text들이 어떤 것이 있는지 알아보기에도 좋은 프로젝트 입니다.

2016/05/09 Editor's choice

[**dbohdan/structured-text-tools**  
_What follows is a list of text-based file formats with command line tools for manipulating each (with a focus on Linux..._github.com][anchor0][][anchor1]

---

#### 어떤 것들이 있을까?

목차는 다음과 같습니다.

* DSV
* XML,HTML
* JSON
* YAML, TOML
* INI

---

#### DSV

DSV는 Delimiter-separated values 의 약자로 CSV 와 TSV를 포함하고 있습니다. 손쉽게 예를 들자면 text 파일안에 구분자를 두고 필드 속성을 할당하는 형태입니다. XML과 JSON이 나오기 전, 대부분의 텍스트 파일 인코딩은 속도를 위해 버퍼를 쪼개는 형식이 아니라면 이 형태를 사용했었습니다.

이 분야의 절대 강자라면 아무래도 오크(AWK) 겠죠.

![][image1]전 오크가 아닙니다.

awk는 상당히 많은 기능이 있는데, 다 소개하기는 곤란하고

빈도 체크를 위해 imsi.qwk 파일을 아래와 같이 만들고
    
    // 소스 원작 : [https://ko.wikipedia.org/wiki/AWK][anchor2]  
    {   
    **for** (i=1; i<=NF; i++)  
    words\[$i\]++  
    }  
      
    END {   
    **for** (i in words)  
    **print** i, words\[i\]  
    }

김건모의 잘못된 만남 가사를 입력하면

$ awk -f imsi.awk gunmo.txt

![][image2]그 어느날!

친구는이 6번 있군요... 같은 결과를 얻을 수 있습니다.

그 외에도 POSIX 커맨드 자체로도 이런 일들을 할 수 있고, GNU datamash, Miller, tab,xsv 같은 프로그램들을 링크로 소개하고 있습니다.

csv같은 경우는 database 툴들과 아주 밀접하게 관계가 있습니다. 아무래도 읽고 쓰는 방법이 밀접하게 연관되어 있으니까요.

관련된 툴도 설명하고 있네요

---

#### XML, HTML

15년전 병특할 때 XML개발자는 300만원(그 때 기준이니까... 좀 다르겠죠?) 씩 주면서 찾던 기억이 나네요. 이제는 그냥 기반 기술이 되어 버렸는데 말이죠.

xml, html 툴은 생각보다 많지 않은게 요즘은 json으로 대세가 넘어가서 그런가 봅니다. SAXON툴은 java의 SAX를 xml2는 libxml같은 걸 사용하는 걸 보면 올드하면서도 견고한(concrete) 라이브러리들 위주로 되어 있습니다.

그나마 최신 트렌드를 반영하는 pup는

go로 설치하거나 brew로 설치가 가능합니다.
    
    $go get github.com/ericchiang/pup

    or  
    $ brew install https://raw.githubusercontent.com/EricChiang/pup/master/pup.rb

이제는 데이타 스크래핑의 고전이 되어있는 해커뉴스의 링크를 얻어와 보겠습니다.
    
    $curl -s https://news.ycombinator.com/ | pup 'table table tr:nth-last-of-type(n+2) td.title a'

를 실행하면..

![][image3]

주루륵 결과가 떨어집니다.

주로 파싱에 관련된 부분입니다.

#### JSON

JSON은 뭔가 상당히 많을 거 같으면서도 좀 썰렁한데 있을 건 다 있는 느낌입니다.

![][image4]

자세한 설명은 jo를 위에 잠깐 언급한 걸로 대신하겠습니다. jq라던지, jshon등은 살펴보고 싶네요

#### YAML,TOML,INI

YAML은 루비 개발자들에게는 필수인 직렬화 형식으로 YAML이란 것은 마크업 언어가 아님을 천명하는 재귀적인 이름입니다. 리눅스처럼 말이죠
> 
> YAML Ain't Markup Language

자쿠와는 다르다! 자쿠와는!

jq, validyaml등을 소개하고 있습니다.

INI파일은 윈도우즈...설정파일의 대명사죠.

---

뭔가 빠진게 있을까 한참 생각을 해 봤는데, 최근에는 XML, JSON, YAML등 말고는 크게 사용할 일이 없을 거 같다는 생각이 듭니다.

By [Keen Dev][anchor3] on [May 8, 2016][anchor4].

Exported from [Medium][anchor5] on May 31, 2017\.


[anchor0]: https://github.com/dbohdan/structured-text-tools "https://github.com/dbohdan/structured-text-tools"
[anchor1]: https://github.com/dbohdan/structured-text-tools
[anchor2]: https://ko.wikipedia.org/wiki/AWK
[anchor3]: https://medium.com/@keendev
[anchor4]: https://medium.com/p/6567f7da692
[anchor5]: https://medium.com


[image0]: /images/1*96Dc_oYFvKKrU4BZEzSE7w.png
[image1]: /images/1*BvtMX-1l7AE0dn44S3-DHw.png
[image2]: /images/1*mh9wZQUyq8xHzIRWqw9FCg.png
[image3]: /images/1*vVfoTFdnhf5XzNELq6h-HQ.png
[image4]: /images/1*3SsRVJU-f82rH26amP77Lw.pn