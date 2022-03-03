---
#005
layout: post
title: "GitHub 블로그 만들기 (4) - 블로그 커스텀"
image: https://user-images.githubusercontent.com/39720852/153696866-881754a0-09ad-4d78-921f-4f4dde3574ea.png
accent_image:
  background: url(https://user-images.githubusercontent.com/39720852/152405232-29b296d1-653c-4505-ad3c-07fd5a680d17.png) center/cover
  overlay: true
date: 2022-02-07 12:35:00 +0900
categories: git-github
tags: [GitHub Pages, GitHub blog, Jekyll, Jekyll theme]
description: >
  🖼️ GitHub 블로그를 커스터마이징합니다.
related_posts:
  - /blog/git-github/2022-02-05-github_blog(2)/
  - /blog/git-github/2022-02-06-github_blog(3)/
  - /blog/git-github/2022-02-08-github_blog(5)/
---

안녕하세요, 해을입니다🦖

이번 글에서는 <span style="background-color:#f1f8ff">**블로그 커스텀**</span>에 대해 알아보겠습니다!

* toc
{:toc}

## 💡시작하기 전에

편집기는 1편에서 말씀드렸던 <span style="background-color:#fff5b1">**Visual Studio Code**</span>를 사용하겠습니다.

커스텀 과정은 로컬 서버를 통해 확인하는데, 로컬 서버는 파일이 수정(및 저장)되면 바로 업데이트됩니다.

하지만 최상단 루트에 있는 _config.yml을 수정할 경우에는 수동으로 로컬 서버를 재시작해야 한다는 사실을 기억해 주세요.

커스텀을 진행하면서 다시 설명드리도록 하겠습니다.

## 💡블로그 커스텀

커스텀은 지난 글에서 적용한 **Hydejack 테마**를 기준으로 진행하겠습니다.

다른 테마는 물론이고 저와 같은 Hydejack 테마를 적용하셨더라도 업데이트되면서 폴더 구조가 조금 다를 수 있습니다.

하지만 Jekyll 테마 구조는 대부분 유사하기 때문에 이번 게시글과 본인의 사용 테마 doc를 함께 참고하면 큰 어려움 없이 진행하실 수 있을겁니다.

### 1. authors.yml : 저자 정보 설정

가장 먼저 블로그 저자 정보를 설정하겠습니다.

저자 정보는 게시글 하단에 위치한 **about**에 보이게 됩니다.

![GitHub블로그4-저자예시](https://user-images.githubusercontent.com/39720852/155050780-f8847cf5-0fdf-4751-a12d-0567b08c409e.png)

저자 정보가 담긴 about
{:.figcaption}

#### 🥨 기본 정보 설정

**_data 폴더**에 있는 **authors.yml 파일**의 내용을 아래와 같이 본인의 정보로 수정합니다.

<> 표시 안에 입력하는 것이 아닌 값만 작성하셔야 합니다.

![image](https://user-images.githubusercontent.com/39720852/155072794-60cc5ae1-bc05-4cb0-904e-ef514e5051d3.png)

* **name** : 이름
* **email** : 이메일
* **about** : 설명 (about에 노출)

#### 🥨 프로필 사진 설정

**assets/img 폴더**에 프로필로 사용할 사진을 추가하고 경로를 수정합니다.

![image](https://user-images.githubusercontent.com/39720852/155455588-4398dfc8-632e-470a-a415-c2841002dcd2.png)

#### 🥨 소셜 미디어 계정 연결

다양한 소셜 미디어 계정을 연결할 수도 있으며, 이는 about뿐만 아니라 사이드 바에도 표시됩니다.

주석을 해제하고 본인의 계정을 적으면 위부터 순서대로 보이게 됩니다.(순서 변경 가능)

저는 깃헙, 이메일, 인스타그램 순서로 3가지를 연결했습니다.

![image](https://user-images.githubusercontent.com/39720852/155458773-556a4de7-fd45-4895-bde6-f71c847e997c.png)

#### 🥨 (선택) 저자 추가하기

여러 명이 관리하는 공동 블로그의 경우, 위 양식을 사용하여 저자를 추가할 수 있습니다.

![image](https://user-images.githubusercontent.com/39720852/155162060-184eb4e3-d443-430f-8605-b89ff68b7bd8.png)

#### 🥨 about 확인

변경사항은 로컬 서버를 재시작하여 확인 가능하며, **로컬 서버는 파일이 수정되면 바로 업데이트** 됩니다.

authors.yml 파일을 저장한 후, 로컬 서버가 업데이트되면 아무 게시글이나 들어가서 하단의 about을 확인합니다.

![image](https://user-images.githubusercontent.com/39720852/155167020-74b0c00d-6fb7-468a-b452-666d0b1258bc.png)

### 2. about.md : 소개 페이지

사이드 바 기본 메뉴로 제공되는 **about은 소개 페이지**입니다.

authors.yml에서 설정한 기본 정보와는 다르게 좀 더 구체적이고 자유롭게 자신을 소개할 수 있습니다.

![image](https://user-images.githubusercontent.com/39720852/155167512-66951c86-7f96-4419-8236-2cee8f50128c.png){: width="450"}

about 페이지 예시
{:.figcaption}

#### 🥨 소개 페이지 작성

about 페이지는 정해진 형식이 없기 때문에 마크다운 문법에 맞춰 자유롭게 작성하면 됩니다.

![image](https://user-images.githubusercontent.com/39720852/155173263-0595b2af-292e-4dad-9767-c92a09f1ae46.png)

### 3. favicon.ico : 웹 브라우저 아이콘 설정

Favicon은 아래와 같이 **웹 브라우저 주소창에 표시되는 아이콘**을 말합니다.

![image](https://user-images.githubusercontent.com/39720852/155463054-7d79e6f2-2ce6-4947-a312-da3969171b17.png)

#### 🥨 Favicon 변경

① [Favicon 제작 사이트](https://www.favicon-generator.org/)에서 favicon을 만든 후, 다운로드합니다.

![image](https://user-images.githubusercontent.com/39720852/155465009-3940aaae-8a8c-46e9-a79e-c59e211bdae8.png)

② **assets/icons에 있는 favicon**을 다운로드한 것으로 바꿔줍니다.

![image](https://user-images.githubusercontent.com/39720852/155465277-edac2d98-a437-46db-9072-75fac86923a2.png)

### 4. _config.yml : 페이지 구성 및 환경 변수 설정

페이지 구성과 환경 변수를 다루는 **_config.yml 파일**의 내용을 차례대로 수정해 보겠습니다.

#### 🥨 url 설정

가장 먼저 url을 본인의 블로그 주소로 수정합니다.

![image](https://user-images.githubusercontent.com/39720852/155473319-d6332ea2-9f79-4633-9f92-f1ca1240e3ad.png)

* **url** : GitHub 블로그 주소(https://username.github.io)

#### 🥨 블로그 정보 설정

자신의 블로그 정보를 입력합니다.

![image](https://user-images.githubusercontent.com/39720852/155475305-a4dbf467-73b3-42fd-8fe2-f0bea5d05806.png)

* **title** : 블로그 제목(사이드바 및 브라우저 탭 노출)
* **description** : 블로그 설명
* **tagline** : 짧은 블로그 설명(사이드바 노출)
* **keywords** : 블로그 키워드

#### 🥨 logo 설정

**assets/img 폴더**에 사이드 바에서 보일 로고나 프로필 사진을 추가하고 경로를 수정합니다.

![image](https://user-images.githubusercontent.com/39720852/155476076-0d5e40bd-25d5-4508-822a-0d914548d080.png)

#### 🥨 저자 설정

**authors.yml**에서 설정했던 이름, 이메일과 동일하게 변경합니다.

![image](https://user-images.githubusercontent.com/39720852/155475817-c330fe9d-cd82-43cf-8baf-8d73141327ac.png)

#### 🥨 메뉴 설정

① 사이드 바에 보이는 블로그 메뉴를 생각하고 title과 url을 적어주세요.

저는 많은 분들이 주로 사용하시는 about(소개 페이지), projects, blog, etc 4가지 항목으로 설정했습니다.

![image](https://user-images.githubusercontent.com/39720852/155845722-db71743a-c100-423f-bd3f-9cb9e64a4aef.png)

* **title** : 메뉴명
* **url** : 메뉴 경로

② url과 일치하도록 최상단 루트에 각각의 메뉴 폴더를 생성합니다.

이때, **about 폴더는 만들지 않습니다.**(이미 만들어져 있는 about.md 파일과 연결되기 때문)

![image](https://user-images.githubusercontent.com/39720852/155515463-8e404dba-729c-439b-958b-11008a7f0a27.png)

#### 🥨 footer 설정

블로그 맨 하단에 위치한 footer에 포함되는 링크와 copyright를 설정합니다.

링크는 주석 처리할 경우, 노출되지 않습니다.

![image](https://user-images.githubusercontent.com/39720852/155518049-b94a3f65-2fe2-42b6-a2e6-e05ca27e95a9.png)

#### 🥨 사이드바 배경 설정

사이드바에 적용할 배경 이미지를 **assets/img 폴더**에 추가하고 경로를 수정합니다.

무료 이미지 찾으신다면 [unsplash](https://unsplash.com/) 사이트 추천드립니다.

![image](https://user-images.githubusercontent.com/39720852/155845968-0fc47401-2a58-4299-a266-01bbb13afe83.png)

*폰트도 변경 가능하나 ~~귀찮은 관계로~~ 패스하겠습니다^^,, 원하시는 분들은 테마 doc를 참고해 주세요,,*

#### 🥨 사이드바 및 footer 확인

**_config.yml 파일은 저장해도 자동으로 로컬 서버가 업데이트되지 않습니다.**

_config.yml 파일 저장 및 로컬 서버 종료(ctrl+c) 후, 재시작 한 뒤에 변경 사항을 확인해 주세요.

참고로 사이드 바 메뉴 클릭 시, 아직 파일을 생성하지 않아 404 에러가 납니다.

![image](https://user-images.githubusercontent.com/39720852/155523344-51310bc6-ec5d-41e1-a1bd-a32ac371d488.png)

### 5. _includes : 레이아웃 재정의

_includes에서는 레이아웃 파일을 관리합니다.

레이아웃 파일이 이미 있다면 그 파일을 수정하면 되고, 없다면 파일을 복사해와야 합니다.

<details> 
<summary>레이아웃 파일 찾는 방법 펼치기</summary>
<div markdown="1">

1. 위치 따라가기  
    vendor/bundle/ruby/3.0.0  
    /gems  
    /jekyll-theme-hydejack-9.1.5  
    /includes  
    /body

    ![2022-02-25 00;23;39](https://user-images.githubusercontent.com/39720852/155553893-8fd2eb34-761c-4c0b-af59-cc91a5ea1d28.gif)

2. .gitignore에서 vendor 주석 처리 및 저장 후, 키워드 검색하기

    ![2022-02-25 00;34;43](https://user-images.githubusercontent.com/39720852/155555874-7c11169e-c6eb-4dce-9c4b-4f2edd927492.gif)

    * .gitignore 수정 및 저장 후, vendor 폴더의 색이 뚜렷해져야 검색이 가능합니다.
    * footer, 9.1.5 등 키워드 검색 후, vendor~~로 시작하는 폴더의 footer 파일을 찾아주세요.
    * 파일을 찾은 후에는 .gitignore에서 **vendor 주석을 풀고 저장**해주세요.

</div>
</details>

#### 🥨 footer 커스텀

**_includes에 body 폴더**를 만든 후, footer.html 파일을 복사/붙여넣기 합니다.

Powered by ~~ 부분을 html 형식대로 자유롭게 수정하시면 됩니다.

저는 테마를 궁금해하시는 분들이 계실까 봐 버전 내용을 지우지 않고 블로그 명만 추가했습니다.

![image](https://user-images.githubusercontent.com/39720852/155558619-08fdfc7b-88f5-49b5-83cd-cc06daa8319c.png)

![image](https://user-images.githubusercontent.com/39720852/155559817-81c59d0e-2aea-4291-ba9f-1dd0919980d1.png){: width="350"}

### 6. _featured_categories : 카테고리 설정

메뉴 레이아웃은 2가지 종류가 있으며, 종류에 따라 파일 구성이 달라집니다.

* **리스트 레이아웃** : 게시글 리스트 형식
* **페이지 레이아웃** : 사용자 지정 형식

![image](https://user-images.githubusercontent.com/39720852/155870072-d9885f37-3deb-4524-8db6-aa4553c78f27.png){: width:="500"}

#### 🥨 리스트 레이아웃 설정

리스트 레이아웃은 연도별 게시글 리스트를 보여주는 형식으로, 세부 카테고리 없이 메뉴 자체가 하나의 카테고리 있는 것입니다.

세부 카테고리가 필요 없는 etc 메뉴에 리스트 레이아웃을 적용해 보겠습니다.

etc 카테고리를 추가하기 위해 **_featured_categories 폴더**에 있는 example.md의 파일명과 내용을 수정합니다.

![image](https://user-images.githubusercontent.com/39720852/155886006-7ae83e7d-114d-4134-87e1-ed2a75c48ed0.png)

* **title** : 페이지 제목
* **slug** : 게시글에 포함되는 경로 태그명
* **description** : 페이지 설명
* **permalink** : 페이지 경로(_config.yml의 메뉴 url과 동일하게 설정)

#### 🥨 페이지 레이아웃 설정

페이지 레이아웃은 사용자가 정의한 대로 보여주는 형식으로, 세부 카테고리가 있는 메뉴에 적합한 레이아웃입니다.

다양한 주제를 다루게 될 blog 메뉴에 세부 카테고리를 추가해 보겠습니다.

① blog 메뉴에서 사용할 카테고리를 **_featured_categories 폴더**에 추가합니다.

![image](https://user-images.githubusercontent.com/39720852/155974267-ed67b080-8e8b-4a03-b829-a763083b7e27.png)

② blog 폴더에 각각의 카테고리 폴더를 생성합니다.

③ docs 폴더에서 README.md를 복사해온 뒤, 마크다운 문법에 맞춰 내용을 수정합니다.

![image](https://user-images.githubusercontent.com/39720852/155977450-27583f95-3c2a-4c1e-ab77-fd991c661b70.png)

#### 🥨 메뉴 및 카테고리 확인하기

수정한 파일들을 저장 후, 메뉴 레이아웃 적용과 카테고리 추가, 이동이 잘 동작하는지 확인합니다.

![2022-02-28 21;10;36](https://user-images.githubusercontent.com/39720852/155981358-653bfe72-b98f-4025-bbcb-8f61e3182bda.gif)

### 7. _posts : 게시글 작성

아래의 example 폴더와 같이 블로그 게시글은 _posts 폴더에서 작성합니다.

![image](https://user-images.githubusercontent.com/39720852/155982012-83514307-4b2f-4927-a22e-18c7e6a235a5.png)

#### 🥨 _posts 폴더 추가

카테고리 폴더마다 **_posts 폴더**를 생성합니다.

참고로 폴더 안에 게시글이 없는 경우, 블로그 게시글 전체 리스트가 나타납니다.

게시글 작성은 다음 글에서 자세히 소개해 드리도록 하겠습니다.

![image](https://user-images.githubusercontent.com/39720852/155986654-dbc6be8b-1aba-4abd-9344-e319db21f10c.png)

---

자! 이렇게 해서 Github 블로그 테마를 커스텀 해봤습니다.

자신만의 개성 있는 블로그로 변한 모습이 설레지 않나요😝

다음 글에서는 <span style="background-color:#f1f8ff">**블로그 게시글 작성**</span>에 대해서 소개해 드리도록 하겠습니다.
<br/><br/><br/>
**오류 및 오타 지적, 질문, 인사** 등 무엇이든 언제나 환영입니다!

읽어주셔서 감사합니다.

끝!🦕
<br/><br/><br/>
🔗 다음 글 바로가기 [GitHub 블로그 만들기 (5) - 블로그 게시글 작성](/blog/git-github/2022-02-08-github_blog(5))

## 👍 참고

* [[GithubPages] 하루만에 만드는 깃허브 블로그-03.커스텀하기](https://khw11044.github.io/blog/githubpages/2020-12-26-making-blog-03/)
