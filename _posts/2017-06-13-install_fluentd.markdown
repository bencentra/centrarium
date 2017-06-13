---
layout: post
title:  "Centos Fluentd 설치"
date:   2017-06-13 08:43:59
author: Beom
categories: Fluentd
---

Before Installing Fluentd
설치전에 해야 할 서버 환경 셋팅

Set Up NTP
파일 디스크립터가 1024일 경우 65535로 변경
```
$ ulimit -n
1024
```
```
$ vi /etc/security/limits.conf

root soft nofile 65536
root hard nofile 65536
* soft nofile 65536
* hard nofile 65536

```
Optimize Network Kernel Parameters
네트워크 파라메타 변경
```
$ vi /etc/sysctl.conf

net.ipv4.tcp_tw_recycle = 1
net.ipv4.tcp_tw_reuse = 1
net.ipv4.ip_local_port_range = 10240    65535
```

재부팅 하여 설정 적용

Install td-agent

td-agent는 Fluentd를 사용하기 편하게 래핑? 한 패키지로 보면 된다.

CentOS and RHEL 5, 6, 7 and Amazon Linux are currently supported.

```
$ curl -L https://toolbelt.treasuredata.com/sh/install-redhat-td-agent2.sh | sh
```

Service 스타트
```
$ /etc/init.d/td-agent start 
Starting td-agent: [  OK  ]
$ /etc/init.d/td-agent status
td-agent (pid  21678) is running...
```

서비스 명령어
```
$ /etc/init.d/td-agent start
$ /etc/init.d/td-agent stop
$ /etc/init.d/td-agent restart
$ /etc/init.d/td-agent status
```

테스트 로그 전송
```
$ curl -X POST -d 'json={"json":"message"}' http://localhost:8888/debug.test
```

다음 포스트는 Confige 설정과 로그 수집 데모