<template>
  <footer class="container-fluid">
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
    <section id="footer-bottom">
      <div class="container flex align-items-center h-100">
        <div id="sign">
          <a href="#">sign-up now!</a>
        </div>
        <div id="social">
          <a href="#">Follow Us</a>
          <ul>
            <li v-for="(img, index) in socialimages" :key="index">
              <a href="#">
                <img
                  :src="require(`../assets/img/footer-${img.url}.png`)"
                  :alt="`${img.url}`"
                />
              </a>
            </li>
          </ul>
        </div>
      </div>
    </section>
  </footer>
</template>

<script>
export default {
  name: "Footer",
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
  padding: 25px 0;
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
    font-size: 0.7rem;
    color: grey;
    a {
      text-decoration: none;
      color: grey;
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
  top: 0;
  right: 0;
  transform: translateY(-30%);
}
// **FOOTER BOTTOM
#footer-bottom {
  background-color: $bg-grey;
  position: fixed;
  bottom: 0;
  left: 0;
  width: 100%;
  padding: 20px 0px;
}
#sign a,
#social a {
  text-transform: uppercase;
  padding: 5px 15px;
  font-size: 0.75rem;
  text-decoration: none;
}
#sign a {
  color: #ffffff;
  border: 2px solid #0282f9;
}
#social {
  display: flex;
  justify-content: space-between;
  align-items: center;
  a {
    color: #0282f9;
  }
  ul li {
    display: inline-block;
    width: 25px;
    margin: 0 5px;
  }
}
</style>