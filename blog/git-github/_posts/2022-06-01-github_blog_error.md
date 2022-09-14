---
#071
layout: post
title: "GitHub 블로그 만들기(9) - build error"
image: https://user-images.githubusercontent.com/39720852/190166671-9cd79a21-8f14-4e17-8d41-78d6e2dd9405.png
accent_image:
  background: url(https://user-images.githubusercontent.com/39720852/152405232-29b296d1-653c-4505-ad3c-07fd5a680d17.png) center/cover
  overlay: true
date: 2022-09-14 22:01:00 +0900
categories: git-github
tags: [GitHub Pages, GitHub blog, Jekyll, Jekyll theme, error]
description: >
  📝 GitHub 블로그의 build error를 해결합니다.
related_posts:
  - /blog/git-github/2022-02-08-github_blog(6)/
  - /blog/git-github/2022-02-09-github_blog(7)/
  - /blog/git-github/2022-02-10-github_blog(8)/
---

안녕하세요, 해을입니다🦖

이번 글에서는 <span style="background-color:#f1f8ff">**GitHub 블로그 build error**</span>에 대해 알아보겠습니다!

* toc
{:toc}

## 💡error 확인

블로그에 업로드가 반영되지 않아 commit 기록을 확인해 보니 에러가 발생하고 있었습니다.

로그를 살펴본 결과, 테마 관련 에러임을 확인할 수 있었습니다.

![image](https://user-images.githubusercontent.com/39720852/190166847-bf1c8073-6fc1-4134-ae3b-f56c31f55eae.png)

![image](https://user-images.githubusercontent.com/39720852/190166546-3f05367c-73e7-420a-bc09-9b8b070f0315.png)

```
Configuration file: /github/workspace/./_config.yml
             Theme: jekyll-theme-hydejack
github-pages 227 | Error:  The jekyll-theme-hydejack theme could not be found.
```

## 💡해결하기

### 🥨 config 테마 설정

![image](https://user-images.githubusercontent.com/39720852/190167843-d9622695-8c1a-4164-9022-18f9f6375169.png)


해결 방법은 간단합니다.

**_config.yml 파일의 Theme 쪽에 있는 theme는 주석 처리, remote_theme는 주석 해제**하면 됩니다.

---

자! 이렇게 해서 Github 블로그의 build error를 해결해 봤습니다.

다음 글에서는 새로운 기능을 추가하게 되면 소개해 드리도록 하겠습니다.
<br/><br/><br/>
**오류 및 오타 지적, 질문, 인사** 등 무엇이든 언제나 환영입니다!

읽어주셔서 감사합니다.

끝!🦕