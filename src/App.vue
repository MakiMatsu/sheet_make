<template>
  <div id="app">
    <GitData repoName="MakiMatsu" />
  </div>
</template>

<script>
import GitData from "./components/Git.vue";

export default {
  name: "app",
  components: {
    GitData
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
