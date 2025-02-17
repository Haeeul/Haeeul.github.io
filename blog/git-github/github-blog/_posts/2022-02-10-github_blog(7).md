---
#008
layout: post
title: "GitHub 블로그 만들기 (7) - 구글 애널리틱스 기능"
image: https://user-images.githubusercontent.com/39720852/156726769-93d906b4-f7f7-431c-96a8-2dfd6f455a29.png
accent_image:
  background: url(https://user-images.githubusercontent.com/39720852/152405232-29b296d1-653c-4505-ad3c-07fd5a680d17.png) center/cover
  overlay: true
date: 2022-02-10 18:52:00 +0900
categories: git-github
tags: [GitHub Pages, GitHub blog, Jekyll, Jekyll theme, analytics]
description: >
  📝 GitHub 블로그에 구글 애널리틱스 기능을 추가합니다.
related_posts:
  - /blog/git-github/2022-02-08-github_blog(5)/
  - /blog/git-github/2022-02-09-github_blog(6)/
  - /blog/git-github/2022-03-20-github_blog(8)/
---

안녕하세요, 해을입니다🦖

이번 글에서는 <span style="background-color:#f1f8ff">**구글 애널리틱스 기능**</span>에 대해 알아보겠습니다!

* toc
{:toc}

## 💡구글 애널리틱스

![image](https://user-images.githubusercontent.com/39720852/156784769-cf54968e-6ff2-4c74-96ef-236fd324abcd.png){: width="500"}

구글 애널리틱스는 **웹 사이트의 트래픽을 추적하는 구글 서비스**입니다.

Jekyll에는 별도의 방문자 기록 시스템이 없기 때문에 구글 애널리틱스를 사용하여 방문 기록을 확인합니다.

구글 애널리틱스는 언제, 어디서, 누가, 어떤 페이지에 방문했는지 등 무척 자세하게 방문 기록을 확인할 수 있습니다.

이를 통해 자신의 블로그에 주 방문자는 어떤 계층인지, 어떤 게시글이 인기가 많은지 등 분석할 수 있겠죠?

계정을 만든 후, ID 입력만 하면 되기 때문에 설정도 굉장히 간편합니다.

## 💡추적 ID? 측정 ID?

구글 애널리틱스를 설정하기 위해서는 ID를 입력해야 하는데, ID의 종류는 2가지입니다.

1. **추적 ID : 'UA-'로 시작**
2. **측정 ID : 'G-'로 시작**

사용 테마 doc의 예시를 보고 어떤 ID를 사용해야 하는지 확인해 주세요.

올바른 ID를 사용하지 않으면 애널리틱스가 동작하지 않습니다.

Hydejack의 경우, UA로 시작하므로 **추적 ID**를 사용해야 합니다.

![image](https://user-images.githubusercontent.com/39720852/156769777-49756925-7680-4e79-b5cf-1ed77ec33193.png)

## 💡기능 추가하기

### 🥨 계정 만들기

구글 애널리틱스 [사이트](https://analytics.google.com/)에 접속한 후,

사이드바 가장 아래에 있는 **관리 탭의 계정 만들기**로 들어갑니다.

![image](https://user-images.githubusercontent.com/39720852/156733623-12f26cc4-ce9f-479c-bdfb-991c3e5f484c.png){: width="350"}

### 🥨 계정 설정

필수 정보인 **계정 이름**을 입력합니다.

![image](https://user-images.githubusercontent.com/39720852/156778266-f2ff523d-286e-48f1-a7c2-48e70b3e6f82.png)

### 🥨 속성 설정

**속성 이름**을 입력하고 **시간대와 통화**를 한국 기준으로 변경합니다.

속성 이름은 아무 값이나 상관없으며, 저는 블로그 이름으로 설정했습니다.

![image](https://user-images.githubusercontent.com/39720852/156778821-1a32f28c-d1bd-41ce-99ef-201233a9b576.png)

🌟 **유니버셜 애널리틱스 속성 만들기**  
(<span style="background-color:#ffdce0">**추적 ID('UA ~~')가 필요하신 분들만 진행**</span>/ 측정 ID가 필요하신 분들은 넘어가시면 됩니다.)

**고급 옵션 보기-유니버설 애널리틱스 속성 만들기**를 선택하고

깃헙 블로그 주소를 입력한 후, 꼭!!!! **유니버설 애널리틱스 속성만 만들기**를 체크해 주세요.

![image](https://user-images.githubusercontent.com/39720852/156799042-9b89ca26-9aa8-4978-a1a7-95087ee2d681.png)

### 🥨 비즈니스 정보 설정

카테고리, 규모, 사용 계획을 자유롭게 선택한 후, 약관에 동의합니다.

![image](https://user-images.githubusercontent.com/39720852/156781622-0d2a4eab-960c-4a8b-807f-4f64571b05b7.png){: width="450"}

![image](https://user-images.githubusercontent.com/39720852/156781949-bcca8ee9-cc3e-4ebf-8cac-7fb6c508b7e9.png){: width="350"}

### 🥨 (선택) 측정 ID('G ~~') 발급

**측정 ID**가 필요해서 그냥 넘어오신 분들은 아래의 추가 설정을 진행해 주세요.

<details> 
<summary>측정 ID('G ~~') 추가 설정</summary>
<div markdown="1">

1. **웹** 플랫폼의 **데이터 스트림을 설정**합니다.
  ![image](https://user-images.githubusercontent.com/39720852/156800419-f4a6da38-a380-4e6c-a73a-ba4ebcff7973.png)

2. 깃헙 블로그 **주소**와 **스트림 이름**을 입력합니다.
  ![image](https://user-images.githubusercontent.com/39720852/156798169-e72a1562-4e06-476c-89c5-ce685fde737a.png)

3. 발급된 **측정 ID('G ~~')를 복사**합니다.
  ![image](https://user-images.githubusercontent.com/39720852/156800493-c320a595-f960-4085-bec7-598e47400c70.png)

</div>
</details>

### 🥨 추적 ID 확인

발급된 **추적 ID('UA ~~')를 복사**합니다.

![image](https://user-images.githubusercontent.com/39720852/156800374-22d83cf8-c5dd-4121-9313-49bd2ce7bd88.png)

### 🥨 _config.yml 설정

복사한 ID를 **_config.yml** 파일 **google_analytics**에 붙여넣기 합니다.

![image](https://user-images.githubusercontent.com/39720852/156786531-cf52ecfd-4876-49e9-bab7-d0c52dac3edf.png)

### 🥨 대시보드 확인

**commit/push를 통해 저장소에 업로드**한 후, 블로그에 접속합니다.

블로그 창을 띄운 채로 구글 애널리틱스 홈을 살펴보면 실시간으로 활성 사용자를 확인할 수 있습니다.

(저는 미리 설정해둬서 방문 기록도 찍혀있네요ㅎㅎ)

![image](https://user-images.githubusercontent.com/39720852/156783825-5fafd33d-b015-4da1-ab87-097eb2ef9217.png)

---

.

자! 이렇게 해서 Github 블로그에 구글 애널리틱스 기능을 추가해 봤습니다.

어떤 분들이 블로그에 방문해 주실지 무척 기대되지 않나요😝

다음 글에서는 구글에서 블로그를 검색할 수 있도록 하는 <span style="background-color:#f1f8ff">**구글 서치 콘솔**</span>에 대해서 소개해 드리도록 하겠습니다.

.

🔗 다음 글 바로가기 [GitHub 블로그 만들기 (8) - 구글 서치 콘솔](/blog/git-github/github-blog/2022-03-20-github_blog(8))

.

**오류 및 오타 지적, 질문, 인사** 등 무엇이든 언제나 환영입니다!

읽어주셔서 감사합니다.

끝!🦕

.

---

**👍 참고**

* [[GithubPages] 하루만에 만드는 깃허브 블로그-08.조회수 나타내기](https://khw11044.github.io/blog/githubpages/2020-12-26-making-blog-08/)
* [티스토리 구글 애널리틱스 연결(추적ID와 측정ID)](https://pujin28.tistory.com/entry/%ED%8B%B0%EC%8A%A4%ED%86%A0%EB%A6%AC-%EA%B5%AC%EA%B8%80-%EC%95%A0%EB%84%90%EB%A6%AC%ED%8B%B1%EC%8A%A4-%EC%97%B0%EA%B2%B0-%EC%B6%94%EC%A0%81-ID%EC%99%80-%EC%B8%A1%EC%A0%95-ID)
* [애널리틱스 도움말](https://support.google.com/analytics/answer/10269537?hl=ko)
