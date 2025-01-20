---
#111
layout: post
title: "[Android] Error - com.android.ddmlib.AdbCommandRejectedException 에러 해결"
date: 2025-01-20 15:00:00 +0900
categories: error
tags: [Android error, AdbCommandRejectedException]
---

안녕하세요, 해을입니다🦖

이번 글에서는 <span style="background-color:#ffdce0">**com.android.ddmlib.AdbCommandRejectedException 에러 해결 방법**</span>에 대해 알아보겠습니다!

## 🚨 에러 발생

![Image](https://github.com/user-attachments/assets/b9f7650d-053b-4951-b680-d97b7de04b3c)

```
com.android.ddmlib.AdbCommandRejectedException: device unauthorized.
This adb server's $ADB_VENDOR_KEYS is not set
Try 'adb kill-server' if that seems wrong.
Otherwise check for a confirmation dialog on your device.
Error while Installing APK
```

다른 버전의 Android studio에서 프로젝트를 실행하는 과정에서 **<span style="background-color:#ffdce0">com.android.ddmlib.AdbCommandRejectedException 에러</span>**가 발생했습니다.

## ❓ 원인

![Image](https://github.com/user-attachments/assets/bad4e9e3-c757-4c6e-9ceb-bb54ce8f8a64)

해당 에러는 **<span style="background-color:#fff5b1">device에서 USB Debugging을 허용하지 않아</span>** 발생한 단순한 에러였습니다.

천천히 살펴보니 실행 기기를 선택하는 창에서 **'[UNAUTHORIZED - Press 'OK' in the 'Allow USB Debugging' dialog on your device]'**라는 안내 문구가 있었습니다.

## ❗ 해결

![Image](https://github.com/user-attachments/assets/55702a6c-e044-4423-87d9-ca3edbb0f349){: width="450"}

**<span style="background-color:#dcffe4">USB를 다시 연결하여 디버깅을 허용한 후에</span>** 재시도해 본 결과, 정상적으로 작동되었습니다.

## 💡 느낀 점

이번 경험을 통해 기본적으로 세팅해둔 것들도 주기적으로 점검하는 것이 중요하다는 것을 다시 한번 깨닫게 되었습니다.

---

.

자! 이렇게 해서 **com.android.ddmlib.AdbCommandRejectedException 에러**에 대해 알아봤는데요.

오늘의 기록을 통해 다음에는 위와 같은 문제를 겪지 않았으면 좋겠습니다😊

그럼 다음 글에서는 또 다른 error에 대해 소개해 드리도록 하겠습니다.

.

**오류 및 오타 지적, 질문, 인사** 등 무엇이든 언제나 환영입니다!

읽어주셔서 감사합니다.

끝!🦕
