<template>
  <div>
    <Header />
    <Main />
    <footer>
      <footer-top></footer-top>
      <footer-bottom></footer-bottom>
    </footer>
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Main from "./components/Main.vue";
export default {
  name: "App",
  components: {
    Header,
    Main,
  },
};
</script>

<style lang="scss">
@import "./assets/sass/style.scss";
</style>
