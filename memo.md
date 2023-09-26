# Nuxt Framework

---

- 깃헙 공식 https://github.com/nuxt/nuxt
- 공식 문서 https://nuxt.com/
- nuxt KO 문서 https://develop365.gitlab.io/nuxtjs-0.10.7-doc/ko/guide/installation/
- npm nuxt [ver 3.7.4] https://www.npmjs.com/package/nuxt
- 개념 잡기1 https://doozi0316.tistory.com/entry/Nuxtjs-%EC%9D%98-%EA%B0%9C%EB%85%90%EA%B3%BC-%EC%98%88%EC%A0%9C-SSR-CSR-Universal
- 개념 잡기2 http://guide.ustraframework.kro.kr/ref-doc/03/0umuyYIYdjIf2PPf4bDN
- 코드 연습1 https://junyharang.tistory.com/290
- 코드 연습2 https://www.youtube.com/playlist?list=PL4cUxeGkcC9haQlqdCQyYmL_27TesCGPC
  - 소스코드 https://github.com/iamshaunjp/nuxt-3-tutorial

> **Nuxt.js** - framework for framework

- Vue.js 프레임워크 기반 SSR(Server Side Rendering) 웹 페이지를 만들 수 있도록 해 주는 프레임워크. [Vue + Library]
- **검색 엔진 최적화**
  - SEO(Search Engine Optimization) 등의 문제로 CSR이 아닌 SSR 웹을 구축해야 하는 경우에 유용하게 사용할 수 있음.
  - SSR 구현을 위해 Express 서버를 내장하고 있음.
- 3가지의 렌더링 모드를 지원.
  - Single Page App(SPA), Universal App, Static App
- **Universal App**
  - Nuxt 앱을 첫 방문할 때는 서버에서 렌더링을 하고 그 이후에는 SPA마냥 클라이언트에서 렌더링 [Prefetching , Code Splitting , Hydration]
  - 페이지 로딩 속도와 사용자 경험 향상
- 초기 프로젝트 설정 비용 감소와 생산성 향상
- 라우터, 스토어 등의 라이브러리 설치 및 설정 파일 필요 X
- 파일 기반의 라우팅 방식. 설정 파일 자동 생성
- pages 폴더 vue 파일 기반으로 routing 서비스 제공

**Nuxt.js 에 포함된 기능들**
Vue 3
Vue Router
Vuex
Vue Server Renderer
vue-meta
vue-loader
babel-loader
Webpack

**Nuxt 프로젝트 & Vue.js 프로젝트 차이**

- src 폴더 아래에 있던 코드들이 루트 레벨로
- router와 views 폴더 -> pages 폴더
- router/index.js 에 직접 라우터를 등록해 주던 것과 달리 Nuxt에서는 빌드시 자동으로 pages 폴더의 구조대로 라우터를 생성
- 추가 라이브러리 없이 메타 태그를 작성가능.
- Layout 폴더가 추가
- Nuxt를 통해 라우팅되는 컴포넌트를 감싸는 레이아웃을 별도로 만들어줄 수 있습니다.
- middleware, plugin 폴더 추가
- middleware : 렌더링 이전 단계에 수행하는 함수 등을 선언하고 관리
- plugin : 렌더링 이전 단계에서 외부 라이브러리(i.e. Axios)를 불러오는 등의 기능을 수행

**Nuxt 키워드**

- [extension] Vue Language Features (volar)
- ㅇㄴ
- ㅇㄴ
- ㅇㄴ
- ㅇㄴㅇㄴ

Nuxt 기초 / 데이터 가져오기 / 라우팅 처리 / tailwindcss / 서버라우팅

### 용어 참고

---

> static-site-generator , node , vue , universal , ssr
> nuxt , full-stack , server-rendering , csr , hybrid , ssg , SEO

**Isomorphic JavaScript**

- 프론트엔드와 백엔드에서 모두 사용 가능한 Universal JavaScript
- JavaScript는 서버 개발자가 화면 구현을 위해 템플릿 언어와 함께 일부 사용하던 언어에 불과했음.
- Web 기술이 급격하게 성장하면서 화면 개발 영역을 체계적으로 관리할 필요가 생김.
- 각종 프론트엔드/백엔드 라이브러리&프레임워크가 등장

