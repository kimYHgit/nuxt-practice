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
- [extension] Vue VSCodes Snippets
- ㅇㄴ
- ㅇㄴ
- ㅇㄴ
- ㅇㄴㅇㄴ

Nuxt 기초 / 데이터 가져오기 / 라우팅 처리 / tailwindcss / 서버라우팅

### 용어 참고

---

> static-site-generator , node , vue , universal , ssr
> nuxt , full-stack , server-rendering , csr , hybrid , ssg , SEO

> **Isomorphic JavaScript**

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

> **SSR**

- 첫 페이지를 렌더링 된 상태로 응답해주는 것
- SPA 특성상 내용이 없는 빈 html에 번들링 된 js가 실행되면서 내용물들이 렌더링이 되기 전까지 사용자는 빈 화면만 보고 있어야 하고 js를 실행하지 못하는 검색엔진 등도 해당 페이지의 내용물을 알지 못함.

> **컴포넌트와 컴포저블**

- 컴포넌트는 UI 요소를 정의하고 구성하는 데 사용
- 컴포저블은 코드 재사용과 로직 분리를 위한 도구로 사용

Composition API를 통해 컴포넌트의 로직을 컴포저블로 분리하고, 컴포넌트에서 이러한 컴포저블을 가져와 사용할 수 있습니다.

1. 컴포넌트 (Components):

   - 컴포넌트는 Vue 애플리케이션의 UI를 구성하는 블록 단위입니다.
   - 컴포넌트는 Vue 컴포넌트 인스턴스로 정의되며, 데이터, 메서드, 라이프사이클 훅, 템플릿 등을 포함할 수 있습니다.
   - 컴포넌트는 Vue 인스턴스로부터 상속된 옵션을 사용하여 정의되며, 이러한 컴포넌트는 재사용 가능하며, 여러 곳에서 사용될 수 있습니다.

2. 컴포저블 (Composition API):
   - 컴포저블은 Vue 3에서 도입된 새로운 방식의 코드 구성 방법입니다.
   - 컴포저블은 컴포넌트의 로직을 논리적인 단위로 분리하고 재사용 가능한 모듈로 만드는 데 사용됩니다.
   - 컴포저블은 Vue 3의 Composition API를 사용하여 작성되며, 단일 파일 컴포넌트의 `<script>` 섹션 내에서 정의됩니다.
   - 컴포저블을 사용하면 컴포넌트의 코드를 더 작고 읽기 쉽게 유지하고, 로직을 재사용하기 용이하게 만들 수 있습니다.

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

### **페이지 구성 & 경로 라우팅**

- https://nuxt.com/docs/getting-started/routing
- pages 폴더 생성
- 특정 URL에 Mapping 되어 그려질 Component들이 담기는 곳.
- app.vue 삭제 , pages 폴더 추가
- pages 폴더에 index.vue , about.vue 파일 추가
- v base 3 setup 스니펫 사용

> index.vue , about.vue

```javascript
<template>
  <div>
    <h2>Home</h2>
    <p>
      Lorem ipsum dolor, sit amet consectetur adipisicing elit. Quae earum
      numquam sapiente. Pariatur, provident blanditiis omnis molestiae quaerat
      eum! Maiores ut ratione tempore. Aut error accusamus dolore distinctio
      velit! Assumenda.
    </p>
  </div>
</template>

<script setup></script>

<style scoped>
h2 {
  margin-bottom: 20px;
  font-size: 36px;
}
p {
  margin: 20px 0;
}
</style>

```

pages 폴더 내의 모든 Vue 파일은 파일의 내용을 표시하는 해당 URL(또는 경로)을 생성합니다.
예를들어 pages폴더 내에 products 라는 폴더를 만들면 해당 폴더이름으로 경로를 자동으로 생성합니다.

- pages폴더 내 products폴더
- 경로 : /products

products폴더의 하위 경로를 구성하려면 경로이름에 맞는 새로운 vue 파일을 생성하면됨.

- products폴더 내 item.vue 파일
- 경로 : /products/item

**useRoute() 컴포저블을 이용한 매개변수 경로 라우팅 처리**

- useRoute().params 메서드를 이용하면 매개변수가 포함된 동적 경로의 라우팅 처리도 가능하다.

```
pages/
--| about.vue
--| index.vue
--| products/
----| index.vue
----| item.vue
----| [id].vue
```

사용자 ID를 매개변수로 받는 경로를 구성해보자

경로 : /products/:id

**[id].vue 파일 생성**

- 파일 이름을 **대괄호로** 감싼다.
- 파일 이름은 매개변수로 사용할 이름을 입력한다.

> [id].vue

```javascript
<template>
  <div>
    <p>
      Prduct Details for <b>{{ id }}</b>
    </p>
    <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit.</p>
  </div>
</template>

<script setup>
const { id } = useRoute().params;
</script>

<style scoped></style>

```

- template에 **이중 중괄호로** 매개변수를 감싼다.
- script 태그에 해당 코드 추가

```javascript
// 객체 구조분해할당
const { id } = useRoute().params;
```

매개변수 validation은....?

