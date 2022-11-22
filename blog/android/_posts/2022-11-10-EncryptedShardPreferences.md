---
#105
layout: post
title: "[Android] EncryptedSharedPreferences를 사용하여 SharedPreferences 암호화하는 방법"
date: 2022-11-10 22:09:00 +0900
categories: android
tags: [Android, SharedPreferences, EncryptedSharedPreferences, Security]
---

안녕하세요, 해을입니다🦖

이번 글에서는 <span style="background-color:#dcffe4">**EncryptedSharedPreferences를 사용하여 SharedPreferences 암호화하는 방법**</span>에 대해 알아보겠습니다!

## 💡 EncryptedSharedPreferences란?

안드로이드에서 간단한 데이터를 저장할 때, **SharedPreferences**를 사용합니다.

그러나 SharedPreferences의 경우, **내용이 그대로 저장되기 때문에 보안이 취약**하다는 단점이 있습니다.

이에 구글에서는 SharedPreferences를 암호화하여 쉽게 사용할 수 있도록 **Security 라이브러리(EncryptedSharedPreferences)**를 제공하고 있습니다.

Security는 Android SDK 23 (6.0) 이상부터 사용 가능하며, 마스터키를 만들어 사용합니다.

## 💡 EncryptedSharedPreferences 사용하기

### 🥨 라이브러리 추가

**app/build.gradle**에 Security 라이브러리를 추가합니다.

```kotlin
implementation "androidx.security:security-crypto:1.0.0-alpha02"
```

### 🥨 암호화에 사용할 마스터키 생성

**MasterKey 클래스**를 통해 암호화에 사용할 **마스터키**를 생성합니다.

```kotlin
val masterKey = MasterKey.Builder(context).setKeySchem(MasterKey.KeyScheme.AES256_GCM).build()
```

키를 생성하는 알고리즘은 공식 문서에서 사용하는 AES256_GCM를 그대로 사용했으나 커스텀 하여 적용 가능합니다.

### 🥨 객체 생성

**EncryptedSharedPreferences를** 사용하여 **SharedPreferences 인스턴스를 생성**합니다.

이때 데이터가 저장될 **xml 파일명**과 미리 생성한 **마스터키**, **Key/Value 저장에 사용할 암호화 방식**을 지정합니다.

마스터키 생성 때와 마찬가지로 공식 문서를 따라 Key 암호화 방식은 AES256_SIV, Value 암호화 방식은 AES256_GCM를 사용했습니다.

```kotlin
var sharedPreferences: SharedPreferences = EncryptedSharedPreferences.create(
        context,
        "secret_shared_prefs", // 파일명
        masterKey, // 생성한 마스터키
        EncryptedSharedPreferences.PrefKeyEncryptionScheme.AES256_SIV, // Key 암호화 방식
        EncryptedSharedPreferences.PrefValueEncryptionScheme.AES256_GCM // Value 암호화 방식
    )
```

### 🥨 데이터 읽기/쓰기

데이터의 읽고 쓰기는 sharedPreferences를 사용하던 방법 그대로 사용하면 됩니다.

```kotlin
var userNickname: String
        get() = sharedPreferences.getString(USER_NICKNAME)
        set(value) = sharedPreferences.putString(USER_NICKNAME, value)
```

### 🥨 저장된 데이터 확인(내부 저장소 확인)

**Device File Explorer**를 사용하여 내부 저장소에 접근한 뒤, 저장된 데이터를 확인해 보겠습니다.

1. 애뮬레이터 또는 실제 기기를 연결하여 앱을 실행합니다.

2. Shift 키를 2번 눌러 검색창이 실행되면 Device File Explorer를 입력합니다.

    ![image](https://user-images.githubusercontent.com/39720852/203227071-5531327c-5f55-49fd-ad7a-4fd6573c7d01.png)

3. 내부 저장소 경로(**/data/data/package명/shared_prefs**)를 찾아 접근합니다.

    ![image](https://user-images.githubusercontent.com/39720852/203227823-65325dc6-6501-48aa-a0f5-50bb212940a6.png)

    이때 1번 내용대로 앱을 실행하지 않을 경우, 파일이 표시되지 않습니다.

    ![image](https://user-images.githubusercontent.com/39720852/203227307-9eaec66d-3be2-4d94-a9cd-88c9cc85954b.png)

4. xml 파일을 열어 저장된 데이터를 확인합니다.

    기존의 sharedPreferences 파일을 살펴보면 Key와 Value 값이 모두 그대로 저장되어 있지만,

    ![image](https://user-images.githubusercontent.com/39720852/203229281-1dcc1f52-1b89-401e-b963-9176cc2fee5a.png)

    새로 생성된 파일을 살펴보면 Key와 Value 값에 암호화가 적용된 것을 확인할 수 있습니다.

    ![image](https://user-images.githubusercontent.com/39720852/203229318-2929fafd-57d9-4afd-b723-85f5040ea67a.png)

## 💡 느낀 점

앱 출시를 준비하며 처음으로 **데이터 암호화**에 대해 고민하고 실제 적용까지 해볼 수 있었습니다.

이를 통해 **개인 정보 및 보안의 중요성**을 다시 한번 깨닫게 되었고

구글에서 **보안 관련 라이브러리**를 제공한다는 사실을 새롭게 알 수 있었던 좋은 경험이었습니다.

---

.

자! 이렇게 해서 EncryptedSharedPreferences를 사용하여 SharedPreferences를 암호화하는 방법에 대해 알아봤는데요.

글을 읽어주신 분들께 도움이 됐으면 좋겠습니다😊

다음 글에서는 또 다른 android 관련 내용에 대해 소개해 드리도록 하겠습니다.
<br/><br/><br/>
**오류 및 오타 지적, 질문, 인사** 등 무엇이든 언제나 환영입니다!

읽어주셔서 감사합니다.

끝!🦕
<br/>

## 👍 참고

- [안드로이드 공식 문서](https://developer.android.com/reference/kotlin/androidx/security/crypto/EncryptedSharedPreferences?hl=ko)
- [[kotlin] android EncryptedSharedPreferences example](https://shary1012.tistory.com/223)
- [SharedPreferences / EncryptedSharedPreferences](https://philosopher-chan.tistory.com/1557)
- [EncryptedSharedPreferences로 데이터 암호화하기](https://cliearl.github.io/posts/android/encrypted-sharedpreferences/)
