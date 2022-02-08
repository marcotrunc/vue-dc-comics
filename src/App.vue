<template>
  <div>
    <Header />
    <main>
      <main-top></main-top>
      <main-bottom></main-bottom>
    </main>
    <footer>
      <footer-top></footer-top>
      <footer-bottom></footer-bottom>
    </footer>
  </div>
</template>

<script>
import Header from "./components/Header.vue";
export default {
  name: "App",
  components: {
    Header,
  },
};
</script>

<style lang="scss">
@import "./assets/sass/style.scss";
</style>
