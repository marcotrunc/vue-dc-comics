<template>
  <main class="container-fluid">
    <Jumbotron />
    <!-- Main top -->
    <section id="main-top">
      <Maintop :series-list="seriesList" />
    </section>
    <!-- Main Bottom -->
    <section id="main-bottom">
      <Mainbottom />
    </section>
  </main>
</template>

<script>
import Maintop from "./Maintop.vue";
import Mainbottom from "./Mainbottom.vue";
import Jumbotron from "./Jumbotron.vue";
export default {
  name: "Main",
  components: {
    Jumbotron,
    Maintop,
    Mainbottom,
  },
  props: ["seriesList"],
};
</script>

<style lang="scss" scoped>
@import "../assets/sass/_vars.scss";
// ** Main-top
#main-top {
  background-color: $bg-black;
}
// ** Main-bottom
#main-bottom {
  background-color: $bg-blue;
  padding: 35px 0px;
}
</style>