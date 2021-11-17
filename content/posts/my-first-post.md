---
title: "Hugo 시작하기"
date: 2021-11-12T21:07:15+09:00
draft: false
---

## Hugo 시작하기

> 휴고는 Go로 작성된 정적 사이트 생성기이다.
> 메인페이지에 가면 웹사이트 구축을 위한 세계에서 가장 빠른 프레임워크(The world’s fastest framework for building websites) 라고 안내하고 있다.

## 목차

1. Chocolate 설치[link: Chocolate 설치]
2. Hugo 설치[link: Hugo 설치]

### Chocolate 설치 (Windows)

> ## 윈도우 패키지 매니져인 Chocolatey 를 설치합니다.
>
> 1. Windows PowerShell을 관리자 모드로 실행합니다.
> 2. Command 복사해서 실행
>
> ```bash
> Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
> ```
>
> 3. 설치가 완료되면 command를 입력해서 설치를 확인힙니다.
>
> ```bash
> choco
> Chocolatey v0.11.3
> Please run 'choco -?' or 'choco <command> -?' for help menu.
> ```

### Hugo 설치 (Windows)

> ## 설치된 Chocolatey 로 Hugo를 설치합니다.
>
> 1. Cmder를 관리자 권한으로 실행합니다.
>
> ```bash
> choco install hugo -confirm
> #or
> choco install hugo-extended -confirm
> ```
>
> 2. command를 입력해서 설치를 확인합니다.
>
> ```bash
> hugo help
> ```

### Hugo 사이트 생성

> ## 설치된 Hugo 로 사이트를 생성합니다.
>
> ```bash
> hugo new site ironpot.app
> cd ironpot.app
> git init
> # 테마 설치하기
> git submodule add https://github.com/nanxiaobei/hugo-paper.git themes/paper
> echo theme = 'paper' >> config.toml
> # 첫번째 글 등록하기
> hugo new posts/my-first-post.md
> # 실행하기
> hugo server -D
> # Build static pages
> hugo -D
> ```

ref.

[https://gohugo.io](https://gohugo.io)
[https://chocolatey.org/install](https://chocolatey.org/install)
