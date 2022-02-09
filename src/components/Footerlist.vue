<template>
  <div class="row">
    <div class="col-4 text-white">
      <!-- DC COMICS -->
      <h4 class="list-title">Dc Comics</h4>
      <ul>
        <li v-for="(link, index) in listLinks" :key="index">
          <a href="link.urk">{{ link.text }}</a>
        </li>
      </ul>
      <!-- DC SHOP -->
      <h4 class="list-title">Shop</h4>
      <ul>
        <li v-for="(element, index) in shopList" :key="index">
          <a href="element.url">
            {{ element.text }}
          </a>
        </li>
      </ul>
    </div>
    <div class="col-4 text-white">
      <!-- DC -->
      <h4 class="list-title">DC</h4>
      <ul>
        <li v-for="(element, index) in dcLinks" :key="index">
          <a href="element.url">
            {{ element.text }}
          </a>
        </li>
      </ul>
    </div>
    <div class="col-4 text-white">
      <!-- SITES -->
      <h4 class="list-title">SITES</h4>
      <ul>
        <li v-for="(element, index) in sitesList" :key="index">
          <a href="element.url">
            {{ element.text }}
          </a>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: "Footerlist",
  props: ["listLinks", "dcLinks", "sitesList"],
  data() {
    return {
      shopList: [
        { text: "Shop DC", url: "#", active: false },
        { text: "Shop DC Collectibles", url: "#", active: false },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/sass/_vars.scss";
.list-title {
  color: #fff;
  text-transform: uppercase;
  font-weight: bolder;
  font-size: 1.2rem;
}
ul {
  padding-left: 0;
}
ul li {
  list-style-type: none;
  list-style-position: inside;
  a {
    text-decoration: none;
    color: $color_grey;
    font-size: 0.7rem;
  }
}
</style>