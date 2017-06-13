---
layout: post
title:  "Introduce of Fluentd"
date:   2017-06-13 08:43:59
author: Beom
categories: Fluentd
---

빅데이터 흐름을 익히기 위해 아래와 같은 구조의 프로세스를 구상 중
WAS -> fluentd -> kafka -> spark Streaming -> HFDS 
( or spark streaming -> Easticsearch -> Kibana )

이중 분산로그 수집을 위해 사용 할 fluentd에 대한 정리

아래 그림은 Fluentd에 대해 한장으로 잘 표현한 그림이다.

| column | column |
|--------|--------|
|<img src="https://github.com/ntmaster84/ntmaster84.github.io/blob/master/_posts/resource/fluentd-before.png?raw=true" width="300">|<img src="https://github.com/ntmaster84/ntmaster84.github.io/blob/master/_posts/resource/fluentd-architecture.png?raw=true" width="300">|

자세한 내용은 조대협님의 블로그에 잘 정리 되어 있다.

[Fluentd 간단 정리 바로가기](http://rnder.tistory.com/25)




