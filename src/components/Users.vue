<template>
    <div class="users">
      <h1>hello users</h1>
      <ul>
        <li v-for="user in users">
          <h2>{{user.name}}</h2>
          <h3>{{user.email}}</h3>
        </li>
      </ul>
      <button v-on:click="delUser">删除</button>
    </div>
</template>

<script>
    export default {
      name: "Users",
      props: {
        users: {
          type: Array,
          required: true
        }
      },
      data() {
          return {

          }
      },
      methods: {
        delUser: function () {
          this.users.pop();
        }
      }
    }
</script>

<style scoped>
  .users{
    width: 100%;
    max-width: 1200px;
  }

  ul{
    display: flex;
    flex-wrap: wrap;
    padding: 0;
    list-style-type: none;
  }

  li{
    flex-grow: 1;
    flex-basis: 50px;
    text-align: center;
    padding: 10px;
    border: 1px solid #222;
  }
</style>
