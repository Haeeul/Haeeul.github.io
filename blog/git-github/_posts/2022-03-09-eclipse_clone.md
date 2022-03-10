---
#012
layout: post
title: "Eclipse에서 Git 사용하기 - clone"
image: https://user-images.githubusercontent.com/39720852/157496299-bd43b166-6f42-497b-a5ee-cbd86e8adeeb.png
date: 2022-03-09 14:22:00 +0900
categories: git-github
tags: [Git, GitHub, Eclipse, Clone]
description: >
  📥 이클립스에서 Git Repository를 내려받습니다.
# related_posts:
#   - /blog/git-github/2022-02-07-github_blog(4)/
#   - /blog/git-github/2022-02-08-github_blog(5)/
#   - /blog/git-github/2022-02-09-github_blog(6)/
---

안녕하세요, 해을입니다🦖

이번 글에서는 <span style="background-color:#f1f8ff">**이클립스에서 clone하는 방법**</span>에 대해 알아보겠습니다!

* toc
{:toc}

### 🥨 1. 원격 저장소 주소 복사

clone 받을 **원격 저장소의 주소를 복사**합니다.

![image](https://user-images.githubusercontent.com/39720852/157279237-d3aa4b7d-c09d-4043-bce0-efc32ac7fed5.png)

### 🥨 2. 이클립스 실행 및 Git 퍼스펙티브 추가

이클립스를 실행하여 우측 상단 **Open Perspective 버튼**을 클릭한 후, **Git을 추가**합니다.

![image](https://user-images.githubusercontent.com/39720852/157279770-80181c17-bbfe-4b42-8da0-9a56c37fbed5.png)

![image](https://user-images.githubusercontent.com/39720852/157280473-192eadb9-f5d7-45ec-a440-41432bccbb74.png)

### 🥨 3. 원격 저장소 Clone

메뉴에서 **Clone a Git repository**를 클릭합니다.

![image](https://user-images.githubusercontent.com/39720852/157280721-def39cf3-c46a-42b7-991b-f156ba0c0972.png)

URI에 복사해둔 **원격 저장소 주소를 붙여넣기**하면, Host와 path 칸이 자동으로 입력됩니다.

하단에 있는 **User와 Password는 직접 입력**한 후, 다음으로 넘어갑니다.

![image](https://user-images.githubusercontent.com/39720852/157281345-8886d8f5-0370-45b7-8ba9-90ba64954698.png)

**브랜치 선택** 후, 다음으로 넘어갑니다.

![image](https://user-images.githubusercontent.com/39720852/157281822-7da0d57f-45c3-4681-b91b-6e9a85b27aa8.png)

clone 받을 **로컬 저장소 위치를 입력**합니다.

![image](https://user-images.githubusercontent.com/39720852/157284803-2e3f445a-f2c5-4cde-a041-1489969deb05.png)

### 🥨 4. 프로젝트 가져오기

Working Tree에서 작업하려는 **프로젝트를 Import** 합니다.

![image](https://user-images.githubusercontent.com/39720852/157288462-0e98bf3a-6ab9-4d47-84ee-cbe3fcb03edb.png)

**Import 경로 확인** 후, Finish 버튼을 클릭하면 프로젝트가 생성됩니다.

![image](https://user-images.githubusercontent.com/39720852/157288794-6600d528-ec16-43e2-acec-0c76ecea84f3.png)

![image](https://user-images.githubusercontent.com/39720852/157289034-7af324ff-00fb-4d0c-920b-2c20bcac0c88.png)

---

자! 이렇게 해서 이클립스에서 Git Clone하는 방법을 알아봤습니다.

다음 글에서는 <span style="background-color:#f1f8ff">**Eclipse에서 commit하는 방법**</span>에 대해서 소개해 드리도록 하겠습니다.
<br/><br/><br/>
**오류 및 오타 지적, 질문, 인사** 등 무엇이든 언제나 환영입니다!

읽어주셔서 감사합니다.

끝!🦕
<br/><br/><br/>
🔗 다음 글 바로가기 [GitHub 블로그 만들기 (5) - 블로그 게시글 작성](/blog/git-github/2022-02-08-github_blog(5))

## 👍 참고

* [[Git] 이클립스에서 Git Repository 내려받기](https://hgko1207.github.io/2020/05/18/eclipse-git-clone/)
