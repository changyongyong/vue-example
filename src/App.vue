<template>
  <div id="app">
    <ul>
      <li><a href="/">Home</a></li>
      <li><a href="/test">test</a></li>
      <li><a href="/helloworld">HelloWorld</a></li>

      <!-- 路由链接，整个页面不刷新 -->
      <li><router-link to="/">Home</router-link></li>
      <li><router-link to="/test">test</router-link></li>
      <li><router-link to="/helloworld">HelloWorld</router-link></li>

    </ul>
    <router-view></router-view>
  </div>
</template>

<script>

export default {
  name: 'App',
  data() {
    return {

    }
  }
}
</script>

<style scoped>
h1 {
  color: aqua;
}
</style>