**NuxtLink 컴포넌트를 활용한 링크 처리**

- https://nuxt.com/docs/api/components/nuxt-link
- Vue Router's "RouterLink" component and HTML's "a" tag.

Nuxt에서 제공하는 NuxtLink 컴포넌트를 사용하면 효율적으로 네비게이션을 구현할수있다.

pages폴더 index.vue 의 template 코드를 수정한다.

> pages/index.vue

```javascript
<template>
  <div>
    <h2>Home</h2>
    <p>
      Lorem ipsum dolor, sit amet consectetur adipisicing elit. Quae earum
      numquam sapiente. Pariatur, provident blanditiis omnis molestiae quaerat
      eum! Maiores ut ratione tempore. Aut error accusamus dolore distinctio
      velit! Assumenda.
    </p>
    <div>
      <header>
        <nav>
          <NuxtLink to="/">Nuxt Project</NuxtLink>
          <ul>
            <li><NuxtLink to="/">Home</NuxtLink></li>
            <li><NuxtLink to="/about">About</NuxtLink></li>
            <li><NuxtLink to="/products">Products</NuxtLink></li>
          </ul>
          <a href="/about"> normal link - anchor tag </a>
        </nav>
      </header>
    </div>
  </div>
</template>
<!-- 앵커 태그와 nuxtlink 차이는?
서버의 요청을 가로채서 필요한 부분만 렌더링
앵커태그는 서버로 다시 요청한다.
-->
```

### 레이아웃

---

- https://nuxt.com/docs/guide/directory-structure/layouts
- 애플리케이션 전체에서 사용할 수 있는 사용자 정의 요소
- 재사용 가능한 일반적인 UI 또는 코드 패턴

**슬롯**

- 부모 컴포넌트가 자식 컴포넌트에게 콘텐츠를 전달할 수 있는 메커니즘을 제공.
- 이를 통해 부모 컴포넌트에서 자식 컴포넌트로 동적으로 콘텐츠를 주입하거나 자식 컴포넌트의 일부 영역에 커스텀 마크업을 제공할 수 있음.

**레이아웃 작성**

1. 루트 폴더에 layouts 폴더 생성한다.
2. 폴더 하위에 default.vue 파일 생성한다.
3. 재사용할 코드 내용을 작성한다.

index.vue , default.vue 코드를 다음과 같이 작성한다.

> **pages/index.vue**

```javascript
<template>
  <div>
    <h2>Home</h2>
    <p>
      Lorem ipsum dolor, sit amet consectetur adipisicing elit. Quae earum
      numquam sapiente. Pariatur, provident blanditiis omnis molestiae quaerat
      eum! Maiores ut ratione tempore. Aut error accusamus dolore distinctio
      velit! Assumenda.
    </p>
  </div>
</template>

<script setup></script>

<style scoped>
h2 {
  margin-bottom: 20px;
  font-size: 36px;
}
p {
  margin: 20px 0;
}
</style>


```

- .router-link-exact-active
- 현재 활성화된 라우터 링크(경로)를 나타내는 클래스.

> **layouts/default.vue**

```javascript
<template>
  <div>
    <header>
      <nav>
        <NuxtLink to="/">Nuxt Project</NuxtLink>
        <ul>
          <li><NuxtLink to="/">Home</NuxtLink></li>
          <li><NuxtLink to="/about">About</NuxtLink></li>
          <li><NuxtLink to="/products">Products</NuxtLink></li>
        </ul>
        <a href="/about"> normal link - anchor tag </a>
      </nav>
    </header>
  </div>
  <!-- output the page content -->
  <!-- 페이지 구성이 slot으로 처리됨. -->
  <div>
    <slot />
  </div>
</template>

<style scoped>
.router-link-exact-active {
  color: #12b488;
}
</style>

```

**Custom layouts - 특정 경로에만 레이아웃 처리**

특정 경로에만 특정 레이아웃을 주고 싶을때 layouts 폴더에 vue파일을 새롭게 생성해서 관리한다.

- 파일이름과 경로가 같지 않아도 된다.

작성된 레이아웃 파일을 적용하고자 하는 페이지의 script 태그에 definePageMeta() 함수를 사용하여 적용한다.

> layouts/products.vue

```javascript
<template>
  <div>
    <header>
      <nav>
        <NuxtLink to="/products">Nuxt Project items</NuxtLink>
      </nav>
    </header>
  </div>
  <div>
    <slot />
  </div>
  <footer>
    <ul>
      <li><NuxtLink to="/">Home</NuxtLink></li>
      <li><NuxtLink to="/about">About</NuxtLink></li>
      <li><NuxtLink to="/products">Products</NuxtLink></li>
    </ul>
  </footer>
</template>

<style scoped>
.router-link-exact-active {
  color: #12b488;
}
</style>
```

> **pages/products 폴더내 모든 vue 파일에 script 적용**

```javascript

<script setup>
definePageMeta({
  layout: "products",
});
</script>

```

### Module - tailwindCSS 사용

---

- https://nuxt.com/modules/

