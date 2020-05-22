---
layout: post
title: Git Public Repository 여러 계정 사용하기
subtitle: + Private Repository 에서 SSH 키 등록을 통한 SSH 인증
gh-repo: hwayoungjun/hwayoungjun.github.io
gh-badge: [star, fork, follow]
tags: [git]
comments: true
categories : git
---

**Public Repository 인 경우**

[Git와 연동된 소스폴더]/.git/config 로 이동 및 하단 단락 유저명/이메일 수정 후 추가
{% highlight java linenos %}
[user]
	name = username
	email = useremail@gmail.com
{% endhighlight %}
<br>
Crendential helper 신규 생성
{% highlight java linenos %}
git config credential.helper [헬퍼이름]
{% endhighlight %}
<br>

**Private Repository 인 경우**

RSA 키 생성
{% highlight java linenos %}
ssh-keygen -t rsa
{% endhighlight %}
<br>
깃허브에서 로그인 후 우측 상단 자신의 계정을 클릭한다.
![git](/img/git-cred-3.PNG)
계정 설정페이지로 이동
<br>
SSH and GPG keys 메뉴 클릭
![git](/img/git-cred-4.PNG)
<br>
새로운 SSH 키 생성
![git](/img/git-cred-5.PNG)
<br>
앞에서 생성한 RSA 키의 공개키 값을 key 로 등록한다 (.pub 확장자)
<br>
{% highlight java linenos %}
eval `ssh-agent -s`
ssh-add ~/.ssh/*_rsa
{% endhighlight %}


![git](/img/git-cred-1.PNG)
