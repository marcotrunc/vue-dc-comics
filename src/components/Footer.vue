<template>
  <footer class="container-fluid">
    <!-- Top footer -->
    <section id="footer-top" class="container-fluid py-5">
      <div class="container">
        <div class="row">
          <div class="col-6">
            <Footerlist
              :list-links="listlinks"
              :dc-links="dclinks"
              :sites-list="siteslist"
            />
          </div>
          <div class="col-6">
            <div id="logo-footer">
              <img src="../assets/img/dc-logo-bg.png" alt="Logo" />
            </div>
          </div>
        </div>
      </div>
    </section>
    <!-- Footer bottom -->
    <Footerbottom :socialimages="socialimages" />
  </footer>
</template>

<script>
import Footerlist from "./Footerlist.vue";
import Footerbottom from "./Footerbottom.vue";
export default {
  name: "Footer",
  components: {
    Footerbottom,
    Footerlist,
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
      siteslist: [
        { text: "DC", url: "#" },
        { text: "MAD Magazine", url: "#" },
        { text: "DC kids", url: "#" },
        { text: "DC Universe", url: "#" },
        { text: "DC Power Visa", url: "#" },
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
// ** LOGO FOOTER
#logo-footer {
  position: relative;
  height: 100%;
}
#logo-footer img {
  position: absolute;
  top: 50%;
  right: 0;
  transform: translateY(-50%);
}
</style>