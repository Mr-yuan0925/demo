<template>
  <div class="default-bg">
    <header>
      <!-- 页面顶部导航 -->
      <my-header />
    </header>

    <main>
      <nuxt /> <!-- 渲染页面内容 -->
    </main>

    <footer>
      <!-- 页面底部信息 -->
      <my-footer />
    </footer>
  </div>
</template>
<script setup>
</script>

<style>
.default-bg {
  width: 100%;
  min-height: 100vh;
  background-color: #524fae;
}
</style>
