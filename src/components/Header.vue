<template>
    <header v-on:click="chTitle">
      <h1>
        {{title}}
      </h1>
    </header>
</template>

<script>
    export default {
      name: "app-header",
      props: {
        title: {

        }
      },
      data() {
        return {

        }
      },
      methods: {
        chTitle:function () {
          this.$emit("tiChanged", "son to father")
        }
      },
      beforeCreate: function () {
        console.log("create header");
      },
      created: function () {
        console.log("header is created");
      },
      beforeMount: function () {
        console.log("header mount");
      },
      mounted: function () {
        console.log("header is mounted");
      },
      beforeUpdate: function () {
        console.log("header is before update");
      },
      updated: function () {
        console.log("header is updated");
      },
      beforeDestroy: function () {
        console.log("header is before destroy");
      },
      destroyed: function () {
        console.log("headeris destroyed");
      }

    }
</script>

<style scoped>
  header {
    background: lightgreen;
    padding: 10px;
  }

  h1 {
    color: #222;
  }
</style>
