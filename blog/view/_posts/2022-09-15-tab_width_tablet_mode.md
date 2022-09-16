---
#101
layout: post
title: "[Android] 태블릿 또는 가로 모드에서 Tab의 너비가 좁게 표시되는 문제"
date: 2022-09-15 23:15:00 +0900
categories: view
tags: [Android, view, Tab, TabLayout, tablet, Landscape]
---

안녕하세요, 해을입니다🦖

이번 글에서는 <span style="background-color:#fff5b1">**태블릿 또는 가로 모드에서 Tab의 너비가 좁게 표시되는 문제**</span>에 대해 알아보겠습니다!

## 💡 문제 발견

![image](https://user-images.githubusercontent.com/39720852/190442488-f73bfb53-f276-4085-8eae-fd8620814c0a.png)

태블릿과 가로 모드처럼 넓은 화면일 때, Tab의 너비가 좁게 표시되는 문제를 발견했습니다.

## 💡 해결하기

### 🥨 TabLayout 속성 추가

![image](https://user-images.githubusercontent.com/39720852/190443048-9e3e5bd0-b846-4a12-b2cf-af8b2f4752f4.png)

```
app:tabGravity="fill" // 전체 너비를 일정한 간격으로 나눠서 정렬
app:tabMode="fixed"   // 화면에 모든 Item을 노출
app:tabMaxWidth="0dp" // 최대 너비를 parent에 꽉 차도록(0dp)
```

해결 방법은 무척 간단한데요.

TabLayout에 3가지 속성을 추가하면 됩니다.

### 🥨 확인하기

![image](https://user-images.githubusercontent.com/39720852/190444648-b859b807-31a4-4285-9db0-0324d4fe8868.png)

Tab의 너비가 화면에 맞게 정상적으로 표시되는 것을 확인할 수 있습니다.

## 💡 느낀 점

이번 경험을 통해 **다양한 모드에서의 비율을 고려하여 작업하는 것이 중요하다는** 것을 깨닫게 되었는데요.

view를 배치하는데 있어서 좀 더 폭넓게 생각하는 계기가 되었습니다.

---

.

자! 이렇게 해서 Tab 너비와 관련된 문제 해결 방법에 대해 알아봤는데요.

글을 읽어주신 분들께 도움이 됐으면 좋겠습니다😊

다음 글에서는 또 다른 유용한 view 관련 방법에 대해 소개해 드리도록 하겠습니다.
<br/><br/><br/>
**오류 및 오타 지적, 질문, 인사** 등 무엇이든 언제나 환영입니다!

읽어주셔서 감사합니다.

끝!🦕
<br/>

## 👍 참고

- [안드로이드 공식 문서](https://developer.android.com/reference/com/google/android/material/tabs/TabLayout)
- [[Android] TabLayout 너비가 꽉 차지 않는 문제에 관하여](https://velog.io/@dev_2dong/Android-TabLayout-%EB%84%88%EB%B9%84%EA%B0%80-%EA%BD%89-%EC%B0%A8%EC%A7%80-%EC%95%8A%EB%8A%94-%EB%AC%B8%EC%A0%9C%EC%97%90-%EA%B4%80%ED%95%98%EC%97%AC)
- [[Android] TabLayout의 Tab의 가로 길이가 태블릿에서 좁게 표시되는 문제](https://satisfactoryplace.tistory.com/227)
