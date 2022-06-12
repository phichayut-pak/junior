<template>
  <router-view/>
  <formAlert/>
</template>

<script>
import formAlert from "./components/formAlert.vue";

export default {
  components: {
    formAlert,
  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

body {
  width: 100%;
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
background-image: linear-gradient(120deg, #e0c3fc 0%, #8ec5fc 100%);
}
</style>
