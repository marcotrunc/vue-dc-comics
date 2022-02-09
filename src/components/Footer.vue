<template>
  <footer class="container-fluid">
    <!-- Top footer -->
    <section id="footer-top">
      <div class="container flex">
        <div id="list-footer">
          <div class="col">
            <h4>Dc Comics</h4>
            <ul>
              <li v-for="(link, index) in listlinks" :key="index">
                <a href="link.url"> {{ link.text }}</a>
              </li>
            </ul>
            <h4>Shop</h4>
            <ul>
              <li><a href="#">Shop DC</a></li>
              <li><a href="#">Shop DC Collectibles</a></li>
            </ul>
          </div>
          <div class="col">
            <h4>DC</h4>
            <ul>
              <li v-for="(link, index) in dclinks" :key="index">
                <a :href="link.url">{{ link.text }}</a>
              </li>
            </ul>
          </div>
          <div class="col">
            <h4>SITES</h4>
            <ul>
              <li><a href="#">DC</a></li>
              <li><a href="#">MAD Magazine</a></li>
              <li><a href="#">DC Kids</a></li>
              <li><a href="#">DC Universe</a></li>
              <li><a href="#">DC Power Visa</a></li>
            </ul>
          </div>
        </div>
        <div id="logo-footer">
          <figure>
            <img src="../assets/img/dc-logo-bg.png" alt="Logo" />
          </figure>
        </div>
      </div>
    </section>
    <!-- Footer bottom -->
    <Footerbottom :socialimages="socialimages" />
  </footer>
</template>

<script>
import Footerbottom from "./Footerbottom.vue";
export default {
  name: "Footer",
  components: {
    Footerbottom,
  },
  data() {
    return {
      listlinks: [
        { text: "Characters", url: "#", active: false },
        { text: "Comics", url: "#", active: false },
        { text: "Movies", url: "#", active: false },
        { text: "TV", url: "#", active: false },
        { text: "Games", url: "#", active: false },
        { text: "Collectibles", url: "#", active: false },
        { text: "Videos", url: "#", active: false },
      ],
      dclinks: [
        { text: "Terms Of Use", url: "#" },
        { text: "Privacy policy (New)", url: "#" },
        { text: "Ad Choices", url: "#" },
        { text: "Advertising", url: "#" },
        { text: "Jobs", url: "#" },
        { text: "Subscriptions", url: "#" },
        { text: "Talent Workshops", url: "#" },
        { text: "CPSC Certificates", url: "#" },
        { text: "Ratings", url: "#" },
        { text: "Shop Help", url: "#" },
        { text: "Contact us", url: "#" },
      ],
      socialimages: [
        { url: "facebook" },
        { url: "twitter" },
        { url: "youtube" },
        { url: "pinterest" },
        { url: "periscope" },
      ],
    };
  },
};
</script>

<style lang ="scss" scoped>
// ** FOOTER TOP
#footer-top {
  background-image: url("../assets/img/footer-bg.jpg");
  overflow: hidden;
}
.flex {
  display: flex;
  justify-content: space-between;
}
// ** LIST FOOTER
@import "../assets/sass/_vars.scss";
#list-footer {
  padding: 35px 0;
  display: flex;
  justify-content: start;
  color: white;
}
.col {
  padding-right: 15px;
  h4 {
    margin: 10px 0px;
    text-transform: uppercase;
  }
  ul li {
    list-style-type: none;
    font-size: 0.8rem;
    margin: 5px 0;
    a {
      text-decoration: none;
      color: grey;
      margin: 10px 0;
    }
  }
}
// ** LOGO FOOTER
#logo-footer {
  width: 40%;
  position: relative;
  figure {
    overflow: hidden;
  }
}
#logo-footer img {
  position: absolute;
  top: 50%;
  right: 0;
  transform: translate(0, -50%);
}
</style>