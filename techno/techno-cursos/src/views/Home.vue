<template>
  <div>
    <div v-if="loading">
      <PageLoading />
    </div>

    <transition>
      <div v-if="api" class="conteudo">
        <div>
          <h1>Sobre a {{ api.titulo }}</h1>
          <p>{{ api.descricao }}</p>
          <router-link tag="button" to="/cursos" class="btn-cursos">
            Cursos
          </router-link>

          <div>
            <h2>Avaliações</h2>
            <ul>
              <li v-for="{ nome, descricao } in api.avaliacoes" :key="nome">
                <p>{{ nome }}</p>
                <p>
                  {{ descricao }}
                </p>
              </li>
            </ul>
          </div>
        </div>
        <img src="@/assets/reach-your-goal.png" alt="Alcance seus objetivos!" />
      </div>
    </transition>
  </div>
</template>

<script>
import fetchData from "@/mixins/fetchData.js";

export default {
  name: "Home",
  mixins: [fetchData],
  created() {
    this.fetchData("/home");
  },
};
</script>

<style scoped>
.btn-cursos {
  border: none;
  background: #4b8;
  color: #fff;
  padding: 16px 32px;
  border-radius: 4px;
  font-size: 1rem;
  margin-top: 10px;
  margin-bottom: 40px;
  box-shadow: 0px 4px 2px rgba(0, 0, 0, 0.1);
}

.btn-cursos:active {
  background: #234;
}
</style>
