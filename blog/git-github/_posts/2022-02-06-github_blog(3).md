---
layout: post
title: "GitHub 블로그 만들기 (3) - Jekyll 테마 적용"
image: https://user-images.githubusercontent.com/39720852/153595323-25bae3b4-5715-4911-b5cd-fa873dd99c4e.png
accent_image:
  background: url(https://user-images.githubusercontent.com/39720852/152405232-29b296d1-653c-4505-ad3c-07fd5a680d17.png) center/cover
  overlay: true
date: 2022-02-06 19:38:00 +0900
categories: git-github
tags: [GitHub Pages, GitHub blog, Jekyll, Jekyll theme]
description: >
  🎨 GitHub 블로그에 테마를 적용해 봅니다.
related_posts:
  - /blog/git-github/2022-02-05-github_blog(2)/
  - /blog/git-github/2022-02-07-github_blog(4)/
  - /blog/git-github/2022-02-08-github_blog(5)/
---

안녕하세요, 해을입니다🦖

아직은 어디 내놓기에 너무나도 초라한 GitHub 블로그를 Jekyll을 사용하여 간Zl나게 꾸며볼건데요😏

이번 글에서는 <span style="background-color:#f1f8ff">**Jekyll 테마 적용**</span>에 대해 알아보겠습니다!

* toc
{:toc}

실습 표시 : 🥨  
(🥨 표시는 실습 부분임을 뜻합니다)

## 💡Jekyll 테마 결정

이전 글에서 말씀드렸다시피 Jekyll에는 무료로 제공되는 테마가 굉장히 많습니다.

또한 테마 검색 사이트도 무척 다양한데, 제공되는 테마는 거의 비슷하고 사이트의 구성만 다른 느낌입니다.

* [https://jekyllthemes.io/free](https://jekyllthemes.io/free)
* [https://jekyll-themes.com/free/](https://jekyll-themes.com/free/)
* [http://themes.jekyllrc.org/](http://themes.jekyllrc.org/)

검색이 편리한 곳에서 **반응형, 가독성, 지원 기능 등 자신만의 기준대로 테마를 결정**하시면 됩니다.

결정이 어려우시다면 테마 추천글도 많이 있으니 참고하시면 좋을 것 같습니다.

저는 여러 추천 테마 중에서 고민 끝에 효과와 호환성이 뛰어난 [Hydejack 테마](https://github.com/hydecorp/hydejack)로 결정했습니다.

![GitHub블로그3-데모](https://user-images.githubusercontent.com/39720852/153604849-db3c4919-34b4-40b2-8ff1-1a73320fd72f.gif)

[Hydejack 데모 사이트](https://hydejack.com/)
{:.figcaption}

## 💡Jekyll 테마 적용

### 1. 테마 소스 파일 다운로드

🥨 결정한 테마의 **GitHub 저장소에서 다운로드** 받습니다.

![GitHub블로그3-소스파일다운](https://user-images.githubusercontent.com/39720852/153533421-c3975b9c-43a1-433e-8dcf-220447cbf714.png)

검색 사이트에서 바로 다운로드 가능하지만, 제 경험담을 말씀드리면 <span style="background-color:#ffdce0">**파일이 누락되는 경우**</span>가 있습니다,,,

안전하게(?) GitHub 저장소에서 다운로드하는 것을 추천드려요,,,

### 2. 다운로드 파일 복사

🥨 파일은 압축을 풀고 **전체 복사**합니다.

![GitHub블로그3-파일복사](https://user-images.githubusercontent.com/39720852/153534679-c443607e-8172-4769-b538-e7bafffb1bbb.png)

### 3. 자신의 블로그 폴더에 붙여넣기

🥨 자신의 **블로그 폴더에 붙여넣기**한 후, 이름이 같은 파일은 **덮어쓰기** 합니다.

![GitHub블로그3-블로그폴더](https://user-images.githubusercontent.com/39720852/153535154-95e324e4-4ed8-4c5f-8f83-96b7c3078aec.png)

![GitHub블로그3-붙여넣기](https://user-images.githubusercontent.com/39720852/153534786-074883cd-568f-4355-a164-717fc7c62df2.png)

### 4. bundle 설치

🥨 터미널을 실행하고 아래 명령어를 사용하여 **bundle을 설치**합니다.

```
bundle install
```

![GitHub블로그3-bundle설치](https://user-images.githubusercontent.com/39720852/153535629-ee79b12b-81fd-402e-bab0-73307e7e9a1a.png)

### 5. 로컬 서버 확인

🥨 브라우저에서 **로컬 서버를 확인**해 봅니다.

```
bundle exec jekyll serve

// 에러 발생할 경우(이전 게시글 참고)
bundle exec jekyll serve --trace
```

![GitHub블로그3-테마적용확인](https://user-images.githubusercontent.com/39720852/153536473-5d37c88e-996b-477a-a840-55ec656be3c0.gif)

### 6. (선택) commit/push

🥨 원격 저장소에 push하면 username.github.io 주소에 반영됩니다.

```
git add --all

git commit -m "Jekyll 설치"

git push -u origin main
```

지금 commit/push 하셔도 좋고 커스텀까지 한 이후에 하셔도 괜찮습니다.

---

<br/>
자! 이렇게 해서 Github 블로그에 테마를 적용해 봤습니다.

커스텀 할 생각에 조금 신나는 기분이네요😝

다음 글에서는 <span style="background-color:#f1f8ff">**블로그 커스텀**</span>에 대해서 소개해 드리도록 하겠습니다.
<br/><br/><br/>
**오류 및 오타 지적, 질문, 인사** 등 무엇이든 언제나 환영입니다!

읽어주셔서 감사합니다.

끝!🦕
<br/><br/><br/>
🔗 다음 글 바로가기 [GitHub 블로그 만들기 (4) - 블로그 커스텀](/blog/git-github/2022-02-07-github_blog(4))

## 👍 참고

* [왕초보를 위한 Github 블로그 만들기(2)](https://zeddios.tistory.com/1223?category=682196)
* [[GithubPages] 하루만에 만드는 깃허브 블로그-02.시작하기](https://khw11044.github.io/blog/githubpages/2020-12-26-making-blog-02/)