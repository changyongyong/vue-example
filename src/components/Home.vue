<template>
  <div id="home">
    <app-header v-on:tiChanged="upTitle($event)" v-bind:title="title"></app-header>
    <users v-bind:users="users"></users>
    <users v-bind:users="users"></users>
    <app-footer></app-footer>
  </div>
</template>

<script>
  // 局部注册组件
  import Users from './Users'
  import Header from './Header'
  import Footer from './Footer'

  export default {
    name: 'Home',
    data() {
      return {
        users:[
          // {name: "zhangsan", position: "web", show: false},
          // {name: "zhangsan", position: "web", show: false},
          // {name: "zhangsan", position: "web", show: false},
          // {name: "zhangsan", position: "web", show: false},
          // {name: "zhangsan", position: "web", show: false},
          // {name: "zhangsan", position: "web", show: false},
          // {name: "zhangsan", position: "web", show: false}
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
    },
    created() {
      this.$http.get("http://jsonplaceholder.typicode.com/users")
        .then((data) => {
          console.log(data);
          this.users = data.body;
        });
    }
  }
</script>

<style scoped>
  h1 {
    color: aqua;
  }
</style>
