---
#013
layout: post
title: "GitHub 블로그 만들기 (8) - 구글 서치 콘솔"
image: https://user-images.githubusercontent.com/39720852/159161021-90badc15-3023-47b5-9f83-38b1b4324eed.png
accent_image:
  background: url(https://user-images.githubusercontent.com/39720852/152405232-29b296d1-653c-4505-ad3c-07fd5a680d17.png) center/cover
  overlay: true
date: 2022-03-20 20:43:00 +0900
categories: git-github
tags: [GitHub Pages, GitHub blog, Jekyll, Jekyll theme, Google, search console]
description: >
  📝 구글에 GitHub 블로그가 검색되도록 합니다.
related_posts:
  - /blog/git-github/2022-02-08-github_blog(5)/
  - /blog/git-github/2022-02-09-github_blog(6)/
  - /blog/git-github/2022-02-10-github_blog(7)/
---

안녕하세요, 해을입니다🦖

이번 글에서는 <span style="background-color:#f1f8ff">**구글 서치 콘솔**</span>에 대해 알아보겠습니다!

* toc
{:toc}

## 💡Google Search Console

구글 서치 콘솔은 **구글 검색 시, 등록한 사이트가 노출되도록 해주는 구글 서비스**입니다.

열심히 작성한 게시글을 다른 사람들과 공유하면 더욱 좋겠죠?

바로 시작하겠습니다.

## 💡블로그 등록하기

### 🥨 사이트 접속

구글 서치 콘솔 [사이트](https://search.google.com/search-console/about)에 접속한 후, **시작하기**로 들어갑니다.

![image](https://user-images.githubusercontent.com/39720852/159161957-58b44d85-2460-4c3c-bc1a-bfd114493dae.png)

### 🥨 속성 유형 선택

**URL 접두어에 블로그 주소**를 적고 계속 버튼을 클릭하면 URL 유효성 확인 후, 소유권 확인으로 넘어갑니다.

![image](https://user-images.githubusercontent.com/39720852/159161969-51f4fa5d-c6a2-4ca0-ad39-b202f6787d26.png)

### 🥨 소유권 확인 - Google HTML

소유권 확인에는 다양한 방법이 있으나 **HTML 파일을 사용**하는 방식이

가장 간편하고 보편적인 방법이라고 하니 해당 방식으로 진행하겠습니다.

1. **HTML 파일을 다운로드** 받습니다.  
  (확인 버튼은 저장소 업로드 후에 클릭할 예정이니 창을 유지해 주세요)  
  ![image](https://user-images.githubusercontent.com/39720852/159161755-7f4a223a-1bf4-4c8c-977f-f2e2023fc964.png){: width="500"}

2. 다운로드한 파일을 **_config.xml가 있는 Root 위치**에 넣어줍니다.  
  ![image](https://user-images.githubusercontent.com/39720852/159162105-b3f9595a-ce8c-40c1-9de8-acf226245d2a.png)

### 🥨 크롤링 노출시키기 - sitemap.xml

이번에는 크롤링(검색) 되도록 하는 파일을 추가하겠습니다.

[sitemap.xml](https://github.com/Haeeul/Haeeul.github.io/blob/main/sitemap.xml) 코드를 조금 전 **HTML 파일을 추가한 Root 위치**에 추가합니다.

![image](https://user-images.githubusercontent.com/39720852/159162571-d8423c8e-4d00-486d-a2d3-fdab2c02d0ad.png)

### 🥨 반영하기 - commit, push

commit, push를 통해 저장소에 업로드한 뒤에

열어뒀던 Google search console 소유권 확인 창에서 확인 버튼을 클릭합니다.

![image](https://user-images.githubusercontent.com/39720852/159163499-ff661749-cfce-4aff-8637-eb80a94e7661.png)

![image](https://user-images.githubusercontent.com/39720852/159212480-81150d1b-b8bd-46dd-b776-6d065ca85860.png){: width="500"}

### 🥨 sitemap.xml 등록

소유권 확인이 끝나면 sitemaps 탭에서 자신의 **sitemap.xml을 등록**합니다.

상태가 성공으로 처리되기까지는 보통 3~5일 정도 걸린다고 합니다.

![image](https://user-images.githubusercontent.com/39720852/159208859-6ffe03b4-f485-4eb9-a279-b1eb5f11fe46.png)

### 🥨 등록 확인

3~5일 후에 다시 확인해 봤지만 여전히 '가져올 수 없음' 상태였습니다.

답답한 마음에 구글링 해보니 여러 해결 방안이 있었고 2주간 모든 방법을 시도해 봤지만 계속 같은 상태..

그렇게 포기하고 방치해둔 결과, '성공' 처리되었습니다!(성질 급한 한국인이 문제였네요🤣)

**3~5일 이상 여유 있게 기다리시는 것을 추천**드립니다.

![image](https://user-images.githubusercontent.com/39720852/182631459-245c2bb3-fbca-49cd-9f6f-97d802daf2e7.png)

---

.

자! 이렇게 해서 구글에 Github 블로그가 검색되도록 해봤습니다.

구글에서 내 블로그를 검색할 수 있다니 설레지 않나요😝

다음 글에서는 새로운 기능을 추가하게 되면 소개해 드리도록 하겠습니다.

.

🔗 다음 글 바로가기 [GitHub 블로그 만들기 (9) - build error](/blog/git-github/github-blog/2022-09-14-github_blog(9))

.

**오류 및 오타 지적, 질문, 인사** 등 무엇이든 언제나 환영입니다!

읽어주셔서 감사합니다.

끝!🦕

.

---

**👍 참고**

* [[Github Blog] 검색창 노출시키기](https://velog.io/@eona1301/Github-Blog-%EA%B2%80%EC%83%89%EC%B0%BD-%EB%85%B8%EC%B6%9C%EC%8B%9C%ED%82%A4%EA%B8%B0)
* [깃허브 블로그 구글 검색 가능하게 하기](https://ip99202.github.io/posts/%EA%B9%83%ED%97%88%EB%B8%8C-%EB%B8%94%EB%A1%9C%EA%B7%B8-%EA%B5%AC%EA%B8%80-%EA%B2%80%EC%83%89-%EA%B0%80%EB%8A%A5%ED%95%98%EA%B2%8C-%ED%95%98%EA%B8%B0/)
