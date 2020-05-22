<template>
  <div id="app">
    <AppHeader />

    <AppForm />
  </div>
</template>

<script>
import AppHeader from "./components/AppHeader.vue";
import AppForm from "./components/AppForm.vue";

export default {
  components: {
    AppHeader,
    AppForm
  }
};
</script>

<style>
*,
*:before,
*:after {
  box-sizing: border-box;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
