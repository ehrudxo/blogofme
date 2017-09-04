---
title: "CASH — Cross-platform Linux without the suck"
date: 2016-02-25 06:40:42
tags: github, github-trend, tech-trend 
---


제목 한번 찰진 듯 합니다. CASH라니. 게다가 자기 소개도 도발적. 리눅스 Shell을 virtualization 하는 기술은 아니군요. Node.js 기반으로 Linux 명령어를 만들고 있습니다 Cygwin 처럼 이해하면 될 것 같은데, dll기반이 아니라는 점을 장점으로 이야기 하고 있네요. 주 타깃층은 Windows 환경에서 Linux 커맨드를 쓰고 싶어 하는 사람일 거 같습니다. 아직은 명령어가 많지는 않지만, 누가 알겠습니까? 향후 플랫폼 처럼 사용될 지

2016/02/25 Today's best ( 1671 ★ )

![][image0]

내용을 한번 들여다 보죠.

1- 명령어

지금 지원하고 있는 명령어는 다음과 같습니다.

* alias
* cat
* cd
* cp
* echo
* grep
* kill
* less
* ls
* mkdir
* mv
* pwd
* rm
* sort
* touch
* unalias

[https://github.com/dthree/cash/wiki/Roadmap][anchor0] 에 들어가시면 다음 명령어 개발을 위한 한표도 행사할 수 있습니다. Feedback 기반으로 개발하는 정말 훌륭한 개발자네요.

2- 설치
> 
> npm install cash -g

> cash@0.2.1 /usr/local/lib/node\_modules/cash  
> ├── filesize@3.2.1  
> ├── minimist@1.2.0  
> ├── vorpal-less@0.0.13 (slice-ansi@0.0.3)  
> ├── vorpal-autocomplete-fs@0.0.3 (strip-ansi@3.0.1)  
> ├── chalk@1.1.1 (escape-string-regexp@1.0.5, supports-color@2.0.0, has-ansi@2.0.0, strip-ansi@3.0.1, ansi-styles@2.2.0)  
> ├── fkill@3.1.0 (arrify@1.0.1, pify@2.3.0, taskkill@1.0.0, pinkie-promise@2.0.0)  
> ├── glob@6.0.4 (path-is-absolute@1.0.0, inherits@2.0.1, inflight@1.0.4, once@1.3.3, minimatch@3.0.0)  
> ├── vorpal-grep@0.1.2 (glob@5.0.15)  
> ├── fs-extra@0.23.1 (path-is-absolute@1.0.0, jsonfile@2.2.3, graceful-fs@4.1.3, rimraf@2.5.2)  
> ├── username@1.0.1 (meow@3.7.0)  
> ├── lodash@4.5.1  
> └── vorpal@1.9.5 (mindash@4.5.0, node-localstorage@0.6.0, strip-ansi@3.0.1, log-update@1.0.2, inquirer@0.11.0, babel-polyfill@6.5.0, babel-runtime@6.5.0)

위와 같은 dependency를 가지네요.

3- 실행

cash 명령어를 치거나 아예 글로벌 커맨드로 사용할 수 있습니다
    
    npm install cash-global -g

같이 명령어를 사용한다면 말이죠.

실행되는 예제는 다음 화면이 더 도움이 될 듯합니다

![][image1]

4- 인사이트

[https://github.com/dthree/vorpal][anchor1] 프로젝트가 있습니다.

* Node's framework for interactive CLIs

CASH가 나오게 된데에는 미리 이런 프로젝트를 통해 기반 기술이 확보되어 있습니다.

Node는 실제로 CrossPlatform 어플리케이션을 개발하는데 점점 더 많이 쓰여지고 있습니다. Write Once, Run Everywhere를 얘기하던 옛 Java 처럼 많은 어플리케이션이 도입되고 있네요.

By [Keen Dev][anchor2] on [February 24, 2016][anchor3].

Exported from [Medium][anchor4] on May 31, 2017\.


[anchor0]: https://github.com/dthree/cash/wiki/Roadmap
[anchor1]: https://github.com/dthree/vorpal
[anchor2]: https://medium.com/@keendev
[anchor3]: https://medium.com/p/525d7d2b27eb
[anchor4]: https://medium.com


[image0]: /images/1*wuFiHf8_uTy8UDTkb8K4Bw.png
[image1]: /images/1*KF2mU_F9Sk3Kac7oYdhd8w.gi