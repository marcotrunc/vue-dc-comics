<template>
  <div>
    <section id="footer-bottom">
      <div class="container d-flex align-items-center justify-content-between">
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
  </div>
</template>

<script>
export default {
  name: "Footerbottom",
  props: ["socialimages"],
};
</script>

<style lang="scss" scoped>
// **FOOTER BOTTOM
@import "../assets/sass/_vars.scss";
#footer-bottom {
  background-color: $bg-grey;
  padding: 35px 0px;
}

#sign a,
#social a {
  text-transform: uppercase;
  padding: 10px 20px;
  font-size: 1rem;
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
    width: 35px;
    margin: 0 5px;
  }
}
</style>