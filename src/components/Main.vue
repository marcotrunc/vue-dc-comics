<template>
  <main class="container-fluid">
    <!-- Main top -->
    <section id="main-top">
      <div class="container">
        <p>-->Content goes here--></p>
      </div>
    </section>
    <!-- Main Bottom -->
    <section id="main-bottom">
      <Mainbottom />
    </section>
  </main>
</template>

<script>
import Mainbottom from "./Mainbottom.vue";
export default {
  name: "Main",
  components: {
    Mainbottom,
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/sass/_vars.scss";
// ** Main-top
#main-top {
  background-color: $bg-black;
}
#main-top .container {
  display: flex;
  align-content: center;
  padding: 40px 0px;
  p {
    color: #fff;
    font-size: 1.2rem;
    font-weight: bold;
  }
}
// ** Main-bottom
#main-bottom {
  background-color: $bg-blue;
  padding: 35px 0px;
}
</style>