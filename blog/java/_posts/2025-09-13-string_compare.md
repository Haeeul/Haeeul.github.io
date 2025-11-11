---
#120
layout: post
title: "[JAVA] String / StringBuffer / StringBuilder 비교"
date: 2025-09-13 11:00:00 +0900
categories: java
tags: [Java, String, StringBuffer, SringBuilder]
# related_posts:
  # - /blog/algorithm/bronze-v/2022-04-01-Q1000/
  # - /blog/algorithm/bronze-v/2022-04-01-Q1001/
---

안녕하세요, 해을입니다🦖

이번 글에서는 <span style="background-color:#f1f8ff">**자바의 String / StringBuffer / StringBuilder**</span>에 대해 알아보겠습니다!

위 세 가지 클래스는 모두 문자열을 다루는 클래스이지만, **불변 여부 / 동기화 지원 / 성능 특성**에서 차이가 있습니다.

이번 포스팅에서는 각각의 특징과 차이를 비교하며 어떤 상황에서 어떤 클래스를 사용하는 게 좋은지 알아보겠습니다.

* toc
{:toc}


## 💡정의

### 🥨 String

- 문자열을 나타내는 대표적인 클래스

- 가장 많이 사용되지만, **불변(Immutable)** 특성을 가지고 있어 문자열 변경 시 주의가 필요

