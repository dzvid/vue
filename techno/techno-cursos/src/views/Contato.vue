<template>
  <div>
    <h1>Contato</h1>
    <div v-if="loading">
      <PageLoading />
    </div>
    <div v-if="api">
      <p>{{ api }}</p>
    </div>
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
