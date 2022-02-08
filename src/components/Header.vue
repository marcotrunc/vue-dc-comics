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
          <li><a href="#">Characters</a></li>
          <li><a href="#" class="active">Comics</a></li>
          <li><a href="#">Movies</a></li>
          <li><a href="#">TV</a></li>
          <li><a href="#">Games</a></li>
          <li><a href="#">Collectibles</a></li>
          <li><a href="#">Videos</a></li>
          <li><a href="#">Fans</a></li>
          <li><a href="#">News</a></li>
          <li><a href="#">Shop</a></li>
        </ul>
      </div>
    </header>
  </div>
</template>

<script>
export default {
  name: "Header",
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
      &:hover,
      &:active {
        color: $color_blue;
        border-bottom: 3px solid $color_blue;
      }
    }
  }
}
</style>