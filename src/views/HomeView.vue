<template>
  <div>
    <nav>
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </nav>

    <Header />
  </div>
</template>

<script>
import Header from "../components/Header.vue";

export default {
  components: {
    Header,
  },
};
</script>

<style></style>
