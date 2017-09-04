---
title: "[github-trend]swift web-frameworks"
date: 2016-02-23 05:52:28
tags: github, github-trend, tech-trend 
---


오늘은 swift로 된 두개의 web-framework 가 동시에 깃헙 트렌딩에 올라 왔습니다.

2016/02/23 editor's choice

하나는 vapor라는 녀석이구요.또 다른 하나는 SwiftOn 입니다.

**1.Vapor**

![][image0][https://github.com/qutheory/vapor][anchor0]

보시다시피 Laravel/Lumen 으로부터 영감을 받았다고 합니다. iOS,OSX, Linux에서 돌아가도록 만들었다고 합니다.

일단 실행환경을 보면 Ubuntu를 위한 example 과 docker 파일들이 있습니다.

heroku에서 돌리기 위해서는 [https://github.com/kylef/heroku-buildpack-swift][anchor1] 빌드팩을 참조하면 됩니다.

잘 돌아가는 예제는 [http://vapor.qutheory.io/][anchor2] 에서 확인할 수 있습니다.

swifton.me 라는 온라인 실행환경 사이트에서 example을 돌려보면 같은 결과를 확인할 수 있습니다.

![][image1]app is being deployed

![][image2]

서비스를 구성하는 것은 간단합니다.
    
    import Vapor  
      
    let server = Server()  
    server.run()

이렇게 간단하게 서버를 기동 시킬 수도 있지만,
    
    Route.get("solar-system") { request in  
    let json = \[  
    "planets" : \[  
    "mars",  
    "venus",  
    "jupiter",  
    "earth"  
    \]  
    \]  
    return Json(json)  
    }

와 같은 형태의 Routing 도 가능하군요.

흥미로운 것은, [vapor-stencil][anchor3] ([Stencil][anchor4]의 implementation for vapor)이라는 자매프로젝트로 View 단의 Template 언어로 사용하는 점과 MiddleWare를 활용한다는 점입니다.

**2\. SwiftOn**

두번째는 SwiftOn 입니다.

![][image3]

이 프로젝트는 RubyOnRails에서 영감을 받았다고 하는군요. 음 위의 짤이 뭘 의미하는지는 잘 모르겠습니다.

똑같이 Heroku빌드팩과 Docker 파일을 포함하고 있습니다.

코드도 대강 비슷합니다.
    
    let router = Router()  
    router.get("/todos/new", TodosController()\["new"\])  
    router.get("/todos/{id}", TodosController()\["show"\])  
    router.get("/todos/{id}/edit", TodosController()\["edit"\])  
    router.get("/todos", TodosController()\["index"\])  
    router.post("/todos", TodosController()\["create"\])  
    router.delete("/todos/{id}", TodosController()\["destroy"\])  
    router.patch("/todos/{id}", TodosController()\["update"\])

당연히 router를 포함하고, stencil을 사용하는것, 미들웨어를 포함하고 JSON응답을 지원하는 등.

**3\. 인사이트**

Swift는 애플이 오픈소스로 풀자마자 이렇게 많은 프로젝트로 확장되는 걸 보면, 정말 올바른 선택을 한 것이 아닌가 하는 생각이 듭니다.

노드 생태계의 express 나 ROR 처럼 일통하는 프레임워크가 언젠가 나올 수 도 있고, Python 처럼 난립할 수도 있겠지만, 웹 프레임워크의 지속적인 등장은 Swift서버 생태계가 풍성해지는 가장 좋은 방법이라고 생각합니다.

지속적으로 Swift를 지켜봐도 괜찮을 거 같습니다.

By [Keen Dev][anchor5] on [February 22, 2016][anchor6].

Exported from [Medium][anchor7] on May 31, 2017\.


[anchor0]: https://github.com/qutheory/vapor
[anchor1]: https://github.com/kylef/heroku-buildpack-swift
[anchor2]: http://vapor.qutheory.io/
[anchor3]: https://github.com/qutheory/vapor-stencil
[anchor4]: https://github.com/kylef/Stencil
[anchor5]: https://medium.com/@keendev
[anchor6]: https://medium.com/p/ffc493c7b4f5
[anchor7]: https://medium.com


[image0]: /images/1*HV_TmmL13N2MP_edFhMJ2w.png
[image1]: /images/1*OY-v6I3MY54hHoAW1czXFA.png
[image2]: /images/1*j4lqs3CWXyurqJ5HQGcDGg.png
[image3]: /images/1*igDzfZrE6oLTNHo7Q8sxog.pn