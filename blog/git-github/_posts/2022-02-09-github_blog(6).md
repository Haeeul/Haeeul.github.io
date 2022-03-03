---
#007
layout: post
title: "GitHub 블로그 만들기 (6) - 블로그 댓글 기능"
image: https://user-images.githubusercontent.com/39720852/156387687-48397e83-3d7f-4aee-b091-35615fe2fa34.png
accent_image:
  background: url(https://user-images.githubusercontent.com/39720852/152405232-29b296d1-653c-4505-ad3c-07fd5a680d17.png) center/cover
  overlay: true
date: 2022-02-09 00:03:00 +0900
categories: git-github
tags: [GitHub Pages, GitHub blog, Jekyll, Jekyll theme, utterances]
description: >
  📝 GitHub 블로그에 댓글 기능을 추가합니다.
---

안녕하세요, 해을입니다🦖

이번 글에서는 <span style="background-color:#f1f8ff">**블로그 댓글 기능**</span>에 대해 알아보겠습니다!

* toc
{:toc}

## 💡블로그 댓글 기능

블로그에서 댓글 기능을 사용하기 위해서는 추가 설정이 필요합니다.

제가 사용하는 Hydejack 테마에서는 **Disqus**를 통해 댓글 기능을 지원하는데요.

설정을 위해 검색하다 보니 **Disqus가 광고가 많고 무겁다**는 얘기가 많았습니다.

그리하여 다른 댓글 플랫폼을 찾던 중에 발견한 <span style="background-color:#fff5b1">**utterances!**</span>

많은 분들이 사용하시기도 하고 장점도 많아서 바로 적용하기로 결정했습니다.

### 1. utterances

#### 📍 정의

utterances는 **GitHub 이슈 기능을 기반으로 한 댓글 위젯**입니다.

**게시글과 이슈가 1:1로 매핑**되는 구조로, 게시글에 댓글을 달면 해당 이슈 댓글에 추가됩니다.

이슈는 첫 댓글을 달 경우, utterances-bot이 자동으로 생성해줍니다.

![image](https://user-images.githubusercontent.com/39720852/156494767-c6c604ce-55ed-48c1-80a0-b05e1773c45d.png)

#### 📍 장점

* **무료로 사용 가능**

* **광고가 없고 가벼움**

* **간편한 설치 및 설정**

* **마크다운 문법 사용 가능**

* **댓글 알림 기능**
  * 이슈가 등록 시, 메일로 알림 받기 가능

* **GitHub 계정 사용**
  * 별도의 가입 없이 GitHub 계정을 사용하므로 주 방문자인 개발자 유저들에게 편리
  * 비회원 댓글 작성 방지

### 2. utterances 적용

#### 🥨 Repository 지정 또는 생성

이슈가 생성될 **댓글 Repository를 지정(본인의 블로그 Repository)하거나 새로 만들어줍니다.**

이때, <span style="background-color:#ffdce0">**댓글 Repository는 Public**</span>이어야 댓글 기능이 동작합니다.

저는 블로그 Repository가 private고 issue 기능을 사용하고 있어서 새로 만들었습니다.

![image](https://user-images.githubusercontent.com/39720852/156496563-e8fcdf7d-52d4-4907-93fb-28d3e666d4af.png)

#### 🥨 utterance app 설치

1. utterance [설치 페이지](https://github.com/apps/utterances)로 들어갑니다.
  ![image](https://user-images.githubusercontent.com/39720852/156577259-5b3218fa-17a5-40bd-8a79-be655cbff228.png)

2. 댓글을 업로드 할 **Repository를 선택**합니다.  
  (본인의 블로그 저장소 또는 새로 만든 댓글 저장소 선택)
  ![image](https://user-images.githubusercontent.com/39720852/156577844-acd23242-7128-494c-bd5d-424b39de5005.png){: width="450"}

3. 비밀번호 확인이 끝나면 아래 페이지로 이동하게 됩니다.
  ![image](https://user-images.githubusercontent.com/39720852/156582451-8e8b5fae-52fb-4b2e-a3c6-78507afe97ff.png)

#### 🥨 utterance 설정

1. 이동한 페이지에서 **Repository 부분에 자신의 github 아이디와 저장소 이름을 입력**합니다.
  ![image](https://user-images.githubusercontent.com/39720852/156582195-e0ba2a5c-953c-40f8-b31d-c8ab8c38eedd.png)

2. 게시글의 **이슈 매핑 방법을 선택**합니다.  
   (매핑인 만큼 대부분 수정할 일이 적은 **pathname을 사용**합니다.)
  ![image](https://user-images.githubusercontent.com/39720852/156584085-7c1837fc-1ff8-459b-a3e7-04bbec3e5ce5.png)

   * **pathname** : 게시글 pathname(ex : /blog/git-github/2022-02-08-title)으로 매핑
   * **URL** : 게시글 URL으로 매핑
   * **title** : 게시글 제목으로 매핑
   * **issue number** : 이슈 번호로 매핑
   * **title contains specific term** : 제목 포함 단어로 매핑

3. 테마 선택 후, **코드를 복사**합니다.  
  ![image](https://user-images.githubusercontent.com/39720852/156585223-687f0a59-94df-4ba7-b091-6828f3906f50.png)

#### 🥨 utterance 적용

지난 글에서 footer를 추가했던 것처럼 **_includes/body 폴더에 comments.html 파일을 추가**하고

기존의 댓글 표시 부분을 주석 처리한 후, **복사한 코드를 붙여넣기** 합니다.

![image](https://user-images.githubusercontent.com/39720852/156586316-dea6bfeb-3a56-4710-952c-c4630a4c21c4.png)

#### 🥨 댓글 표시

게시글에 댓글을 표시하는 방법은 2가지가 있습니다.

1. **해당 게시글 활성화**  
  ![image](https://user-images.githubusercontent.com/39720852/156597921-13d6e4c3-33de-4298-b612-93961aed79aa.png)

2. **전체 게시글 활성화**  
  _config.yml 파일의 comments scope 부분 주석 해제  
  (scope로 인해 게시글 전체에 자동으로 댓글이 활성화됩니다.)
  ![image](https://user-images.githubusercontent.com/39720852/156596998-8ad751f3-d70f-494c-878b-0b179156e568.png)

---

자! 이렇게 해서 Github 블로그 댓글 기능을 추가해 봤습니다.

댓글을 통해 방문자분들과 소통할 생각에 기대되지 않나요😝

다음 글에서는 <span style="background-color:#f1f8ff">**구글 애널리틱스 기능**</span>에 대해서 소개해 드리도록 하겠습니다.
<br/><br/><br/>
**오류 및 오타 지적, 질문, 인사** 등 무엇이든 언제나 환영입니다!

읽어주셔서 감사합니다.

끝!🦕
<br/><br/><br/>
🔗 다음 글 바로가기 [GitHub 블로그 만들기 (7) - 구글 애널리틱스 기능](/blog/git-github/2022-02-10-github_blog(7))

## 👍 참고

* [[GithubPages] 하루만에 만드는 깃허브 블로그-07.댓글기능 추가하기](https://khw11044.github.io/blog/githubpages/2020-12-26-making-blog-07/)
* [[Github 블로그] utterances 으로 댓글 기능 만들기 (+ disqus 비추후기)](https://ansohxxn.github.io/blog/utterances/)
* [블로그에 깃허브 댓글 적용하기(utterances)](https://joyykim.tistory.com/9)
