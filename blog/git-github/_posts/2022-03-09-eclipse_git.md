---
#012
layout: post
title: "Eclipse에서 Git 사용하기"
image: https://user-images.githubusercontent.com/39720852/157686888-ecb6dc04-cd51-4967-b4ce-879551fa9517.png
date: 2022-03-09 14:22:00 +0900
categories: git-github
tags: [Git, GitHub, Eclipse, Clone, Commit, Push]
description: >
  📥 Eclipse에 Git을 연동하여 사용합니다.
# related_posts:
#   - /blog/git-github/2022-02-07-github_blog(4)/
#   - /blog/git-github/2022-02-08-github_blog(5)/
#   - /blog/git-github/2022-02-09-github_blog(6)/
---

안녕하세요, 해을입니다🦖

이번 글에서는 <span style="background-color:#f1f8ff">**이클립스에서 Git 사용하는 방법**</span>에 대해 알아보겠습니다!

* toc
{:toc}

## 💡 이클립스(eclipse)에서 Git 사용하기

잠시 잊고 지냈던 알고리즘 공부를 다시 시작하기 위해 오랜만에 이클립스를 실행시켰습니다.

Clone 하려고 보니 이클립스에서 Git 사용하는 방법을 까먹었지 뭐예요^^,,,

자주 사용하지 않으면 쉬운 거라도 까먹는 것 같습니다,,,

그래서 다음에는 빠르게 찾아볼 수 있도록 **이클립스에서 Git 사용하는 방법을 정리**해두려 합니다.

참고로 기존 저장소에서 Clone 받는 것이 아닌 **처음으로 이클립스와 Git을 연동하시는 분**들도

새로 Repository를 생성한 다음 아래 과정을 진행하시면 됩니다.

## 💡 Git 연동 및 내려받기 - Clone

### 🥨 1. 원격 저장소 주소 복사

clone 받을 **원격 저장소의 주소를 복사**합니다.

(새로 작업하시는 경우, 새로운 저장소를 만들어 주세요.)

