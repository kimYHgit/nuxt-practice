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
