<template>
  <div id="app">
    <Header />
    <cat />
  </div>
</template>

<script>
import Header from "./components/Header";
import Cat from "./components/Cat.vue";

export default {
  name: "App",
  components: {
    Header,
    Cat,
  },
};
</script>

<style>
#app {
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen,
    Ubuntu, Cantarell, "Open Sans", "Helvetica Neue", sans-serif;
  font-size: 16px;
  line-height: 1.5;
  box-sizing: border-box;
}
</style>
