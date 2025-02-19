---
#104
layout: post
title: "[Android] Navigation drawer - menu item의 actionView가 오른쪽으로 치우치는 문제"
date: 2022-09-20 19:37:00 +0900
categories: view
tags: [Android, Navigation drawer, menu, actionView]
---

안녕하세요, 해을입니다🦖

이번 글에서는 <span style="background-color:#dcffe4">**menu item의 actionView가 오른쪽으로 치우치는 문제**</span>에 대해 알아보겠습니다!

## 💡 문제 발견

![image](https://user-images.githubusercontent.com/39720852/193059592-c0f09e66-1991-4b44-b6e5-e0709f43ac75.png)

menu item의 기본 설정 icon은 좌측에 위치하기 때문에 우측에 icon을 넣기 위해서는 actionView를 사용해야 했습니다.

그런데 textView와 imageView를 사용하여 뷰를 만든 후에 actionView로 추가한 결과,

위 사진과 같이 **actionView가 오른쪽으로 치우치는 문제**가 발생했습니다.

gravity 설정을 다시 하는 등 여러 가지 시도를 해봤지만 쉽게 해결되지 않아 며칠 동안 꽤나 삽질을 했습니다,,ㅎㅎ

## 💡 해결하기

### 🥨 menu item의 title 설정

해결 방법은 무척 간단한데요,

<span style="background-color:#fff5b1">**title을 @null로 설정**</span>하면 title 영역이 사라지면서 actionView가 꽉 차게 배치됩니다.

![image](https://user-images.githubusercontent.com/39720852/193064172-b7a85866-a589-4e13-a31f-ec920b3782ee.png)


---

.

자! 이렇게 해서 menu item의 actionView가 오른쪽으로 치우치는 문제에 대해 알아봤는데요.

글을 읽어주신 분들께 도움이 됐으면 좋겠습니다😊

다음 글에서는 또 다른 유용한 view 관련 내용에 대해 소개해 드리도록 하겠습니다.
<br/><br/><br/>
**오류 및 오타 등 피드백, 질문, 인사** 등 무엇이든 언제나 환영입니다!

읽어주셔서 감사합니다.

끝!🦕
<br/>

## 👍 참고

- [안드로이드 공식문서](https://developer.android.com/guide/topics/resources/menu-resource)
- [ActionLayout for navigationview items displays on right side](https://stackoverflow.com/questions/34893872/actionlayout-for-navigationview-items-displays-on-right-side)
