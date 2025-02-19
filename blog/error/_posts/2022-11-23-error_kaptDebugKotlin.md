---
#107
layout: post
title: "[Android] Error - Execution failed for task ':app:kaptDebugKotlin' 및 java.lang.reflect.InvocationTargetException 에러 해결"
date: 2022-12-08 17:51:00 +0900
categories: error
tags: [Android error, kaptDebugKotlin, InvocationTargetException]
---

안녕하세요, 해을입니다🦖

이번 글에서는 <span style="background-color:#ffdce0">**xecution failed for task ':app:kaptDebugKotlin' 및 java.lang.reflect.InvocationTargetException 에러 해결 방법**</span>에 대해 알아보겠습니다!

## 🚨 에러 발생

![image](https://user-images.githubusercontent.com/39720852/206910034-3ed27466-a9f0-4828-b8c4-d66d9de21279.png)

```
Execution failed for task ':app:kaptDebugKotlin'.
> A failure occurred while executing org.jetbrains.kotlin.gradle.internal.KaptWithoutKotlincTask$KaptExecutionWorkAction
   > java.lang.reflect.InvocationTargetException (no error message)
```

response data class를 수정하는 과정에서 **<span style="background-color:#ffdce0">xecution failed for task ':app:kaptDebugKotlin' 및 java.lang.reflect.InvocationTargetException 에러</span>**가 발생했습니다.

처음 보는 내용의 에러였고, 에러가 발생한 지점을 알려주지 않아 꽤나 골머리를 앓았습니다.

## ❓ 원인

에러를 검색하자 원인으로 맥북, gradle, room 등 다양한 요소들이 쏟아져 나왔습니다.

하지만 저의 경우, **<span style="background-color:#fff5b1">수정한 data class를 반영하는 과정에서 미처 변경하지 못한 파일이 있어 타입 불일치</span>**로 인해 발생한 에러였습니다.

하필 며칠 전에 채용 과제를 제출하면서 안드로이드 스튜디오와 gradle 전체를 업그레이드하고

Room을 사용했었기에 관련 키워드로 나오던 다른 것들을 원인으로 잘못 파악하여 삽질을 오래 했습니다.

그러던 중 다행히 예전부터 도움을 많이 받았던 막무가내막내님의 포스팅 덕분에 원인을 찾아 해결할 수 있었습니다.

## ❗ 해결

![image](https://user-images.githubusercontent.com/39720852/206907355-481f9f8c-ff9d-4c69-8276-63a86167d592.png){: width="450"}

수정한 data class를 사용하는 모든 파일을 다시 살펴보며 수정사항이 반영되지 않은 부분을 찾아 고쳤습니다.

하지만 여전히 에러가 발생했고 **<span style="background-color:#dcffe4">Clean Project 및 Rebuild Project</span>**를 실행한 후에 다시 시도해 본 결과, 정상적으로 작동되었습니다.

## 💡 느낀 점

타입 불일치의 경우, 에러로 나타날 것이라고 안일하게 파일을 수정했던 것이 가장 큰 원인인 것 같습니다.

이번 경험을 통해 수정사항을 반영하는데 있어 관련 파일을 꼼꼼하게 살펴보는 것이 중요하다는 것을 다시 한번 깨닫게 되었습니다.

---

.

자! 이렇게 해서 xecution failed for task ':app:kaptDebugKotlin' 및 java.lang.reflect.InvocationTargetException 에러에 대해 알아봤는데요.

오늘의 기록을 통해 다음에는 위와 같은 문제를 겪지 않았으면 좋겠습니다😊

그럼 다음 글에서는 또 다른 error에 대해 소개해 드리도록 하겠습니다.
<br/><br/><br/>
**오류 및 오타 등 피드백, 질문, 인사** 등 무엇이든 언제나 환영입니다!

읽어주셔서 감사합니다.

끝!🦕
<br/>

## 👍 참고

- [[안드로이드] * What went wrong:Execution failed for task ':app:kaptDebugKotlin'.> A fail](https://youngest-programming.tistory.com/305)
