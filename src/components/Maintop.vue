<template>
  <div>
    <div class="container py-5 position-relative">
      <div class="row justify-content-between">
        <div class="title-section">
          <a href="#" class="button-blue">Current series</a>
        </div>
        <div v-for="(serie, index) in seriesList" :key="index" class="col-2">
          <div class="card">
            <figure>
              <img :src="serie.thumb" :alt="serie.series" class="img-fluid" />
            </figure>
            <div class="description mb-2">
              <span class="fs-9">{{ serie.series }}</span>
            </div>
          </div>
        </div>
        <div class="col-12 text-white d-flex justify-content-center pt-5">
          <a href="#" class="button-blue">Load more</a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Maintop",
  props: ["seriesList"],
};
</script>

<style lang="scss" scoped>
@import "../assets/sass/_vars.scss";
// Title
.title-section {
  position: absolute;
  top: 0;
  left: 0;
  transform: translateY(-50%);
  z-index: 2;
}
// Card
.card {
  background-color: $bg-black;

  figure {
    width: 130px;
    overflow: hidden;
  }
  .description {
    color: #ffffff;
    text-transform: uppercase;
    font-weight: bold;
  }
}
// Button
.button-blue {
  text-transform: uppercase;
  padding: 10px 35px;
  background-color: $bg-blue;
  color: #ffffff;
  font-weight: bold;
  text-decoration: none;
  font-size: 0.8rem;
}
</style>