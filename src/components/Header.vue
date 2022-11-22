<template>
  <div ref="container">
    <div ref="titulo">
      <h1 v-if="titulo == 'Página Header'">{{ titulo }}</h1>
      <h1 v-else>Título 2</h1>
      <input type="text" v-model="textoInput" />
      <h2>{{ textoInput }}</h2>
    </div>
    <img :src="imageSrc" /><br />

    <input
      ref="btn"
      type="button"
      value="Deletar Título"
      @click="deletaTitulo"
      @change="voltarTitulo"
    />
  </div>
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
      if (this.titulo == "Página Header") {
        this.titulo = "";
        this.$refs.btn.value = "Voltar Título";
      } else {
        this.titulo = "Página Header";
        this.$refs.btn.value = "Deletar Título";
      }
    },
  },
  mounted() {
    setTimeout(() => {
      this.$refs.container.style.height = "500px";
      this.$refs.container.style.backgroundColor = "black";
      this.$refs.container.style.textAlign = "center";
      this.$refs.titulo.style.color = "#fff";
    }, 1000);
  },
};
</script>

<style></style>
