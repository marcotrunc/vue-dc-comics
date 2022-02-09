<template>
  <div>
    <div id="jumbo" class="container-fluid"></div>
  </div>
</template>

<script>
export default {
  name: "Jumbotron",
};
</script>

<style lang="scss" scoped>
#jumbo {
  height: 300px;
  background-image: url("../assets/img/jumbotron.jpg");
  background-repeat: no-repeat;
  background-position: contain;
  background-size: cover;
}
</style>