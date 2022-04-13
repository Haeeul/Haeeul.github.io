---
#019
layout: post
title: "[JAVA] BigInteger 클래스"
date: 2022-04-02 15:07:00 +0900
categories: java
tags: [Java, BigInteger]
related_posts:
  - /blog/algorithm/bronze-v/2022-04-01-Q1271/
  - /blog/algorithm/bronze-v/2022-04-02-Q2338/
---

안녕하세요, 해을입니다🦖

이번 글에서는 <span style="background-color:#f1f8ff">**자바의 BigInteger 클래스**</span>에 대해 알아보겠습니다!

* toc
{:toc}

## 💡 BigInteger 클래스

BigInteger는 **매우 큰 정수를 사용하기 위한 클래스**입니다.

정수형의 기본 자료형인 int, long의 범위를 넘어가는 큰 정수를 표현할 때 사용합니다.

### 🥨 특징

* **패키지 포함 필수**  
   ![image](https://user-images.githubusercontent.com/39720852/162801043-13aeee45-49ce-4e81-9036-f6b57c959a0c.png)  
   BigInteger는 java.math 패키지에 있으며 사용 시, 패키지를 포함해야 합니다.

* **다양한 메서드**
   ![image](https://user-images.githubusercontent.com/39720852/162801335-bb6d22d8-6834-4cc0-940d-3b6b67eaaaf8.png)  
   메서드를 사용하여 간편하게 연산을 진행할 수 있습니다.

* **문자열 형태**  
  long 형을 넘어가는 범위의 값을 표현하기 위해 BigInteger는 문자열 형태로 이루어져 있습니다.

### 🥨 생성자

```java
import java.math.BigInteger;

public class Main {
 public static void main(String[] args) {
    // 문자열 생성자
    BigInteger bigInt = new BigInteger("123123123123123");

    // 진법 생성자
    BigInteger radixBigInt = new BigInteger("1234", 8); // 8진법 1234를 10진법으로 변환
 }
}
```

* **BigInteger(String val)**  
  : long 형을 넘어가는 범위를 표현하기 위해 String으로 생성합니다.
  
* **BigInteger(String val, int radix)**  
  : 해당 진법의 수를 10진법으로 변환합니다.

### 🥨 형변환

```java
import java.math.BigInteger;

public class Main {
 public static void main(String[] args) {
    BigInteger radixBigInt = new BigInteger("1234", 8);

    // 형변환
    int intBigNum = radixBigInt.intValue();

    long longBigNum = radixBigInt.longValue();

    float floatBigNum = radixBigInt.floatValue();

    double doubleBigNum = radixBigInt.doubleValue();
 }
}
```

* **BigInteger.intValue()**

* **BigInteger.longValue()**

* **BigInteger.floatValue()**

* **BigInteger.doubleValue()**
  : BigInteger를 해당 자료형으로 형변환합니다.

### 🥨 사칙연산

```java
import java.math.BigInteger;

public class Main {
 public static void main(String[] args) {
    BigInteger bigInt = new BigInteger("123123123123123");
    BigInteger radixBigInt = new BigInteger("1234", 8);

    // 더하기
    bigInt.add(radixBigInt);

     // 빼기
    bigInt.subtract(radixBigInt);

     // 곱하기
    bigInt.multiply(radixBigInt);

     // 나누기
    bigInt.divide(radixBigInt);
 }
}
```

* **BigInteger.add(BigInteger val)**

* **BigInteger.longValue(BigInteger val)**

* **BigInteger.floatValue(BigInteger val)**

* **BigInteger.doubleValue(BigInteger val)**
  : BigInteger 값을 사용하여 더하기, 빼기, 곱하기, 나누기 합니다.

### 🥨 그 외

```java
import java.math.BigInteger;

public class Main {
 public static void main(String[] args) {
    BigInteger bigInt = new BigInteger("123123123123123");
    BigInteger radixBigInt = new BigInteger("1234", 8);

    // 나머지
    bigInt.remainder(radixBigInt);

     // 최대, 최소
    bigInt.max(radixBigInt);

    bigInt.min(radixBigInt);

     // 비교
    bigInt.compareTo(radixBigInt);
 }
}
```

[나머지[]
* **BigInteger.remainder(BigInteger val)**
  : % 연산 즉, 나머지를 구합니다.

[최대,최소]
* **BigInteger.max(BigInteger val)**
  : 2개 중 큰 값을 반환합니다.

* **BigInteger.min(BigInteger val)**
  : 2개 중 작은 값을 반환합니다.

[비교]
* **BigInteger.compareTo(BigInteger val)**
  : 2개의 값을 비교합니다. (앞이 크면 : 1, 같으면 : 0, 작으면 : -1)

---

자! 이렇게 해서 **Java의 BigInteger 클래스**를 살펴봤습니다.

앞으로는 정수의 범위를 고려하여 그에 맞는 자료형을 잘 사용해야겠네요😊

글에서 소개한 주요 메서드 및 더욱 자세한 내용은 공식 문서에서 확인 가능합니다.
<br/><br/><br/>
**오류 및 오타 지적, 질문, 인사** 등 무엇이든 언제나 환영입니다!

읽어주셔서 감사합니다.

끝!🦕
<br/>

## 👍 참고

* [Java 공식 문서](https://docs.oracle.com/javase/9/docs/api/java/math/BigInteger.html)
* [자바 BigInteger: 매우 큰 정수 표현](https://madplay.github.io/post/biginteger-in-java)
* [[Java] BigInteger Class](https://velog.io/@gillog/Java-BigInteger-Class)
* [[JAVA] #28 BigInteger 클래스 정리](https://travelbeeee.tistory.com/465)
