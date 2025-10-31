---
#119
layout: post
title: "[JAVA] String 클래스"
date: 2025-08-16 16:00:00 +0900
categories: java
tags: [Java, String]
# related_posts:
  # - /blog/algorithm/bronze-v/2022-04-01-Q1000/
  # - /blog/algorithm/bronze-v/2022-04-01-Q1001/
---

안녕하세요, 해을입니다🦖

이번 글에서는 <span style="background-color:#f1f8ff">**자바의 String 클래스**</span>에 대해 알아보겠습니다!

* toc
{:toc}

## 💡String 클래스란?

String은 **문자열을 나타내는 자료형 클래스**로, 아래와 같이 2가지 방식으로 사용 가능합니다.

```java
// 리터럴(literal) 선언
String str1 = "Hello World";
String str2 = "a";

// new 키워드 선언
String str3 = new String("Hello World");
String str4 = new String("a");
```

## 💡내장 함수 살펴보기

### 🥨 equals

2개 문자열의 **내용이 서로 같은지 비교**하여 boolean 값 반환

```java
String str1 = "hello";
String str2 = "world";
String str3 = "hello";
System.out.println(str1.equals(str2)); // false 출력
System.out.println(str1.equals(str3)); // true 출력
```

<details>
<summary>(주의) 문자열 내용을 비교할 때 '== 연산자'가 아닌 'equals() 메서드'를 사용해야되는 이유?</summary>
<div markdown="1">

 - `== 연산자` : 두 문자열의 **주소(참조)값을 비교**
 - `equals() 메서드` : 두 문자열의 **내용을 비교**

> 문자열은 내용이 같더라도 선언 방식에 따라 주소(참조)값이 달라지기 때문에  
> 주소값을 비교하는 `== 연산자` 사용시 원하는 결과와 다른 결과가 나올 수 있음 

 </div>
</details>

<details>
<summary>(참고) 선언 방식에 따라 달라지는 주소(참조)값</summary>
<div markdown="1">

🍀 **리터럴(literal)** 선언 : **주소(참조)값 같음**

리터럴의 경우, 자바 컴파일러는 String Constant Pool 영역에 **같은 값의 문자열을 공유하여 메모리 사용량을 최적화** 하기 때문에 str1과 str2의 **주소 값은 같습니다.**

```java
String str1 = "Hello World";
String str2 = "Hello World";
```

🍀 **new 키워드** 선언 : **주소(참조)값 다름**

new 키워드의 경우, **항상 새로운 객체를 생성**하여 Heap 영역에 저장하기 때문에 **다른 주소값을 할당 받게** 됩니다. 따라서 str1과 str3의 주소값은 다르며, str3과 str4의 주소값 역시 다릅니다.

```java
String str3 = new String("Hello World");
String str4 = new String("Hello World");
```

</div>
</details>

#### 🥨 indexOf

**특정 문자열이 시작되는 위치**, 즉 인덱스값을 반환

만약, 찾는 문자열이 **존재하지 않을 경우 -1 반환**

```java
String str = "Hello World";
System.out.println(str.indexOf("World"));  // 6 출력 : index는 0부터 시작하므로
System.out.println(str.indexOf("Java"));  // -1 출력
```

#### 🥨 contains

**특정 문자열의 포함 여부**를 반환

```java
String str = "Hello World";
System.out.println(str.contains("World"));  // true 출력
System.out.println(str.contains("Java"));  // false 출력
```

#### 🥨 charAt

**특정 위치의 문자**를 반환

```java
String str = "Hello World";
System.out.println(str.charAt(6));  // "W" 출력
```

#### 🥨 replaceAll

특정 문자열을 **다른 문자열로 변경**

```java
String str = "Hello World";
System.out.println(str.replaceAll("World","Java"));  // "Hello Java" 출력
```

#### 🥨 substring

시작 위치부터 끝 위치 바로 앞까지의 **문자열을 추출**

*(주의) 끝 위치 문자는 미포함

```java
String str = "Hello World";
System.out.println(str.substring(0,4));  // "Hell" 출력
```

#### 🥨 toUpperCase

문자열을 **모두 대문자로 변경**

```java
String str = "Hello World";
System.out.println(str.toUpperCase());  // "HELLO WORLD" 출력
```

#### 🥨 toLowerCase

문자열을 **모두 소문자로 변경**

```java
String str = "Hello World";
System.out.println(str.toLowerCase());  // "hello world" 출력
```

#### 🥨 split

문자열을 **특정 구분자로 나눠 문자열 배열로 반환**

```java
String str = "j:a:v:a";
String[] result = str.split(":");  // result는 {"j", "a", "v", "a"}
```

---
<br/>
**오류 및 오타 등 피드백, 질문, 인사** 등 무엇이든 언제나 환영입니다!

읽어주셔서 감사합니다.

끝!🦕
<br/>

## 👍 참고

* [[Java] 문자열(String) 비교 방법 ==, equals() 차이](https://milku.tistory.com/112)
* [[점프 투 자바] 03-04 문자열](https://wikidocs.net/205)
