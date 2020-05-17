---
layout: post
title: Docker Windows 10 home 환경에서 설치하기
subtitle: Docker Toolbox 소개 및 Mysql 설치 및 구동까지.
gh-repo: hwayoungjun/hwayoungjun.github.io
gh-badge: [star, fork, follow]
tags: [docker]
comments: true
image: /img/docker_logo.jpg
categories : [spring]
pagination: 
  enabled: true
---

처음 RDBMS 설치할 적에 굉장히 애를 많이 먹었던 기억이 납니다. 게다가 한번 잘못 설치해서 지우고 다시 깔아야 하는 날에는... 차라리 포맷을 하는게 낫겠다는 생각까지 했었죠.

Docker 는 개발 생태계를 완전히 바꾼 플랫폼이라고 생각합니다.

Docker 공식 문서에서 발췌해온 소개글입니다. [Docker Docs](https://docs.docker.com)

{: .box-note}
Docker is an open platform for developing, shipping, and running applications. Docker enables you to separate your applications from your infrastructure so you can deliver software quickly. With Docker, you can manage your infrastructure in the same ways you manage your applications. By taking advantage of Docker’s methodologies for shipping, testing, and deploying code quickly, you can significantly reduce the delay between writing code and running it in production.

...인프라랑 App을 분리해준다고? App을 관리하는 방법과 같은 방법으로 인프라를 관리한다고?
<br>
<br>
무슨 말인지 지금은 도통 알 수가 없습니다. 일단 설치부터 해봅시다.

그런데 지금 제 노트북은 Windows 10 home 버전인 관계로 legacy 버전? 이라고 할 수 있는 Docker Toolbox 를 쓸겁니다.

**Docker Toolbox 는 Docker Desktop 에서 사용하는 Hyper-V 라는 가상화 기술을 미지원하는 OS 를 위해 만들어진 installer 입니다.**

{: .box-note}
Docker Toolbox is an installer for quick setup and launch of a Docker environment on older Mac and Windows systems that do not meet the requirements of the new Docker Desktop for Mac and Docker Desktop for Windows apps.

만약 상위 버전의 Windows 를 사용하시는 분이라면 Docker Desktop 을 사용하시면 되겠습니다.
<br>
<br>
하단 Git 배포 페이지에서 exe 또는 맥사용자라면 pkg 파일을 다운받아주세요. 

[Docker ToolBox 설치](https://github.com/docker/toolbox/releases)

다운받은 설치프로그램을 실행해보시면

![docker](https://hwayoungjun.github.io/img/docker_install_1.PNG)

설치 관련 이슈 등에 대해 도커에게 제공할 것인지 묻고 있습니다. 쿨하게 보내줍시다.
<br>
<br>
<br>
<br>
![docker](https://hwayoungjun.github.io/img/docker_install_2.PNG)

이번엔 설치할 컴포넌트를 선택하는 화면입니다.

**Docker Machine** 은 쉽게 말하자면 가상 호스트를 제공해주는 툴이라고 보시면 되겠습니다. Docker Desktop 을 사용할 경우 로컬 호스트(127.0.0.1)를 사용할 수 있지만 Docker Toolbox 의 경우 Docker Machine 에서 주는 가상 IP 를 통해야 Docker 컨테이너에 접근 가능합니다.

{: .box-note}
Docker Machine is a tool that lets you install Docker Engine on virtual hosts, and manage the hosts with docker-machine commands.

**Docker Compose** 는 멀티 컨테이너를 정의하고 실행할 수 있게 해주는 툴이라고 하는데 아직까진 사용해본 적이 없네요. 설치하지 않으셔도 무방하니 필요없으신 분은 과감히 체크 해제 해주시면 됩니다.

{: .box-note}
Compose is a tool for defining and running multi-container Docker applications. With Compose
<br>
<br>
<br>
<br>
![docker](https://hwayoungjun.github.io/img/docker_install_3.PNG)

이제 바탕화면 바로가기 아이콘을 만들지, 시스템 환경변수에 추가할지 등을 묻는 화면입니다. 환경변수는 소중하니 무조건 넣도록 합시다.

환경변수 추가하실 경우 DOCKER_ 로 prefix 된 환경변수 등이 추가됩니다.

![docker](https://hwayoungjun.github.io/img/docker_install_4.PNG)

**DOCKER_HOST** 라는 환경변수의 값이 앞으로 사용할 Docker Machine 이 제공하는 가상 호스트입니다. Docker 컨테이너에 설치한 DB, Server 등에 접근 시 이 가상 호스트 IP 를 통해 접근할 것입니다.
<br>
<br>
<br>
<br>
설치가 완료됐으면 이제 Docker 를 실행해봅시다.

Docker QuickStart Terminal 또는 Docker 설치경로 내 start.sh 를 통해 실행 가능합니다.

![docker](https://hwayoungjun.github.io/img/docker_install_5.PNG)

위 사진과 같이 귀여운 도커 고래가 뜬다면 설치 완료입니다. 
<br>
<br>
<br>
<br>
다음 포스팅은 Mysql 설치 및 포트 분리를 통한 2대의 Mysql 구동 테스트로 찾아뵙겠습니다.
<br>
<br>
---------------------------------------
> 틀린 내용이 있다면 개인메일로 언제든지 피드백 부탁드립니다.
> jun9813@gmail.com
<br>
