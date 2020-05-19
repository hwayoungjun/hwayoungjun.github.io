---
layout: post
title: Jekyll 블로그 튜토리얼
subtitle: 로컬 환경 세팅
gh-repo: hwayoungjun/hwayoungjun.github.io
gh-badge: [star, fork, follow]
tags: [jekyll]
comments: true
---

**1. Ruby 설치**

[윈도우 Ruby 인스톨러](https://rubyinstaller.org/downloads/)

Ruby+Devkit 2.6.6-1 (x64) 버전 설치

(최신 버전은 미지원으로 플러그인 설치가 되지 않는 경우가 있음.)

**2. 필요한 플러그인 설치 진행**

깃 디렉토리로 이동 후 명령어 실행
> bundle install

**3. 로컬 환경에서 서버를 돌리기 위해 위해 Gemfile 수정**
> gem 'tzinfo-data', platforms: [:mingw, :mswin, :x64_mingw]

Gemfile 추가 및 주석 해제

**4. 서버 실행**
> chcp 65001

>   Conversion error: Jekyll::Converters::Scss encountered an error while converting 'assets/css/style.scss':
                    Invalid CP949 character "\xE2" on line 5

위와 같은 에러 방지

명령프롬프트 인코딩 설정

> bundle exec jekyll serve

로컬 실행 (Default 4000 포트를 사용한다.)