```
PS C:\Workspace\uvc\nuxt3-practice\nuxt-practice> npm run dev

> dev
> nuxt dev

Nuxt 3.7.4 with Nitro 2.6.3                                                                                                                   오후 5:55:05
[get-port] Unable to find an available port (tried 3000-3100 on host "localhost"). Using alternative port 3001                                오후 5:55:05
                                                                                                                                              오후 5:55:05
  ➜ Local:    http://localhost:3001/
  ➜ Network:  use --host to expose

ℹ Using default Tailwind CSS file                                                                                           nuxt:tailwindcss 오후 5:55:08
✔ Nuxt DevTools enabled (v0.8.5), press Shift + Alt + D in app to open  (experimental)                                                       오후 5:55:10
ℹ Tailwind Viewer: http://localhost:3001/_tailwind/                                                                         nuxt:tailwindcss 오후 5:55:10

 WARN                                                                                                                                         오후 5:55:13


[오후 5:55:13]  WARN  warn - No utility classes were detected in your source files. If this is unexpected, double-check the content option in your Tailwind CSS configuration.


 WARN  warn - https://tailwindcss.com/docs/content-configuration
```

**1. @nuxtjs/tailwindcss dependency 추가한다.**

```bash
# Using npm
npm install --save-dev @nuxtjs/tailwindcss

```

**2. nuxt.config.ts 파일에 해당 프로퍼티 추가**

```bash
{
  modules: [
    '@nuxtjs/tailwindcss'
  ]
}
```

3. **layouts/default.vue , products.vue 코드 수정 [클래스 적용]**

> **default.vue**

```javascript
<template>
  <div>
    <header class="shadow-sm bg-white">
      <nav class="container mx-auto p-4 flex justify-between">
        <NuxtLink to="/" class="font-bold">Nuxt Project</NuxtLink>
        <ul class="flex gap-4">
          <li><NuxtLink to="/">Home</NuxtLink></li>
          <li><NuxtLink to="/about">About</NuxtLink></li>
          <li><NuxtLink to="/products">Products</NuxtLink></li>
        </ul>
      </nav>
    </header>
  </div>
  <!-- output the page content -->
  <!-- 페이지 구성이 slot으로 처리됨. -->
  <div class="container mx-auto p-4">
    <slot />
  </div>
</template>
```

> **products.vue**

```javascript
<template>
  <div>
    <header class="shadow-sm bg-white">
      <nav class="container mx-auto p-4">
        <NuxtLink to="/products" class="font-bold">
          Nuxt Project items
        </NuxtLink>
      </nav>
    </header>
    <div class="container mx-auto p-4">
      <slot />
    </div>
    <footer class="container mx-auto p-4 flex justify-between border-t-2">
      <ul class="flex gap-4">
        <li>
          <NuxtLink to="/">Home</NuxtLink>
        </li>
        <li>
          <NuxtLink to="/about">About</NuxtLink>
        </li>
        <li>
          <NuxtLink to="/products">Products</NuxtLink>
        </li>
      </ul>
    </footer>
  </div>
</template>
```

**assets/css폴더 추가및 tailwind.css 파일 작성**

> assets/css/tailwind.css

- 폴더구조상 assets하위 폴더로 css가 들어가야 클래스 인식함.

```css
@tailwind base;
@tailwind components;
@tailwind utilities;

body {
  @apply bg-gray-50;
}

@layer components {
  .btn {
    @apply bg-[#12b488] text-white px-3 py-2 rounded-md text-sm text-white;
  }
}
```

### useFetch API를 이용한 데이터 가져오기

---

- https://nuxt.com/docs/getting-started/data-fetching#usefetch
- https://nuxt.com/docs/api/composables/use-fetch#usefetch

Nuxt에는 브라우저 또는 서버 환경에서 데이터 불러오기를 수행할 수 있는 두 가지 컴포저블과 내장 라이브러리인 useFetch, useAsyncData 및 $fetch가 포함되어 있습니다.
이 라이브러리를 함께 사용하면 환경 간 호환성과 효율적인 캐싱을 보장하고 중복 네트워크 호출을 방지할 수 있습니다.

useFetch는 컴포넌트 설정 함수에서 데이터 불러오기를 처리하는 가장 간단한 방법입니다.

반면에 사용자 상호작용을 기반으로 네트워크 요청을 하고자 할 때는 거의 항상 $fetch가 적합한 핸들러입니다.

보다 세분화된 제어가 필요한 경우, useAsyncData와 $fetch 컴포저블을 독립적으로 사용할 수 있습니다.

**상품 목록을 구성할 데이터를 받아오는 API 서버는 다음을 활용한다.**
**https://fakestoreapi.com/**

**전체 상품의 정보를 나타내기**

> **pages/products/index.vue**

```javascript
<template>
  <div>
    <div class="grid grid-cols-4 gap-5">
      <div v-for="p in products">
        <NuxtLink :to="`/products/${p.id}`">{{ p.title }}</NuxtLink>
      </div>
    </div>
  </div>
</template>

<script setup>
definePageMeta({
  layout: "products",
});

//fetch products data.
const { data: products } = await useFetch("https://fakestoreapi.com/products");
</script>

<style scoped></style>

```
