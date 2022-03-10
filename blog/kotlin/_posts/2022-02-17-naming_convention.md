---
#010
layout: post
title: "다양한 코딩 표기법(카멜, 파스칼, 스네이크, 헝가리안, 케밥)"
image: https://user-images.githubusercontent.com/39720852/154499954-c028164e-12a5-4aff-8132-7544d80d4704.png
date: 2022-02-17 22:19:00 +0900
categories: kotlin
tags: [camel case, pascal case, snake case, hungarian notation, kebab case]
---

안녕하세요, 해을입니다🦖

이번 글에서는 <span style="background-color:#f1f8ff">**다양한 코딩 표기법**</span>에 대해 알아보겠습니다!

* toc
{:toc}

## 💡코딩 표기법(Naming Convention)

[kotlin 200제] 책을 훑던 중, 참고용으로 짧게 등장하는 표기법에 대한 내용을 발견했습니다.

이전에 프로젝트를 진행하며 네이밍 룰을 정할 때마다 표기법에 대해 검색했던 기억이 있어 이 기회에 정리해두려 합니다.

포스팅을 위해 검색해 보니 다른 언어에서 사용하는 표기법까지 꽤 종류가 많았는데요.

본인이 사용하는 언어와 규칙에 맞는 적절한 표기법을 사용하는 것이 중요한 것 같습니다.

![naming_convention_table](https://user-images.githubusercontent.com/39720852/154694069-c8183119-41d9-497b-b40b-8ecd6e033c2e.png){: width="600"}

### 1. 카멜 표기법(Camel Case) 🐪

<span style="background-color:#fff5b1">**단어를 연결할 때, 첫 글자를 대문자로**</span> 작성하는 표기법입니다.

<span style="background-color:#f1f8ff">**ex) camelCase**</span>

표기법이 낙타의 혹과 비슷하여 카멜(낙타) 표기법이라고 부릅니다.

주로 Java와 Kotlin에서 많이 사용합니다.

### 2. 파스칼 표기법(Pascal Case) 🐫

<span style="background-color:#fff5b1">**카멜 표기법과 비슷하지만, 맨 앞글자를 대문자로**</span> 작성하는 표기법입니다.

<span style="background-color:#f1f8ff">**ex) PascalCase**</span>

이 표기법은 쌍봉낙타 표기법이라고도 부릅니다.

주로 클래스명에 사용됩니다.

### 3. 스네이크 표기법(Snake Case) 🐍

<span style="background-color:#fff5b1">**단어를 연결할 때, 언더바(_)를 사용**</span>하는 표기법입니다.

<span style="background-color:#f1f8ff">**ex) snake_case**</span>

바닥을 기어 다니는 뱀의 모습에서 따온 표기법이라고 합니다.

### 4. 케밥 표기법(Kebab Case) 🍡

<span style="background-color:#fff5b1">**단어를 연결할 때, 하이픈(-)을 사용**</span>하는 표기법입니다.

<span style="background-color:#f1f8ff">**ex) kebab-case**</span>

케밥의 꼬치 모양에서 따온 표기법이라고 합니다.

대부분의 언어가 하이픈을 지원하지 않아 주로 html과 css에서 쓰입니다.

### 5. 헝가리안 표기법(Hungarian Notation)

<span style="background-color:#fff5b1">**앞부분에 자료형을 알아볼 수 있도록 작성**</span>하는 표기법입니다.

<span style="background-color:#f1f8ff">**ex) strCase**</span>

주로 C언어 진영에서 사용했던 이 방식은 자료형을 변경할 경우,

표기까지 모두 수정해야 되기 때문에 요즘은 잘 사용하지 않는다고 합니다.

*~~(예전에 정보처리기사 시험에서 처음 마주하고 이런 표기법도 있냐며 좌절했던 기억이 떠오르네요^^...)~~*

---

<br/>
자! 이렇게 해서 다양한 코딩 표기법에 대해 알아봤습니다.

낙타, 뱀, 꼬치 등 동물이나 음식에서 표기법을 따온 점이 재밌는 것 같네요😝

다음 글에서는 <span style="background-color:#f1f8ff">**코틀린 코딩 컨벤션**</span>에 대해서 소개해 드리도록 하겠습니다.
<br/><br/><br/>
**오류 및 오타 지적, 질문, 인사** 등 무엇이든 언제나 환영입니다!

읽어주셔서 감사합니다.

끝!🦕
<br/>

## 👍 참고

* [카멜, 파스칼, 스네이크, 헝가리안, 케밥 표기법 정리](https://needjarvis.tistory.com/632)
* [코딩 작성시 자주 사용하는 표기법](https://eblo.tistory.com/136)
