<template>
  <header>
    <nav>
      <div class="logo">
        <router-link to="/">Techno</router-link>
      </div>
      <ul>
        <li>
          <router-link to="/cursos">Cursos</router-link>
        </li>
        <li>
          <router-link to="/contato">Contato</router-link>
        </li>
      </ul>
    </nav>
  </header>
</template>

<script>
export default {
  name: "MainHeader",
};
</script>

<style scoped>
header {
  background: #234;
}

header a {
  color: #fff;
}

a.router-link-active {
  color: #4b8;
}

nav {
  max-width: 800px;
  margin: 0 auto;
  padding: 20px;

  display: flex;
  align-content: space-between;
}

ul li {
  display: inline-block;
}

li a {
  padding: 0px 10px;
  margin-left: 10px;
}

.logo {
  flex: 1;
}

.logo a {
  font-size: 1.2rem;
  color: #fff;
}
</style>