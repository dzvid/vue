<template>
  <div id="app">
    <main-header></main-header>
    <router-view class="container"></router-view>
  </div>
</template>

<script>
import MainHeader from "@/components/MainHeader.vue";

export default {
  name: "App",
  components: {
    MainHeader,
  },
};
</script>

<style>
/* GLOBAL RESET  */
* {
  margin: 0;
  padding: 0;
  outline: 0;
  box-sizing: border-box;
}

*:focus {
  outline: 0;
}

html,
body,
#app {
  height: 100%;
}

body,
input,
button {
  font-size: 16px;
  font-family: "Avenir", Helvetica, Arial, sans-serif;
}

button {
  cursor: pointer;
}

ul {
  list-style: none;
}

a,
body {
  color: #234;
}

a {
  text-decoration: none;
  font-weight: bold;
}

a.router-link-active {
  color: #4b8;
}

/* END GLOBAL STYLE */

/* ROUTER VIEW */
.container {
  max-width: 800px;
  margin: 0 auto;
  padding: 20px;
}
</style>