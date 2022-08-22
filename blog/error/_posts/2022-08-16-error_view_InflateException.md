---
#095
layout: post
title: "[Android] Error - android.view.InflateException"
date: 2022-08-16 15:21:00 +0900
categories: error
tags: [Android error, InflateException, view]
---

안녕하세요, 해을입니다🦖

이번 글에서는 <span style="background-color:#ffdce0">**android.view.InflateException**</span>에 대해 알아보겠습니다!

## 💡 에러 발생

![image](https://user-images.githubusercontent.com/39720852/184814064-ef316756-c3a5-4735-8d88-bfcb0d4f6360.png)

```
E/AndroidRuntime: FATAL EXCEPTION: main
    Process: com.afume.afume_android, PID: 3768
    android.view.InflateException: Binary XML file line #28 in com.afume.afume_android:layout/dialog_app_update: Binary XML file line #28 in com.afume.afume_android:layout/dialog_app_update: Error inflating class com.google.android.material.button.MaterialButton
    Caused by: android.view.InflateException: Binary XML file line #28 in com.afume.afume_android:layout/dialog_app_update: Error inflating class com.google.android.material.button.MaterialButton
    Caused by: java.lang.reflect.InvocationTargetException
```

splash 동작 이후에 업데이트 확인용 다이얼로그를 추가하기 위해 **Material Button을 사용하던 중 <span style="background-color:#ffdce0">InvocationTargetException</span>이 발생**했습니다.

지금까지 다른 뷰에서도 문제없이 Material Button을 잘 사용했는데, 갑자기 error가 발생한 이유가 무엇일까요?

## 💡 원인

위 에러가 발생한 이유는 **Material 테마가 아닌 Activity에서 Material 컴포넌트를 사용했기 때문**이라고 합니다.

관련 파일들을 살펴보니 아래와 같이 **SplashActivity의 경우, AppCompat로 설정**되어있었습니다.

![image](https://user-images.githubusercontent.com/39720852/184854876-c3022f44-1b5c-49bc-bff4-355bf06d4c40.png)

![image](https://user-images.githubusercontent.com/39720852/184854968-4fc1b0f6-5d7b-4926-8af1-df1f0c2b177a.png)

다른 팀원이 작업하던 곳의 추가 작업을 맡으면서 기본적인 사항을 신경 쓰지 못한 것이 문제였네요!

## 💡 해결

![image](https://user-images.githubusercontent.com/39720852/184856385-4f136471-c324-46e2-a267-05b3973b4b84.png)

**<span style="background-color:#fff5b1">SplashActivity의 테마를 Material로 변경</span>**하니 정상적으로 실행되었습니다.

## 💡 느낀 점

이번 경험을 통해 **에러가 발생하지 않더라도 동작 과정을 이해하는 것이 중요**하다는 것을 깨닫게 되었습니다.

또한 다른 사람의 작업을 이어 받았을 경우, **기본적인 것부터 꼼꼼하게 확인**하는 것이 중요하다는 것을 알게 되었습니다.

---

자! 이렇게 해서 InvocationTargetException에 대해 알아봤는데요.

오늘의 기록을 통해 다음에는 위와 같은 문제를 겪지 않았으면 좋겠습니다😊

다음 글에서는 또 다른 error에 대해 소개해 드리도록 하겠습니다.
<br/><br/><br/>
**오류 및 오타 지적, 질문, 인사** 등 무엇이든 언제나 환영입니다!

읽어주셔서 감사합니다.

끝!🦕
<br/>

## 👍 참고

- [[kotlin - Error] 코틀린 Android Error inflating class com.google.android.material.button.MaterialButton](https://fre2-dom.tistory.com/464)
