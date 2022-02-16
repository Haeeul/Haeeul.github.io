---
layout: post
title: "GitHub 블로그 만들기 (2) - Jekyll 설치"
image: https://user-images.githubusercontent.com/39720852/153006263-fa7a3d15-69b6-455a-a540-e7964fd951b9.png
accent_image:
  background: url(https://user-images.githubusercontent.com/39720852/152405232-29b296d1-653c-4505-ad3c-07fd5a680d17.png) center/cover
  overlay: true
date: 2022-02-05 22:20:00 +0900
categories: git-github
tags: [GitHub Pages, GitHub blog, Jekyll]
description: >
  🧪 Jekyll에 대해 알아보고 설치해 봅니다.
related_posts:
  - /blog/git-github/2022-02-04-github_blog(1)/
  - /blog/git-github/2022-02-06-github_blog(3)/
---

안녕하세요, 해을입니다🦖

이번 글에서는 <span style="background-color:#f1f8ff">**Jekyll 설치**</span>에 대해 알아보겠습니다!

* toc
{:toc}

실습 표시 : 🥨  
(🥨 표시는 실습 부분임을 뜻합니다)

## 💡Jekyll이란?

Jekyll은 **GitHub Pages에 대한 지원이 내장된 정적 사이트 생성기**로, Markdown과 HTML 파일을 사용하여 정적 웹 사이트를 만듭니다.

GitHub에서 추천하는 도구인 Jekyll에는 무료로 제공되는 테마가 많기 때문에 HTML/CSS/JS 삼대장으로 직접 사이트를 구현하지 않아도 **쉽고 빠르게 사이트를 만들어 블로그를 운영**할 수 있습니다.

그럼 지금부터 블로그 테마 적용을 위해 Jekyll을 설치해 보겠습니다.

![GitHub블로그2-Jekyll사이트](https://user-images.githubusercontent.com/39720852/152536699-5ace9b9a-3999-469b-8ff8-3c1a79c9b08d.png)

[Jekyll 공식 사이트](https://jekyllrb-ko.github.io/)
{:.figcaption}

다음으로 넘어가기 전에 참고용으로 **정적/동적 웹 페이지**에 대해 간략하게 설명드리자면 아래와 같습니다.

> 📌 **정적 웹 페이지**  
>
> * 웹 서버에 저장되어 있는 파일을 그대로 전달
>
> * 한 요청에 대해 모든 사용자가 같은 페이지를 전달받음

> 📌 **동적 웹 페이지**
>
> * 서버에 있는 데이터를 스크립트를 통해 가공한 후, 전달
>
> * 사용자는 요청에 따라 다른 페이지를 전달받음

## 💡 Jekyll 설치

### 1. Ruby 설치

🥨 Jekyll 설치에 앞서 먼저 Ruby 설치 여부를 확인합니다.

```
// Ruby 설치 확인 명령어
ruby -v
```

Jekyll은 Ruby 기반이기 때문에 <span style="background-color:#ffdce0">**Jekyll 먼저 설치하면 오류가 발생하므로**</span> 명령어를 사용하여 Ruby의 설치 여부부터 확인합니다.

🥨 Ruby가 없는 경우, 공식 사이트에서 [설치 방법](https://www.ruby-lang.org/ko/documentation/installation/)을 확인 후, os에 맞게 설치를 진행합니다.

<details> 
<summary>(Windows 기준) 설치 과정 펼치기</summary>
<div markdown="1">

1. [다운로드 페이지]((https://rubyinstaller.org/))에 들어가서 **'=>' 표시가 있는 Installer를 다운로드한 후, 실행**합니다.

    ![GitHub블로그2-ruby인스톨러](https://user-images.githubusercontent.com/39720852/152679646-e61f1305-e286-414e-ba5a-8e990b4770e1.png){: width="450"}

2. Select Components 단계에서 **체크박스를 모두 선택**합니다.

    ![GitHub블로그2-ruby인스톨러실행](https://user-images.githubusercontent.com/39720852/152681201-92bddd7d-0fe4-489c-9246-8397bc70dcb5.png)

3. Installer가 종료되고 터미널이 실행되면 **'1' 입력 후, 엔터**를 누릅니다.

    ![GitHub블로그2-ruby설치1](https://user-images.githubusercontent.com/39720852/152683476-0a6373ed-dd58-4fd6-a995-248b9b43713a.png)

4. 설치가 완료된 후, 엔터를 누르면 터미널이 종료됩니다.

    ![GitHub블로그2-ruby설치2](https://user-images.githubusercontent.com/39720852/152683505-80f93d14-278b-45c5-9289-e94bd06781f4.png)

5. 터미널을 실행하여 **Ruby 설치 확인 명령어**를 입력한 후, Ruby 버전이 뜬다면 설치 완료!

    ![GitHub블로그2-ruby설치확인](https://user-images.githubusercontent.com/39720852/152683522-16338f0b-9b14-4062-a999-82f1be8ed49f.png)

</div>
</details>

### 2. Jekyll 설치

#### ① Jekyll 설치

🥨 터미널 실행 후, 명령어를 입력하여 **Jekyll을 설치**합니다.

```
gem install jekyll bundler
```

#### ② 파일 삭제

🥨 index.html과 README.md **파일을 삭제**합니다.

![GitHub블로그2-파일제거](https://user-images.githubusercontent.com/39720852/152684112-7296a5a1-9523-4926-b6fa-0e97b6b58ff3.png)

#### ③ Jekyll 생성

🥨 파일들을 삭제한 위치에서 터미널을 실행하여 **Jekyll을 생성**합니다.

```
jekyll new ./
```

![GitHub블로그2-jekyll생성](https://user-images.githubusercontent.com/39720852/152684517-dc053381-ccce-4d2e-b2f0-f40ed16e6de0.png)

#### ④ bundle 설치

🥨 **bundle을 설치**합니다.

```
bundle install
```

#### ⑤ 로컬 서버 실행
🥨 **로컬 서버를 실행**합니다.

```
bundle exec jekyll serve
```

저는 이 단계에서 <span style="background-color:#ffdce0">**2가지 오류**</span>가 발생했고, 아래와 같은 방법으로 해결했습니다.

> 📌 에러 1) Jekyll 4.2.1   Please append `--trace` to the `serve` command for any additional information or backtrace.  
![GitHub블로그2-에러1](https://user-images.githubusercontent.com/39720852/152685266-20ae57d1-eb81-4406-a8f2-4d54c06d08ba.png)

> 📌 **해결) 명령어 뒤에 --trace 추가**  
![GitHub블로그2-해결1](https://user-images.githubusercontent.com/39720852/152688222-21ee431a-be2c-42a1-9bec-234333ca3d47.png)

> 📌 에러 2) C:/Ruby30-x64/lib/ruby/gems/3.0.0/gems/jekyll-4.2.1/lib/jekyll/commands/serve/servlet.rb:3:in `require': cannot load such file -- webrick (LoadError)  
![GitHub블로그2-에러2](https://user-images.githubusercontent.com/39720852/152688507-73028291-579b-4e37-9564-74080c703852.png)

> 📌 **해결) bundle add webrick 명령어 실행**
> ```
> bundle add webrick
> ```

#### ⑥ 로컬 서버 확인

🥨 브라우저에서 **로컬 서버 주소를 확인**해 봅니다.

![GitHub블로그2-로컬주소](https://user-images.githubusercontent.com/39720852/152688667-64db2677-d032-4222-92f8-39b7a8cb6277.png)

![GitHub블로그2-로컬주소확인](https://user-images.githubusercontent.com/39720852/152688733-842e3809-dfe4-4eed-8699-8ab31d3f0499.png)

#### ⑦ (선택) commit/push

🥨 원격 저장소에 push하면 username.github.io 주소에 반영됩니다.

```
git add --all

git commit -m "Jekyll 설치"

git push -u origin main
```

지금 commit/push 하셔도 좋고 테마 적용까지 한 이후에 하셔도 괜찮습니다.

저는 버전 관리 차원에서(테마 적용 중에 잘못된다면 Jekyll 설치 상태로 돌아오기 위해ㅎ) commit만 했습니다!

---

<br/>
자! 이렇게 해서 Jekyll을 설치해 봤습니다.

이제 테마를 적용할 생각에 설레네요😝

다음 글에서는 <span style="background-color:#f1f8ff">**테마 적용하는 법**</span> 에 대해서 소개해 드리도록 하겠습니다.
<br/><br/><br/>
**오류 및 오타 지적, 질문, 인사** 등 무엇이든 언제나 환영입니다!

읽어주셔서 감사합니다.

끝!🦕
<br/><br/><br/>
🔗 다음 글 바로가기 [GitHub 블로그 만들기 (3) - Jekyll 테마 적용](/blog/git-github/2022-02-06-github_blog(3))

## 👍 참고

* [GitHub Pages 공식 문서](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/about-github-pages-and-jekyll#front-matter)
* [How to Jekyll?](https://wikidocs.net/91460)
* [왕초보를 위한 Github 블로그 만들기(1)](https://zeddios.tistory.com/1222)
* [[GithubPages] 하루만에 만드는 깃허브 블로그-02.시작하기](https://khw11044.github.io/blog/githubpages/2020-12-26-making-blog-02/)
* [GitHub 블로그 만들기 실패](https://medium.com/@kyuchul2/github-%EB%B8%94%EB%A1%9C%EA%B7%B8-%EB%A7%8C%EB%93%A4%EA%B8%B0-%EC%8B%A4%ED%8C%A8-58eae3416a8c)
