---
layout: post
title: "GitHub 블로그 만들기 (1) - 블로그 생성"
image: https://user-images.githubusercontent.com/39720852/152404568-b2da4b99-b9b1-4bcb-8c94-a2fea473c9db.png
accent_image:
  background: url(https://user-images.githubusercontent.com/39720852/152405232-29b296d1-653c-4505-ad3c-07fd5a680d17.png) center/cover
  overlay: true
date: 2022-02-04 00:49:00 +0900
categories: git-github
tags: [GitHub Pages, GitHub blog]
description: >
  🥨 GitHub Pages에 대해 알아보고 블로그를 생성해 봅니다.
related_posts:
  - /blog/git-github/2022-02-05-github_blog(2)/
  - /blog/git-github/2022-02-06-github_blog(3)/
  - /blog/git-github/2022-02-07-github_blog(4)/
---

안녕하세요, 해을입니다🦖

이번 글에서는 <span style="background-color:#f1f8ff">**GitHub 블로그 만드는 방법**</span>에 대해 알아보겠습니다!

* toc
{:toc}

실습 표시 : 🥨  
(🥨 표시는 실습 부분임을 뜻합니다)

## 💡 GitHub Pages란?

우리가 흔히 **GitHub 블로그**라고 부르는 이 서비스의 정식 명칭은 <span style="background-color:#fff5b1">**GitHub Pages**</span>입니다.

GitHub Pages는 GitHub의 **Repository(저장소)에서 파일을 가져와 정적 웹 사이트를 호스팅 해주는 서비스**로 GitHub에서 제공하고 있습니다.

public 저장소에 한해서 무료로 이용 가능하며, private 저장소를 호스팅 하려면 GitHub 계정이 Pro 이상이여야 합니다.

## 💡 준비하기

### 1. git 설치

🥨 git이 [설치](http://git-scm.com/download/win)되어 있어야 합니다.

### 2. Visual Studio Code 설치

🥨 편집기는 [vscode](https://code.visualstudio.com/)를 사용합니다.

## 💡 GitHub 블로그 생성

### 1. 새로운 Repository 생성

🥨 Repositories 탭 또는 오른쪽 상단 + 탭을 통해 **Repository 생성 페이지**로 들어갑니다.

![GitHub블로그-레포생성](https://user-images.githubusercontent.com/39720852/152359126-02f10610-6903-4e11-9535-656c5eafa768.png)

### 2. Repository 이름 설정

🥨 레포명을 <span style="background-color:#fff5b1">**username.github.io**</span>로 설정하고, **Add a README file**을 체크합니다.  
(ex : Haeeul.github.io)

![GitHub블로그-레포이름설정](https://user-images.githubusercontent.com/39720852/152364544-71e73390-ecf5-4c3a-bd94-a48d32a12a89.png){: width="600"}

부캐 소환
{:.figcaption}

레포명의 첫 부분이 <span style="background-color:#ffdce0">**사용자 이름과 일치하지 않으면 블로그가 작동하지 않을 수 있다**</span>고 하니 정확하게 적어주세요.

또한 <span style="background-color:#ffdce0">**pro 이상의 계정이 아닌 경우, private로는 블로그 이용이 불가능하니**</span> 꼭 public으로 설정해 주세요.

저는 username이 Haeeul2라는 부계정을 이용하여 만들었습니다.

README는 체크하지 않아도 상관없으나, 다음 단계에서 clone 확인용으로 편의상 추가했습니다.

### 3. 로컬저장소에 clone

🥨 Repository가 생성되면 **주소를 복사**합니다.

![GitHub블로그-레포주소복사](https://user-images.githubusercontent.com/39720852/152365904-ad2afccd-db91-4182-aa9b-5f467201374f.png)

🥨 로컬에서 프로젝트를 저장할 폴더를 만들고 해당 폴더로 이동한 후,  
터미널을 실행하여 **Repository를 clone**합니다.

```
git clone (Repository 주소) .

// 예시(터미널 붙여넣기 단축키 - Shift + Ins)
git clone https://github.com/Haeeul2/Haeeul2.github.io.git .
```

> 📌 **git clone (Repository 주소) <span style="background-color:#fff5b1">.</span>**  
> 맨 뒤에 마침표를 붙이지 않으면 원격 저장소 이름의 새로운 폴더가 생기고 그 폴더 안에 파일이 내려받아집니다.  
> 필수는 아니지만 폴더 구조가 복잡해지므로 추가하는 것을 추천드립니다!

> 📌 **clone**  
> : GitHub에 생성한 원격 저장소를 내 컴퓨터(로컬)에 내려받는 것

![GitHub블로그-clone](https://user-images.githubusercontent.com/39720852/152366769-d838b5ea-b55d-4464-8f2a-6e4ceb1f7459.png)

마침표 있는 경우, 해당 위치에 바로 받아짐
{:.figcaption}

![GitHub블로그-clone2](https://user-images.githubusercontent.com/39720852/152366756-fa451d9e-d127-4855-9145-05750b5b2b48.png)

마침표 없는 경우, 새폴더 안에 받아짐
{:.figcaption}

.git 폴더와 README가 생기면 clone 성공!

마침표가 있고 없고의 차이가 느껴지시나요?!

그리고 추가로 <span style="background-color:#ffdce0">**.git 폴더는 기본 설정이 숨김 상태**</span> 이기 때문에 폴더가 안보이시는 분들은 숨긴 항목 표시를 설정하시면 확인 가능합니다.  
window 기준 : [보기] - [표시] - [숨긴 항목]

### 4. 블로그 시작 파일(index.html) 만들기

🥨 clone한 폴더로 **(README.md 파일이 있는 곳)** 이동 후, **index.html** 파일을 생성합니다.

```
// 터미널에서 현재 위치 확인 및 이동
cd username.github.io

echo "Hello World" > index.html
```

> 📌 **cd (폴더명)**  
> : 해당 폴더로 이동

> 📌 **echo "내용" > 파일명**  
> : 해당 파일명과 내용을 가진 새로운 파일을 생성

![GitHub블로그-index생성](https://user-images.githubusercontent.com/39720852/152369831-3ae469d7-f021-4f41-a5e3-ab527a8c095b.png)

마침표 추가한 경우, 폴더 이동 없이 바로 파일 생성
{:.figcaption}

![GitHub블로그-index생성2](https://user-images.githubusercontent.com/39720852/152369732-acd0174d-c837-477b-9ebc-b61cb3770dcc.png)

마침표 없는 경우, 폴더 이동 후에 파일 생성
{:.figcaption}

**GitHub 블로그의 시작 파일은 index.html로 저장**해야 하기 때문에 파일명은 동일하게 해주세요.

생성된 index.html 파일은 열어보면 설정한 "Hello World"를 확인할 수 있습니다.

### 5. 원격 저장소에 push

🥨 아래 명령어를 사용하여 **원격 저장소에 변경사항(index 파일 추가)을 push** 합니다.

```
git add --all

git commit -m "Initial commit"

git push -u origin main
```

> 📌 **git add --all**  
> : 모든 파일을 스테이지에 추가

> 📌 **git commit -m "내용"**  
> : 해당 내용의 메시지와 함께 커밋

> 📌 **git push -u origin main**  
> : 커밋들을 원격 저장소에 업로드

![GitHub블로그-push](https://user-images.githubusercontent.com/39720852/152387750-59d5b599-65c0-4bb7-8621-dbc23738b5cd.png)

### 6. 원격 저장소 확인

🥨 Repository에 index.html이 있다면 push 성공!

![GitHub블로그-원격저장소확인](https://user-images.githubusercontent.com/39720852/152388125-0cd3a768-e22d-4f90-87b9-d19237c8a7c7.png)

### 7. 블로그 생성 확인

🥨 주소창에 **username.github.io**를 입력하면 생성된 블로그를 확인할 수 있습니다.

![GitHub블로그-블로그확인](https://user-images.githubusercontent.com/39720852/152394195-595bcc8f-18c1-467d-ad53-256740480303.png)

---

자! 이렇게 해서 Github 블로그를 만들어봤습니다!

아직 헬(로) 월드뿐이긴 하지만 채워나갈 생각에 설레지 않나요😝

다음 글에서는 <span style="background-color:#f1f8ff">**Jekyll 설치**</span>에 대해서 소개해 드리도록 하겠습니다.
<br/><br/><br/>
**오류 및 오타 지적, 질문, 인사** 등 무엇이든 언제나 환영입니다!

읽어주셔서 감사합니다.

끝!🦕
<br/><br/><br/>
🔗 다음 글 바로가기 [GitHub 블로그 만들기 (2) - Jekyll 설치](/blog/git-github/2022-02-05-github_blog(2))

## 👍 참고

- [GitHub Pages 사이트](https://pages.github.com/)
- [GitHub Pages 공식 문서](https://docs.github.com/en/pages/getting-started-with-github-pages)
- [왕초보를 위한 Github 블로그 만들기(1)](https://zeddios.tistory.com/1222)
