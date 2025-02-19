---
#112
layout: post
title: "[Android] Error - ndk로 인한 빌드 에러 해결"
date: 2025-02-04 15:00:00 +0900
categories: error
tags: [Android error, NDK error, build error]
---

안녕하세요, 해을입니다🦖

이번 글에서는 <span style="background-color:#ffdce0">**ndk로 인한 빌드 에러 해결 방법**</span>에 대해 알아보겠습니다!

## 🚨 에러 발생

![Image](https://github.com/user-attachments/assets/eaa4f5b5-1fd4-4fda-b84b-25e5fdb66f1f)

```
Error:Execution failed for task ':app:clean'.
> Unable to delete directory: C:\........\app\build\intermediates
```

옛날 프로젝트를 맡아 다른 버전의 안스에서 작업하던 중,,,,,

하루 전까지 빌드와 실행 모두 잘 되던 상태에서 갑자기 **<span style="background-color:#ffdce0">Error:Execution failed for task ':app:clean'. 에러</span>**가 발생했습니다.

## ❓ 원인

해당 에러는 어떠한 충돌에 의한 것으로 만능 해결책인 **Invalidate Caches / Restart**를 실행하면 해결된다고 했지만,,,

저는 해결되지 않았습니다^^,,,

눈물을 닦고 이것저것 살펴보다 보니 누가 봐도 수상한 메시지 발견!

![Image](https://github.com/user-attachments/assets/25d43857-0bd8-4462-8a23-9ae48a065b30)

**<span style="background-color:#fff5b1">ndk does not contain any platforms</span>** 에러 메시지를 보니 NDK 관련 이슈인 것 같았습니다.

어제 다른 프로젝트를 작업하던 중 NDK를 설치했다가 삭제하지 않았는데 이런 식으로 발목을 잡힐 줄은 몰랐네요😂

## ❗ 해결

![Image](https://github.com/user-attachments/assets/d2a6d17a-606d-4a81-af58-8626dd73b4d3)

**<span style="background-color:#dcffe4">NDK 제거 및 Invalidate Caches / Restart 실행 후에</span>** 재시도해 본 결과, 빌드와 실행 모두 정상적으로 작동되었습니다.

---

.

자! 이렇게 해서 **ndk로 인한 빌드 에러**에 대해 알아봤는데요.

비슷한 에러를 마주하신 다른 분들께 도움이 되었으면 좋겠습니다😊

그럼 다음 글에서는 또 다른 error에 대해 소개해 드리도록 하겠습니다.

.

**오류 및 오타 등 피드백, 질문, 인사** 등 무엇이든 언제나 환영입니다!

읽어주셔서 감사합니다.

끝!🦕
