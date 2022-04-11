---
#015
layout: post
title: "[JAVA] Scanner 클래스"
date: 2022-04-01 09:41:00 +0900
categories: java
tags: [Java, Scanner]
related_posts:
  - /blog/algorithm/bronze-v/2022-04-01-Q1000/
---

안녕하세요, 해을입니다🦖

이번 글에서는 <span style="background-color:#f1f8ff">**자바의 Scanner 클래스**</span>에 대해 알아보겠습니다!

* toc
{:toc}

## 💡Scanner 클래스

Scanner 클래스는 **사용자로부터 입력을 받기 위한 입력 스트림**입니다.

### 🥨 특징

* **패키지 포함 필수**  
   ![image](https://user-images.githubusercontent.com/39720852/162229725-28a3fd69-e6fb-4c8b-b64f-3923f506f916.png)  
   Scanner는 java.util 패키지에 있으며 사용 시, 패키지를 포함해야 합니다.

* **다양한 메서드**
   ![image](https://user-images.githubusercontent.com/39720852/162230968-2214f7b6-8a87-44a9-a3cd-a198b72c8196.png)  
   메서드를 사용하여 String, int, boolean 등 **다양한 데이터 타입**을 입력받을 수 있습니다.

* **토큰 단위로 입력을 구분**  
  **공백과 개행**(' ', '\t', '\n' 등)을 기준으로 입력을 읽습니다.

### 🥨 사용해보기

``` java
import java.util.Scanner; // 패키지 포함

public class test {
 public static void main(String[] args) {
  Scanner stdIn = new Scanner(System.in); // 객체 생성
  
  // 타입별 입력 및 리턴
  int x = stdIn.nextInt();
   
  String str1 = stdIn.next(); // 공백을 기준으로 한 단어를 읽음
  String str2 = stdIn.nextLine(); // 개행을 기준으로 한 줄을 읽음
  
  System.out.println(x + std1 + std2);
 }
}
```

1. **패키지 포함**  
  ```java
  import java.util.Scanner; // 패키지 포함
  ```
  Scanner 클래스는 사용 시에 **프로그램 상단에서 패키지를 포함**시켜야 합니다.  
2. **객체 생성**
  ```java
  Scanner stdIn = new Scanner(System.in); // 객체 생성
  ```
  키보드 값을 입력받는 메서드를 사용하기 전에 **객체를 먼저 생성**해야 합니다.  
  * System.in : 키보드와 연결된 표준 입력 스트림
  * stdIn : 표준 입력 스트림에서 입력 값을 꺼내는 역할
3. **입력 받기**  
  ```java
  // int 형
  int x = stdIn.nextInt();
  // String 형
  String str1 = stdIn.next();
  String str2 = stdIn.nextLine();
  ```
  [ next~ ] 형식의 다양한 **입력 메서드를 사용**하여 입력을 받습니다.

### 🥨 주의사항

next()와 nextLine()은 같은 String 형을 읽는 메서드지만 읽는 방식에서 차이가 있습니다.

![image](https://user-images.githubusercontent.com/39720852/162766390-e438b371-8b3b-48dc-8cfb-88de4d7d937d.png)

* **next()** : **토큰**을 기준으로 **한 단어**를 읽음
* **nextLine()** : **엔터**를 기준으로 **한 줄**을 읽음

![image](https://user-images.githubusercontent.com/39720852/162768566-3d51b2b8-23d3-4366-99b6-c88aaa0a69a2.png)

또 다른 예시를 살펴보면 위 경우는 **next()가 공백 전까지** 읽고난 후, **공백부터 nextLine()**이 읽기 시작하므로 사진처럼 출력되는 것입니다.

이렇게 2가지 메서드를 같이 쓰는 경우, 위와 같은 상황이 일어날 수 있기 때문에 주의해서 사용해야 합니다.

---

**오류 및 오타 지적, 질문, 인사** 등 무엇이든 언제나 환영입니다!

읽어주셔서 감사합니다.

끝!🦕
<br/>

## 👍 참고

* [Java 공식문서](https://docs.oracle.com/javase/9/docs/api/java/util/Scanner.html)
* [[Java] Scanner() 메서드 총정리](https://velog.io/@cse_pebb/Java-Scanner-%EB%A9%94%EC%84%9C%EB%93%9C-%EC%B4%9D%EC%A0%95%EB%A6%AC)
* [자바 [JAVA] - 스캐너(Scanner) 클래스와 입력](https://st-lab.tistory.com/92)
