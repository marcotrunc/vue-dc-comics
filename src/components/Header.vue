<template>
  <div class="container-fluid">
    <header class="container">
      <div id="header-left">
        <a href="#">
          <img src="../assets/img/dc-logo.png" alt="" />
        </a>
      </div>
      <div id="header-right">
        <ul>
          <li
            v-for="(link, index) in headLinks"
            :key="index"
            @click="setActive(link)"
          >
            <a href="#" :class="{ active: link.active }">{{ link.text }}</a>
          </li>
        </ul>
      </div>
    </header>
  </div>
</template>

<script>
export default {
  name: "Header",
  data() {
    return {
      headLinks: [
        { text: "Characters", url: "#", active: false },
        { text: "Comics", url: "#", active: false },
        { text: "Movies", url: "#", active: false },
        { text: "TV", url: "#", active: false },
        { text: "Games", url: "#", active: false },
        { text: "Collectibles", url: "#", active: false },
        { text: "Videos", url: "#", active: false },
        { text: "Fans", url: "#", active: false },
        { text: "News", url: "#", active: false },
        { text: "Shop", url: "#", active: false },
      ],
    };
  },
  methods: {
    setActive(link) {
      if (link.active === false) {
        console.log("ciao");
        this.headLinks.map((item) => {
          item.active = false;
        });
        link.active = true;
      }
    },
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/sass/_vars.scss";
header {
  padding: 10px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: $bg_white;
}
#header-left {
  width: 5%;
}
#header-right {
  ul li {
    list-style-type: none;
    display: inline-block;
    padding: 0 10px;
    a {
      text-decoration: none;
      text-transform: uppercase;
      padding: 30px 0;
      color: black;
      font-size: 0.7rem;
      &:hover {
        color: $color_blue;
        border-bottom: 3px solid $color_blue;
      }
    }
  }
}
</style>