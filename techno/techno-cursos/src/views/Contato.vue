<template>
  <div>
    <div v-if="loading">
      <PageLoading />
    </div>

    <transition>
      <div v-if="api">
        <h1>{{ api.titulo }}</h1>
        <p>{{ api.descricao }}</p>
        <ul>
          <li>
            <p><b>Telefone:</b> {{ api.contato.telefone }}</p>
          </li>
          <li>
            <p><b>Email:</b> {{ api.contato.email }}</p>
          </li>
          <li>
            <p><b>Endereço:</b> {{ api.contato.endereco }}</p>
          </li>
        </ul>
      </div>
    </transition>
  </div>
</template>

<script>
import fetchData from "@/mixins/fetchData.js";

export default {
  name: "Contato",
  mixins: [fetchData],
  created() {
    this.fetchData("/contato");
  },
};
</script>

<style></style>
