<template>
  <div id="app">
    <app-header v-on:tiChanged="upTitle($event)" v-bind:title="title"></app-header>
    <users v-bind:users="users"></users>
    <users v-bind:users="users"></users>
    <app-footer></app-footer>
  </div>
</template>

<script>
// 局部注册组件
import Users from './components/Users'
import Header from './components/Header'
import Footer from './components/Footer'

export default {
  name: 'App',
  data() {
    return {
      users:[
        {name: "zhangsan", position: "web", show: false},
        {name: "zhangsan", position: "web", show: false},
        {name: "zhangsan", position: "web", show: false},
        {name: "zhangsan", position: "web", show: false},
        {name: "zhangsan", position: "web", show: false},
        {name: "zhangsan", position: "web", show: false},
        {name: "zhangsan", position: "web", show: false}
      ],
      title: "example app"
    }
  },
  components: {
    "users": Users,
    "app-header": Header,
    "app-footer": Footer
  },
  methods: {
    upTitle: function (title) {
      this.title = title;
    }
  }
}
</script>

<style scoped>
h1 {
  color: aqua;
}
</style>
