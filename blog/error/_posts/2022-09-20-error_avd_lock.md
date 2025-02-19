---
#102
layout: post
title: "[Android] Error - 안드로이드 스튜디오 AVD 에뮬레이터 lock 에러 해결"
date: 2022-09-20 12:24:00 +0900
categories: error
tags: [Android error, avd, emulator, lock]
---

안녕하세요, 해을입니다🦖

이번 글에서는 <span style="background-color:#ffdce0">**안드로이드 스튜디오 AVD 에뮬레이터 lock 에러**</span>에 대해 알아보겠습니다!

## 🚨 에러 발생

![image](https://user-images.githubusercontent.com/39720852/191164574-d64a9d39-7534-459d-869f-76079ec3e27d.png)

```
Error while waiting for device: AVD Afume is already running.
If that is not the case, delete the files at
   C:\Users\user\.android\avd/Afume.avd/*.lock
and try again.
```

평소처럼 작업 후에 **에뮬레이터를 실행하던 중 <span style="background-color:#ffdce0">lock 에러</span>가 발생**했습니다.

하루 전까지도 문제없이 실행되던 에뮬레이터에서 갑자기 error가 발생한 이유는 무엇일까요?

## ❓ 원인

위 에러가 발생한 이유는 **<span style="background-color:#fff5b1">에뮬레이터를 비정상적으로 종료했기 때문</span>**이라고 합니다.

어제 외출을 하느라 노트북을 급하게 강제 종료한 것이 문제였던 것 같습니다.

## ❗ 해결

**<span style="background-color:#dcffe4">AVD Manager에서 사용하던 에뮬레이터를 삭제하고 새로 만들어서 실행</span>**하니 정상적으로 작동되었습니다.dcffe4

## 💡 느낀 점

이번 경험을 통해 **실행뿐만 아니라 종료 과정도 중요**하다는 것을 깨닫게 되었습니다.

---

.

자! 이렇게 해서 AVD 에뮬레이터 lock 에러에 대해 알아봤는데요.

오늘의 기록을 통해 다음에는 위와 같은 문제를 겪지 않았으면 좋겠습니다😊

그럼 다음 글에서는 또 다른 error에 대해 소개해 드리도록 하겠습니다.
<br/><br/><br/>
**오류 및 오타 등 피드백, 질문, 인사** 등 무엇이든 언제나 환영입니다!

읽어주셔서 감사합니다.

끝!🦕
<br/>

## 👍 참고

- [[Android] Android Studio AVD 에뮬레이터 실행 시 lock 오류 해결하기](https://lieadaon.tistory.com/entry/Android-Android-Studio-AVD-%EC%97%90%EB%AE%AC%EB%A0%88%EC%9D%B4%ED%84%B0-%EC%8B%A4%ED%96%89-%EC%8B%9C-lock-%EC%98%A4%EB%A5%98-%ED%95%B4%EA%B2%B0%ED%95%98%EA%B8%B0)
- [[Android] 안드로이드 스튜디오 AVD 에뮬레이터 lock 오류 해결법](https://mycodepia.tistory.com/27)
