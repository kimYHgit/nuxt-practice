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
