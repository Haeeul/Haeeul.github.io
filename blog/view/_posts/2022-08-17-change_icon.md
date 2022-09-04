---
#096
layout: post
title: "[Android] 적응형 앱 아이콘(Adaptive icon) 적용하기"
accent_image:
  background: url(https://user-images.githubusercontent.com/39720852/188318519-8f404e64-0c7d-4bd1-97ac-d37b6dd78360.gif) center/cover
  overlay: true
date: 2022-08-17 14:50:00 +0900
categories: view
tags: [Android, view, icon, Adaptive icon]
---

안녕하세요, 해을입니다🦖

이번 글에서는 <span style="background-color:#fff5b1">**적응형 앱 아이콘 적용 방법**</span>에 대해 알아보겠습니다!

## 💡 적응형 앱 아이콘이란?

적응형 앱 아이콘은 **다양한 디바이스에서 여러 가지 형태로 표시될 수 있도록** Android 8.0(API 수준 26)부터 도입된 아이콘으로,

2개의 레이어와 1개의 마스크를 사용하여 정의합니다.

![2022-09-04 23;25;19](https://user-images.githubusercontent.com/39720852/188318519-8f404e64-0c7d-4bd1-97ac-d37b6dd78360.gif){: width="500"}

출처 developer.android.com
{:.figcaption}

기기마다 원형, 라운드형, 사각형, 모서리가 둥근 사각형 등으로 표시될 수 있으며,

![image](https://user-images.githubusercontent.com/39720852/188319790-baf84e13-a253-4b27-8490-7b9980ad3608.png)

상하좌우, 확대/축소 등 **다양한 시각 효과도 지원**합니다.

![2022-09-04 23;38;36](https://user-images.githubusercontent.com/39720852/188319098-53e6b3fc-3647-46a8-bd2f-aa03177d4bac.gif)

출처 developer.android.com
{:.figcaption}

## 💡 적용하기

### 🥨 이미지 에셋 추가

**res(오른쪽 마우스) -> New -> Image Asset**을 클릭합니다.

![image](https://user-images.githubusercontent.com/39720852/185045208-7c840296-6886-485d-97c7-51b6399b75dc.png)

### 🥨 Icon Type 선택

아이콘 타입은 앱 버전에 따라 선택해야 하며, 이번 글에서는 **적응형 런처 아이콘**을 만들어보겠습니다.

![image](https://user-images.githubusercontent.com/39720852/185045562-24b464a3-9449-4134-95c2-99f58bf62d8a.png)

* **Android 8.0 버전 지원** : 적응형 런처 아이콘 및 레거시 런처 아이콘
* **Android 7.1 이하 버전 지원** : 레거시 런처 아이콘

### 🥨 Layer 설정 - Foreground Layer

앱 아이콘 앞쪽에 깔리게 되는 **Foreground Layer에 로고**를 불러옵니다.

이때 사용하는 로고 타입에 맞게 **Asset Type**을 설정합니다.

![image](https://user-images.githubusercontent.com/39720852/185058621-659dbeba-46e8-423e-9361-5c64458685a0.png)

**Resize** 슬라이더를 사용하여 크기를 조절합니다.  
(Preview 속 동그란 원 안에 들어가야 로고가 잘리지 않습니다)

![image](https://user-images.githubusercontent.com/39720852/185058737-7746b401-8bd9-47d6-94f9-5cc6eea04b39.png)

### 🥨 Layer 설정 - Background Layer

앱 아이콘 뒤쪽에 깔리게 되는 **Background Layer에 배경색**을 지정합니다.

저는 Color Type으로 설정한 후, 검은색 바탕을 설정했습니다.

![image](https://user-images.githubusercontent.com/39720852/185062052-98531483-7d95-4280-9942-dda780f3f50e.png)

### 🥨 이미지명 설정

이미지 명을 확인한 후에 다음으로 넘어갑니다.(저는 디폴트 값을 그대로 사용했습니다)

![image](https://user-images.githubusercontent.com/39720852/185435868-59c3a94d-7d3b-4c7f-87de-19c969e81086.png)

아이콘을 교체하기 위해 기존의 이름을 사용하는 경우, 겹친다는 의미로 빨갛게 표시됩니다.

![image](https://user-images.githubusercontent.com/39720852/185435425-4319b045-64df-439c-826d-95e85878e47e.png)

### 🥨 설정 확인

**Manifest 파일에서 icon명을 확인**한 후, 실행하면 변경된 아이콘을 확인할 수 있습니다.

![image](https://user-images.githubusercontent.com/39720852/185436982-09b51789-6ae7-4906-b165-42bf68404169.png)

![image](https://user-images.githubusercontent.com/39720852/185441015-db900fb6-71dc-49a7-8432-464cce6b3b25.png)

## 💡 느낀 점

이번 경험을 통해 **앱 발전에 따라 아이콘도 다양한 형태로 변화하고 있다는** 것을 깨닫게 되었습니다.

안드로이드 개발자라면 앱에 관련된 모든 것에 관심을 가지는 것이 중요할 것 같네요!

---

자! 이렇게 해서 적응형 앱 아이콘 적용 방법에 대해 알아봤는데요.

글을 읽어주신 분들께 도움이 됐으면 좋겠습니다😊

다음 글에서는 또 다른 유용한 view 관련 방법에 대해 소개해 드리도록 하겠습니다.
<br/><br/><br/>
**오류 및 오타 지적, 질문, 인사** 등 무엇이든 언제나 환영입니다!

읽어주셔서 감사합니다.

끝!🦕
<br/>

## 👍 참고

- [안드로이드 공식 문서](https://developer.android.com/studio/write/image-asset-studio?authuser=1#create-adaptive)
- [[안드로이드 스튜디오] 앱 아이콘 변경하기](https://codenet.tistory.com/29)
