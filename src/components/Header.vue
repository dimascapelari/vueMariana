<template>
  <h1 v-if="titulo == 'Página Header'">{{ titulo }}</h1>
  <h1 v-else>Título 2</h1>
  <input type="text" v-model="textoInput" />
  <h2>{{ textoInput }}</h2>
  <img :src="imageSrc" /><br />
  <button @click="deletaTitulo">Deletar Título</button>
</template>

<script>
export default {
  name: "Header",
  data() {
    return {
      titulo: "Página Header",
      textoInput: "",
      imageSrc: "/images/download.png",
    };
  },
  methods: {
    deletaTitulo() {
      this.titulo = "";
    },
  },
};
</script>

<style></style>
