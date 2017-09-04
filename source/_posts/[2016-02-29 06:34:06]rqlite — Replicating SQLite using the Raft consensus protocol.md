---
title: "rqlite — Replicating SQLite using the Raft consensus protocol"
date: 2016-02-29 06:34:06
tags: github, github-trend, tech-trend 
---


분산환경을 위한 Database 복제에 대해서는 여러번 들어보셨을 거라고 생각합니다. rqlite는 sqlite 를 분산 환경에서 복제할 수 있게 만들어 주는 프로젝트입니다. sqlite를 그런 이유에서 쓸 만한 이유들이 그렇게 많은지는 모르겠습니다만 한번 들여다 보도록 하겠습니다.

2016/02/29 today's best ( 357 ★)

![][image0]

일단 consensus protocol 에 대해서 알아야 합니다.

[**Consensus (computer science)**  
_A fundamental problem in distributed computing and multi-agent systems is to achieve overall system reliability in the..._en.wikipedia.org][anchor0][][anchor1]

consensus 알고리즘은 멀티 에이전트와 분산 컴퓨팅 환경에서 시스템 오류를 해결할 수 있는 알고리즘입니다. leader 를 맡는 에이전트 하나를 기반으로 state machine 복제와 atomic broadcasting 에 대한 내용이 중점적인 골자를 이루고 있습니다. (응?)

이 consensus algorithm 혹은 protocol을 이해하기 쉽게 구현한게 raft 입니다.

[**Raft Consensus Algorithm**  
_Raft is a consensus algorithm that is designed to be easy to understand. It's equivalent to Paxos in fault-tolerance..._raft.github.io][anchor2][][anchor3]

잘 설명되어 있는 유튜브 내용입니다.

leader election 부터 자세히 설명하고 있습니다만, 듣고 있는 청중들은 무슨 내용인지는 잘 모르는 눈치입니다. 거지같은 카메라워크라는 댓글이 눈에 띄네요.

이 raft를 사용해 만든 어플리케이션 중에는 RethinkDB가 눈에 띕니다.

그리고 오늘 소개하는 rqlite 입니다.

#### 1- 설치 및 실행
    
    mkdir rqlite \# Or any directory of your choice.  
    cd rqlite/  
    export GOPATH=$PWD  
    go get -t github.com/otoolep/rqlite/...  
    $GOPATH/bin/rqlited ~/node.1

이렇게 하면 4001번 포트를 사용해서 시작이 됩니다.

#### 2- 클러스터 만들기
    
    $GOPATH/bin/rqlited -http localhost:4003 -raft :4004 -join :4001 ~/node.2  
    $GOPATH/bin/rqlited -http localhost:4005 -raft :4006 -join :4001 ~/node.3

3,5,7의 갯수로 만드는게 현명하다는군요

#### 3- 인사이트

clustered DB를 만드는데 유용하게 쓰이는 raft가 sqlite 버전도 나온이상 RethinkDB는 꼭 한번 다뤄봐야겠다는 생각이 듭니다.

그나저나 freecodecamp는 한달 가까이 1등 근처를 내려오지 않는군요. 이번주에는 한번 다녀와 보고 싶네요.

By [Keen Dev][anchor4] on [February 28, 2016][anchor5].

Exported from [Medium][anchor6] on May 31, 2017\.


[anchor0]: https://en.wikipedia.org/wiki/Consensus_%28computer_science%29 "https://en.wikipedia.org/wiki/Consensus_(computer_science)"
[anchor1]: https://en.wikipedia.org/wiki/Consensus_%28computer_science%29
[anchor2]: https://raft.github.io/ "https://raft.github.io/"
[anchor3]: https://raft.github.io/
[anchor4]: https://medium.com/@keendev
[anchor5]: https://medium.com/p/288767738bf8
[anchor6]: https://medium.com


[image0]: /images/1*uvCAYCFZhR9XXGVNGWa3QQ.pn