- (참고) : [[JAVA] String 클래스](https://haeeul.github.io/blog/java/2025-08-16-java_string/)

### 🥨 StringBuffer / StringBuilder

- 문자열을 **추가, 변경, 삭제 등 연산이 빈번할 때** 사용하는 클래스

- `String`으로도 연산이 가능하지만, 문자열 변경 시마다 새로운 객체를 생성하기 때문에 메모리 낭비와 성능 저하가 발생

- 이를 해결하기 위해 자바는 **가변(Mutable)** 구조의 `StringBuffer`와 `StringBuilder`를 제공

- 두 클래스의 사용법은 동일하지만, **동기화(Synchronization) 지원 여부**에서 차이가 있음

## 💡String / StringBuffer / StringBuilder 비교

### 🥨 String : 불변(Immutable)

- **값 변경 불가** : `String`은 한 번 생성되면 내부의 값이 변하지 않는 '불변' 자료형

```java
String str = "java";  // "java"
str.toUpperCase();  // "JAVA"

System.out.println(str); // "java" (불변)
```

- **새로운 객체 생성** : 문자열을 수정하면 기존 객체를 변경하는 것이 아니라 새로운 객체가 생성

```java
String str = "hello";
str = str + " java";

System.out.println(str);  // "hello java" (새 객체 생성)
```


#### 🍀 장점

- **메모리 효율** : String Constant Pool을 활용하여 중복(같은 값의 문자열) 문자열을 공유하여 메모리 사용량을 최적화

- **안정성** : 값이 변하지 않아 멀티스레드 환경에서 안전

#### 🍀 단점

- **성능 저하** : 문자열 변경 연산이 많을 경우 비효율적 (불필요한 객체 다수 생성)


### 🥨 StringBuffer / StringBuilder : 가변(Mutable)

- **가변성** : String과 달리 새로운 문자열을 만들지 않고 기존 객체 내에서 문자열 수정 가능

```java
StringBuffer sb = new StringBuffer("hello");
sb.append("java");

System.out.println(str); // "hello java" (같은 객체 내 수정)
```

#### 🍀 장점

- **높은 성능** : `String`보다 훨씬 빠른 성능

#### 🍀 단점

- 내부 버퍼 확장 등 추가 연산이 발생할 수 있어 **간단한 문자열 조합에는 오히려 비효율**적일 수 있음

## 💡StringBuffer VS StringBuilder 차이점

두 클래스는 문법이나 배열 구성도 모두 같지만 **동기화 지원 유무**가 다릅니다.

멀티 스레드 예제를 통해 자세하게 살펴보겠습니다.

| 클래스 | 동기화(Synchronization) | 스레드 안전성(Thread-safe) | 권장 사용 환경 |
|:--|:--:|:--:|:--|
| **StringBuffer** | ✅ 지원 | ✅ 안전 | 멀티스레드 환경 |
| **StringBuilder** | ❌ 미지원 | ❌ 안전하지 않음 | 단일 스레드 환경 |

```java
public class Main {
    public static void main(String[] args) {
        StringBuffer stringBuffer = new StringBuffer();
        StringBuilder stringBuilder = new StringBuilder();

        // 첫 번째 스레드
        Thread t1 = new Thread(() -> {
            for (int i = 0; i < 1000; i++) {
                safeBuffer.append("A");
                stringBuilder.append("A");
            }
        });

        // 두 번째 스레드
        Thread t2 = new Thread(() -> {
            for (int i = 0; i < 1000; i++) {
                safeBuffer.append("B");
                stringBuilder.append("B");
            }
        });

        // 결과 확인 스레드
        Thread observer = new Thread(() -> {
            try {
                Thread.sleep(2000);
                System.out.println("StringBuffer length: " + safeBuffer.length());
                System.out.println("StringBuilder length: " + stringBuilder.length());
            } catch (InterruptedException e) {
                e.printStackTrace();
            }
        });

        // 스레드 시작
        t1.start();
        t2.start();
        observer.start();
    }
}
```
```
StringBuffer length: 2000
StringBuilder length: 1819
```

결과값을 보면 StringBuilder의 값이 더 작은 것을 확인할 수 있는데요.

- **StringBuilder**(동기화 지원 ❌) : **여러 스레드가 동시에 접근하면 일부 데이터가 손실**될 수 있음

- **StringBuffer**(동기화 처리 ✅) : **안정적인 결과를 보장**

=> 따라서 소켓환경과 같이 **비동기로 동작하는 경우가 많을 때는 StringBuffer를 사용하는 것이 안전**합니다.

## 💡전체 성능 비교

출력 예제를 통해 3가지 클래스의 전체 성능을 비교해 보겠습니다.

```java
public class ComparePerformance {
    public static void main(String[] args) {
        final int LENGTH = 500000;

        // (1) String
        long start1 = System.currentTimeMillis();
        String str = "";
        for (int i = 0; i < LENGTH; i++) {
            str += "A";
        }
        long end1 = System.currentTimeMillis();

        // (2) StringBuffer
        long start2 = System.currentTimeMillis();
        StringBuffer sbf = new StringBuffer();
        for (int i = 0; i < LENGTH; i++) {
            sbf.append("A");
        }
        long end2 = System.currentTimeMillis();

        // (3) StringBuilder
        long start3 = System.currentTimeMillis();
        StringBuilder sbd = new StringBuilder();
        for (int i = 0; i < LENGTH; i++) {
            sbd.append("A");
        }
        long end3 = System.currentTimeMillis();

        // 결과 출력
        System.out.println("String (+ 연산) : " + (end1 - start1) + "ms");
        System.out.println("StringBuffer (append) : " + (end2 - start2) + "ms");
        System.out.println("StringBuilder (append) : " + (end3 - start3) + "ms");
    }
}
```

```
String (+ 연산) : 13431ms
StringBuffer (append) : 10ms
StringBuilder (append) : 3ms
```

StringBuilder는 동기화를 고려하지 않기 때문에 StringBuffer보다 조금 더 빠른 속도를 보입니다.

**멀티스레드 환경이 아니라면 StringBuilder를 사용하는 것이 효율적**입니다.

## 💡최종 정리

| 구분 | 불변성 | 동기화 | 스레드 안전성 | 속도 | 주요 사용 환경 |
|:--|:--:|:--:|:--:|:--:|:--|
| **String** | 불변 (Immutable) | ❌ | ✅ 안전 | 🐢 느림 | 변경이 적은 문자열 |
| **StringBuffer** | 가변 (Mutable) | ✅ | ✅ 안전 | ⚡ 중간 | 멀티스레드 환경 |
| **StringBuilder** | 가변 (Mutable) | ❌ | ❌ 안전하지 않음 | 🚀 빠름 | 단일 스레드 환경 |

- 문자열 변경이 거의 없다면 → `String`

- 멀티스레드 환경이라면 → `StringBuffer`

- 단일 스레드 환경 또는 성능이 중요하다면 → `StringBuilder`

---
<br/>
읽어주셔서 감사합니다.

오타나 내용 오류가 있다면 언제든 댓글로 알려주세요!

끝🦕
<br/>

## 👍 참고

* [[점프 투 자바] 03-05 StringBuffer](https://wikidocs.net/276)
* [자바 String / StringBuffer / StringBuilder 차이점 & 성능 비교](https://inpa.tistory.com/entry/JAVA-%E2%98%95-String-StringBuffer-StringBuilder-%EC%B0%A8%EC%9D%B4%EC%A0%90-%EC%84%B1%EB%8A%A5-%EB%B9%84%EA%B5%90)
