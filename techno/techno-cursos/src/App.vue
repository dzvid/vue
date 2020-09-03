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
body {
  margin: 0px;
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  color: #234;
}

ul {
  list-style: none;
  padding: 0px;
  margin: 0px;
}

a {
  font-weight: bold;
  text-decoration: none;
  color: #234;
}

a.router-link-active {
  color: #4b8;
}

button {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  cursor: pointer;
}

img {
  max-width: 100%;
}

/* END GLOBAL STYLE */

/* ROUTER VIEW */
.container {
  max-width: 800px;
  margin: 0 auto;
  padding: 20px;
}

/* TRANSITION ANIMATION */
.v-enter {
  opacity: 0;
  transform: translate3d(-20px, 0, 0);
}

.v-enter-active {
  transition: all 0.3s;
}

/* GRID */
.conteudo {
  display: grid;
  grid-template-columns: 1fr minmax(200px, 400px);
  grid-gap: 32px;
}

@media screen and (max-width: 400px) {
  .conteudo {
    display: block;
  }
}
</style>
