---
#110
layout: post
title: "[VSCode] 윈도우에서 한글 입력 시 마지막 글자가 2번씩 입력되는 문제"
date: 2025-01-08 13:00:00 +0900
categories: etc-dev
tags: [VSCode error, Microsoft IME]
---

안녕하세요, 해을입니다🦖

이번 글에서는 윈도우에서 <span style="background-color:#ffdce0">**한글 입력 시 마지막 글자가 2번씩 입력되는 문제**</span>에 대해 알아보겠습니다!

## 🚨 문제 발생

![image](https://github.com/user-attachments/assets/6fe95a4e-44e7-4d5c-9ebe-5b0fe901cc77)

회사에서 새 노트북을 받고 신나는 마음으로 작업을 하던 중

**Visual studio Code에서 한글로 입력한 뒤 포커스를 다른 곳으로 이동하면 마지막 글자가 2번씩 입력**되는 사소하지만 아~주 굉~장히 불편한 문제가 발생했습니다.

프로그램 재실행, 노트북 재부팅 등 여러 방법을 시도해 봤지만 쉽게 해결되지 않았습니다.

## ❓ 원인

이 문제는 유저에 따라 Visual Studio Code 뿐만 아니라 Office 프로그램, 브라우저 등 다양한 곳에서 발생하고 있었는데요.

검색해 본 결과 **윈도우 11 한글 입력기 호환성이 원인**이라고 합니다. 

## ❗ 해결

1. **[ `윈도우 설정(윈도우 키 + i )` > `시간 및 언어` ]** 클릭
    ![image](https://github.com/user-attachments/assets/39c35158-65b7-48ec-8033-00da02755b26)

2. **[ `언어 및 지역` ]** 메뉴 클릭
    ![image](https://github.com/user-attachments/assets/858ea398-846e-44ec-b635-e6783a2ddc52)

3. **[ `한국어` 메뉴의 우측 `더보기` > `언어 옵션` ] 클릭**
    ![image](https://github.com/user-attachments/assets/e1bea4e6-b4e6-42fe-ace5-a67247c1eacf)

4. **[ `Microsoft 입력기` 메뉴의 우측 `더보기` > `키보드 옵션` ] 클릭**
    ![image](https://github.com/user-attachments/assets/7f53aeac-5b2c-43c5-915d-3f2d051f8cf8)

5. **`호환성` `켬`**으로 설정
    ![image](https://github.com/user-attachments/assets/ae31658b-bdbe-4678-8e35-13ab6e02899a)

하지만 이 문제는 윈도우11 자체적인 것으로 위 방법은 임시방편밖에 되지 않으며

<span style="background-color:#FFE6E6">**상황에 따라 호환성을 끈 상태에서 정상 동작할 수도**</span> 있다고 하니 자신의 상황에 맞게 적용하여 사용하는 것이 중요할 것 같습니다.

---

.

자! 이렇게 해서 **한글 입력 시 마지막 글자가 2번씩 입력되는 문제**에 대해 알아봤는데요.

오늘의 기록을 통해 다음에는 위와 같은 문제를 겪지 않았으면 좋겠습니다😊

.

**오류 및 오타 등 피드백, 질문, 인사** 등 무엇이든 언제나 환영입니다!

읽어주셔서 감사합니다.

끝!🦕
<br/>

## 👍 참고

- [윈도우11 키보드 타자 입력 밀림 현상 해결 방법](https://lifenourish.tistory.com/2378)
