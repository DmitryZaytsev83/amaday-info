<template>
  <app-header></app-header>
  <app-main></app-main>
</template>

<script>
import AppHeader from "@/components/AppHeader";
import AppMain from "@/components/AppMain";

export default {
  name: 'App',
  components: {
    AppMain,
    AppHeader
  }
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  background-color: #000;
  font-family: sans-serif;
}

#app {
  font-family: "Roboto Light", Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #fff;
  width: 100%;
  height: 100vh;
}

.container {
  max-width: 1140px;
  margin: 0 auto;
  padding: 1rem;
}
</style>
