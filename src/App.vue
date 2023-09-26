<template>
  <div id="app">
    <gerarResposta />
  </div>
</template>

<script>
import gerarResposta from "@/components/gerarResposta.vue";

export default {
  components: {
    gerarResposta,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