![image](https://user-images.githubusercontent.com/39720852/157279237-d3aa4b7d-c09d-4043-bce0-efc32ac7fed5.png)

묵혀뒀던 알고리즘 레포 소환
{:.figcaption}

### 🥨 2. 이클립스 실행 및 Git 퍼스펙티브 추가

이클립스를 실행하여 우측 상단 **Open Perspective 버튼**을 클릭한 후, **Git을 추가**합니다.

![image](https://user-images.githubusercontent.com/39720852/157279770-80181c17-bbfe-4b42-8da0-9a56c37fbed5.png)

![image](https://user-images.githubusercontent.com/39720852/157280473-192eadb9-f5d7-45ec-a440-41432bccbb74.png)

Git 추가된 화면
{:.figcaption}

### 🥨 3. 원격 저장소 Clone

메뉴에서 **Clone a Git repository**를 클릭합니다.

![image](https://user-images.githubusercontent.com/39720852/157280721-def39cf3-c46a-42b7-991b-f156ba0c0972.png)

URI에 복사해둔 **원격 저장소 주소를 붙여넣기**하면, Host와 path 칸이 **자동으로 입력**됩니다.

하단에 있는 **User와 Password는 직접 입력**한 후, 다음으로 넘어갑니다.

![image](https://user-images.githubusercontent.com/39720852/157870416-d3aa2a92-8e4d-4b51-be23-3a0329144942.png)

**브랜치 선택** 후, 다음으로 넘어갑니다.

![image](https://user-images.githubusercontent.com/39720852/157281822-7da0d57f-45c3-4681-b91b-6e9a85b27aa8.png)

clone 받을 **로컬 저장소 위치를 입력**합니다.

![image](https://user-images.githubusercontent.com/39720852/157870012-3b17c631-b281-499f-8768-4211fb959a2f.png)

### 🥨 4-1 프로젝트 가져오기

Working Tree에서 작업할 **프로젝트를 Import** 합니다.

![image](https://user-images.githubusercontent.com/39720852/157288462-0e98bf3a-6ab9-4d47-84ee-cbe3fcb03edb.png)

**Import 경로 확인** 후, Finish 버튼을 클릭하면 해당 프로젝트가 생성됩니다.

![image](https://user-images.githubusercontent.com/39720852/157870055-518b3d61-ebcb-4f37-ac75-922dfdc65d43.png)

![image](https://user-images.githubusercontent.com/39720852/157289034-7af324ff-00fb-4d0c-920b-2c20bcac0c88.png)

### 🥨 4-2 프로젝트 생성하기

Import 하지 않고 새로 프로젝트를 만드는 경우도 살펴보겠습니다.

새로 만든 프로젝트는 Git에 연동되지 않아 따로 설정해야 합니다.

연동 상태는 **프로젝트 옆에 [저장소명 master] 표시**로 알 수 있으며, 표시가 있어야 연동된 상태입니다.

![image](https://user-images.githubusercontent.com/39720852/157701982-a5143244-698d-428f-9c84-7e67dea55464.png)

연동할 프로젝트를 우클릭한 후, **Team -> Share Project**를 클릭합니다.

![image](https://user-images.githubusercontent.com/39720852/157716994-977d33a3-fab0-46d3-84d0-841c9f826ac0.png){: width="500"}

로컬 저장소 생성 창에서 **Use or create repository in parent folder of project**를 체크하면

생성한 프로젝트 폴더 내에 로컬 저장소를 생성하게 됩니다.

다른 폴더에 로컬 저장소를 생성하고 싶다면 체크를 해제하고 create를 통해 경로를 지정하면 됩니다.

저는 체크한 상태로 진행하겠습니다.

![image](https://user-images.githubusercontent.com/39720852/157718513-da6431ca-9a11-4d0d-9894-fe4fdd481311.png)

Finish 버튼을 클릭하면 프로젝트가 연동되어 표시가 나타난 것을 확인할 수 있습니다.

![image](https://user-images.githubusercontent.com/39720852/157719452-202df306-01a0-4e59-9d18-ca88b6644635.png)

## 💡 업로드 - Commit, Push

### 🥨 1. Git Staging 창 띄우기

**Window -> Show View -> Other**에서 **Git Staging**을 선택하면

하단에 Git 작업을 진행할 수 있는 Git Staging 창이 추가됩니다.

![image](https://user-images.githubusercontent.com/39720852/157720013-ff40cacd-aa09-4543-95dd-b22a8d83294c.png)

![image](https://user-images.githubusercontent.com/39720852/157720160-d1b6fc4e-e05e-47a6-bce4-42606b7a3e4c.png)

### 🥨 2. Add

commit할 파일들을 선택 후, **+ 버튼을 눌러 Add(staged Changes로 이동)**합니다.

Add된 파일들은 ? 표시에서 *과 +로 표시가 바뀝니다.

![image](https://user-images.githubusercontent.com/39720852/157690153-1dd753da-d237-4ac3-b4b6-e151adccff76.png)

![image](https://user-images.githubusercontent.com/39720852/157692689-fe1582ba-0fae-4fb2-80ce-ebc09da6a865.png)

? : 추적 안되는 상태, */+ : add(스테이지) 된 상태
{:.figcaption}

### 🥨 3. Commit

**커밋 메시지 작성 후, Commit 버튼을 클릭**합니다.

이때, Commit and Push를 통해 push까지 한번에 진행할 수도 있습니다.

![image](https://user-images.githubusercontent.com/39720852/157691182-428a6564-5683-45b2-ab3e-a7a677d05219.png)

### 🥨 4. Push

따로 Push 하는 경우, 해당 프로젝트 **우클릭 -> Team -> Push to Upstream**을 통해 Push 할 수 있습니다.

![image](https://user-images.githubusercontent.com/39720852/157720759-b4797755-3f9c-44e3-aac4-760104a31758.png)

---

자! 이렇게 해서 이클립스에서 Git 사용하는 방법을 알아봤습니다.

<br/>
**오류 및 오타 지적, 질문, 인사** 등 무엇이든 언제나 환영입니다!

읽어주셔서 감사합니다.

끝!🦕
<br/>

## 👍 참고

* [[Git] 이클립스에서 Git Repository 내려받기](https://hgko1207.github.io/2020/05/18/eclipse-git-clone/)
* [이클립스(eclipse) 깃허브(Git) 사용법 총정리](https://hyunipad.tistory.com/70)