> SEO(Search Engine Optimization)와 SSR(Server Side Rendering) 에 대한 필요성이 대두됨.

- SEO

  - sdsdsd

- CSR & SSR & SPA & Universal app

> **Universal App** : 새로운 방식의 SSR

server-side rendering + client-side navigation

- 첫 화면만 과거의 서버 렌더링 처럼 완성된 HTML을 뿌려주고(SSR), 이 후엔 AJAX로 동적 라우팅을 수행하여 필요한 데이터만 가져온다.(CSN)

CSN -> **PreFetch & Hydration**

- PreFetch
  server side rendering 후, view port의 nuxt-link 태그를 통해 다음 페이지를 미리 다운로드 해 온다.
- Hydration
  렌더링 과정을 마치고 브라우저로 전달된 HTML파일 위에 남은 자바스크립트 코드들을 실행하는 동작이다.
  기존의 SPA와 동일한 동작과 반응성을 보장할 수 있게 된다.
  불완전한 HTML 파일이라는 '마른 땅'에 자바스크립트라는 '물'을 뿌리는 일이다.

> SSR

- 첫 페이지를 렌더링 된 상태로 응답해주는 것
- SPA 특성상 내용이 없는 빈 html에 번들링 된 js가 실행되면서 내용물들이 렌더링이 되기 전까지 사용자는 빈 화면만 보고 있어야 하고 js를 실행하지 못하는 검색엔진 등도 해당 페이지의 내용물을 알지 못함.

### 링크 참고

---

- Nuxt.js vs Vue.js

  - https://velog.io/@bluestragglr/Nuxt.js-vs-Vue.js-SSR-%EC%8B%9C%EC%9E%91%ED%95%98%EA%B8%B0

- Nuxt.js 란? 개념과 예제

  - https://doozi0316.tistory.com/entry/Nuxtjs-%EC%9D%98-%EA%B0%9C%EB%85%90%EA%B3%BC-%EC%98%88%EC%A0%9C-SSR-CSR-Universal

- Next.js / Nest.js / Nuxt.js

  - https://techblog.lotteon.com/next-js-%EB%A1%9C-%EA%B5%AC%ED%98%84%ED%95%98%EB%8A%94-isomorphic-javascript-c77595b626c5
  - https://day0404.tistory.com/8

- nuxt.js 학습하기 시리즈

  - https://abangpa1ace.tistory.com/category/Front-End%28Web%29/Vue?page=1

- nuxt.js 사용후기
  - https://bubobubo003.tistory.com/76

### Nuxt App

---

**사양**

- Node.js - v16.10.0 or newer
- Visual Studio Code with the Volar Extension

> New Project 설치

```bash
npx nuxi init nuxt-practice
```

```bash
✔ Which package manager would you like to use?
npm
◐ Installing dependencies...                                                                                                                  오후 2:54:42

> postinstall
> nuxt prepare


ℹ Nuxt collects completely anonymous data about usage.                                                                                       오후 2:56:00
  This will help us improve Nuxt developer experience over time.
  Read more on https://github.com/nuxt/telemetry


✔ Are you interested in participating?
No

✔ Types generated in .nuxt                                                                                                                   오후 2:56:11

added 798 packages, and audited 800 packages in 1m

121 packages are looking for funding
  run `npm fund` for details

found 0 vulnerabilities
✔ Installation completed.                                                                                                                    오후 2:56:11

✔ Initialize git repository?
Yes
ℹ Initializing git repository...                                                                                                             오후 2:56:20

Initialized empty Git repository in C:/Workspace/nuxt3-practice/nuxt-practice/.git/
                                                                                                                                              오후 2:56:20
✨ Nuxt project has been created with the v3 template. Next steps:
 › cd nuxt-practice                                                                                                                           오후 2:56:20
 › Start development server with npm run dev                                                                                                  오후 2:56:20
```

**Nuxt app 실행**

```bash
npm run dev
```

**app.vue 코드 수정**

- div 태그 내에 코드 수정한다.

```javascript
<template>
  <div>
    <h1>Hi!</h1>
  </div>
</template>
```
