---
layout: post
title: Docker Windows 10 home 환경에서 설치하기
subtitle: Docker Toolbox 소개 및 Mysql 설치 및 구동까지.
gh-repo: hwayoungjun/hwayoungjun.github.io
gh-badge: [star, fork, follow]
tags: [docker]
comments: true
image: /img/docker_logo.jpg
---

처음 RDBMS 설치할 적에 굉장히 애를 많이 먹었던 기억이 납니다. 게다가 한번 잘못 설치해서 지우고 다시 깔아야 하는 날에는... 차라리 포맷을 하는게 낫겠다는 생각까지 했었죠.

Docker 는 개발 생태계를 완전히 바꾼 플랫폼이라고 생각합니다.

Docker 공식 문서에서 발췌해온 소개글입니다. [Docker Docs](https://docs.docker.com)

{: .box-note}
**Note:** Docker is an open platform for developing, shipping, and running applications. Docker enables you to separate your applications from your infrastructure so you can deliver software quickly. With Docker, you can manage your infrastructure in the same ways you manage your applications. By taking advantage of Docker’s methodologies for shipping, testing, and deploying code quickly, you can significantly reduce the delay between writing code and running it in production.

...인프라랑 App을 분리해준다고? App을 관리하는 방법과 같은 방법으로 인프라를 관리한다고?

무슨 말인지 지금은 도통 알 수가 없습니다. 일단 설치부터 해봅시다.

그런데 지금 제 노트북은 Windows 10 home 버전인 관계로 legacy 버전? 이라고 할 수 있는 Docker Toolbox 를 쓸겁니다.



**Docker Toolbox 는 Docker Desktop 에서 사용하는 Hyper-V 라는 가상화 기술을 미지원하는 OS 를 위해 만들어진 installer 입니다.**

{: .box-note}
**Note:** Docker Toolbox is an installer for quick setup and launch of a Docker environment on older Mac and Windows systems that do not meet the requirements of the new Docker Desktop for Mac and Docker Desktop for Windows apps.

만약 상위 버전의 Windows 를 사용하시는 분이라면 Docker Desktop 을 사용하시면 되겠습니다.


하단 Git 배포 페이지에서 exe 프로그램을 다운받아주세요. 

[Docker ToolBox 설치](https://github.com/docker/toolbox/releases)


