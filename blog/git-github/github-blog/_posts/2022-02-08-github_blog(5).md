---
#006
layout: post
title: "GitHub 블로그 만들기 (5) - 블로그 게시글 작성"
image: https://user-images.githubusercontent.com/39720852/156108961-1fdae226-7431-4c61-a0e7-e14b004ecf4c.png
accent_image:
  background: url(https://user-images.githubusercontent.com/39720852/152405232-29b296d1-653c-4505-ad3c-07fd5a680d17.png) center/cover
  overlay: true
date: 2022-02-08 22:04:00 +0900
categories: git-github
tags: [GitHub Pages, GitHub blog, Jekyll, Jekyll theme]
description: >
  📝 GitHub 블로그에 게시글을 작성합니다.
related_posts:
  - /blog/git-github/2022-02-06-github_blog(3)/
  - /blog/git-github/2022-02-07-github_blog(4)/
  - /blog/git-github/2022-02-09-github_blog(6)/
---

안녕하세요, 해을입니다🦖

이번 글에서는 <span style="background-color:#f1f8ff">**블로그 게시글 작성**</span>에 대해 알아보겠습니다!

* toc
{:toc}

## 💡블로그 게시글

커스텀을 통해 블로그 단장을 마쳤으니 이제는 글로 채워나갈 준비를 해야겠죠?

그럼 지금부터 지난 글에서 만들었던 _posts 폴더 내에 게시글을 작성해 보겠습니다.

### 1. 게시글 파일 생성

블로그 게시글은 아래와 같이 **마크다운 파일로 작성**합니다.

![image](https://user-images.githubusercontent.com/39720852/156111393-7e72d608-c325-43cf-9ee0-d513e815ed43.png)

#### 🥨 .md 파일 생성

**year-month-day-title** 제목으로 마크다운 파일을 생성합니다.

![image](https://user-images.githubusercontent.com/39720852/156114610-8765c145-9679-4705-a001-7f71e6f57e0d.png)

#### 🥨 파일 기본 설정

아래와 같이 기본 설정 내용을 입력합니다.

![image](https://user-images.githubusercontent.com/39720852/156115726-73aec570-ac5f-4c6b-8b3e-4b7ac33dd5e0.png)

* **title** : 게시글 제목
* **date** : 작성 날짜 및 시간(현재 시간보다 이후의 시간을 적는 경우, 게시글이 나타나지 않습니다)
* **categories** : 게시글 카테고리(자동 링크 연결)

#### 🥨 파일 추가 설정

설명과 태그도 추가 가능합니다.

![image](https://user-images.githubusercontent.com/39720852/156116211-f5d511e5-e8cc-4292-9ada-ce0c6370d337.png)

* **tags** : 게시글 태그
* **description** : 게시글 설명

#### 🥨 썸네일 설정

**image 키**를 통해 썸네일을 추가할 수 있습니다.

![image](https://user-images.githubusercontent.com/39720852/156117264-6922b0b6-479d-4576-8be3-aace3cdc6c91.png)

📢 **(참고) 이미지, Gif의 url을 쉽게 따는 방법**

GitHub의 issue를 활용하는 방법이 있습니다.

자신의 아무 Repository의 issue 생성 페이지로 들어가서 원하는 파일을 붙여넣기 하시면 됩니다.

![2022-03-01 15;50;11](https://user-images.githubusercontent.com/39720852/156119340-41b54f35-a8fd-4896-8fd9-3fdbd01d6d17.gif)

#### 🥨 사이드 바 강조

**accent_image 키**를 통해 게시글에서 사이드 바 이미지를 일시적으로 변경할 수 있습니다.

overlay 효과도 사용 가능합니다.

![image](https://user-images.githubusercontent.com/39720852/156118722-33e3773c-9047-46af-8b40-5e7058cb5d7b.png)

### 2. 내용 추가

hydejack 테마에서 제공하는 클래스나 마크다운 문법을 활용하여 내용을 작성합니다.

#### 🥨 메모 추가

**note 클래스**를 활용하여 메모를 추가할 수 있습니다.

```
// 노트 추가
You can add a note.
{:.note}

// 노트 타이틀 설정
A custom label.
{:.note title="Attention"}
```

![image](https://user-images.githubusercontent.com/39720852/156123087-347e3e98-5953-4c3e-aef2-56287569a4b3.png)

#### 🥨 이미지 및 캡션 추가

이미지를 추가하고 해당 이미지에 캡션을 달 수 있습니다.

이때 캡션은 이미지가 아닌 전체 너비를 기준으로 가운데인 곳에 추가됩니다.

```
// 원본 사이즈로 추가
![image](이미지 url 입력)

// 사이즈 지정
![image](이미지 url 입력){: width="너비" height="높이"}

// 캡션 추가
캡션 내용 입력
{:.figcaption}
```

![image](https://user-images.githubusercontent.com/39720852/156124818-5a80fde6-119a-4d0f-96dc-149d613e3986.png){: width="500"}

![image](https://user-images.githubusercontent.com/39720852/156124868-d0738e83-e360-400d-8365-088d0dbf151e.png)

#### 🥨 글자 색상 변경 및 하이라이트 설정

html 문법을 사용하여 글자의 색 또는 배경색을 변경할 수 있습니다.

색상은 color name 또는 16진수로 입력합니다.

```
// 글자 색 변경
<span style="color:red"> 빨간 글씨 </span> 

// 하이라이트 처리
<span style="background-color:#fff5b1">노랑색 형광펜</span> 
```

![image](https://user-images.githubusercontent.com/39720852/156126179-15cbe89a-93c9-494e-bfa7-5c2af049181c.png)

마크다운 파일에서 html 문법을 사용할 경우, 사진과 같이 노란 줄로 경고 표시가 뜨게 됩니다.
{:.note}

#### 🥨 링크 설정

외부 링크와 내부 문서 링크를 연결할 수 있습니다.

```
// 외부 링크 설정
[표시 내용](링크 url)

// 내부 링크 설정
[표시 내용](문서 경로)
```

![image](https://user-images.githubusercontent.com/39720852/156127504-f78a60ca-cad5-42a6-945e-b80b749f3891.png)

#### 🥨 그 외

이 외에도 hydejack 테마와 마크다운 문법에는 다양한 표현 방법이 있습니다.

(ex - 테이블, 인용문, 글자 효과 등)

[테마 공식 문서](https://hydejack.com/docs/writing/#adding-large-quotes)와 마크다운 문법을 살펴본 후, 필요에 따라 적용하시길 바랍니다.

### 4. 목차 추가

목차 기능은 PRO에서만 제공하는 기능이지만 표시는 가능합니다.

게시글 시작 위치에 아래 내용을 입력해 주세요.

```
* toc
{:toc}
```

![image](https://user-images.githubusercontent.com/39720852/156128399-20ad130a-f54f-4035-af72-b99b2c392f28.png)

### 5. 관련 게시물 추가

파일 설정에 **related_posts 키**를 추가하여 관련 게시물을 추가할 수 있습니다.

관련 게시물은 게시글 하단에 위치한 about 아래에 표시됩니다.

키를 입력하지 않는 경우, 임의의 게시물이 노출됩니다.

![image](https://user-images.githubusercontent.com/39720852/156128965-81e831f0-dcd0-4e33-9f2f-660f83e94b0f.png)

---

.

자! 이렇게 해서 Github 블로그 게시글 작성 방법을 살펴봤습니다.

첫 포스팅할 생각에 신나지 않나요😝

다음 글에서는 <span style="background-color:#f1f8ff">**블로그 댓글 기능**</span>에 대해서 소개해 드리도록 하겠습니다.

.

🔗 다음 글 바로가기 [GitHub 블로그 만들기 (6) - 블로그 댓글 기능](/blog/git-github/
github-blog/2022-02-09-github_blog(6))

.

**오류 및 오타 지적, 질문, 인사** 등 무엇이든 언제나 환영입니다!

읽어주셔서 감사합니다.

끝!🦕

.

---

**👍 참고**

* [Hydejack 공식문서](https://hydejack.com/docs/)
