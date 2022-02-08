<template>
  <footer class="container-fluid">
    <section id="footer-top">
      <div class="container flex">
        <div id="list-footer">
          <div class="col">
            <h4>Dc Comics</h4>
            <ul>
              <li><a href="#"></a>dasdas</li>
              <li><a href="#"></a>dasdas</li>
              <li><a href="#"></a>dasdas</li>
              <li><a href="#"></a>dasdas</li>
              <li><a href="#"></a>dasdas</li>
              <li><a href="#"></a>dasdas</li>
              <li><a href="#"></a>dasdas</li>
            </ul>
            <h4>Shop</h4>
            <ul>
              <li><a href="#"></a>dasdas</li>
              <li><a href="#"></a>dasdas</li>
            </ul>
          </div>
          <div class="col">
            <h4>DC</h4>
            <ul>
              <li>Terms of Use</li>
              <li>dadsadsa</li>
              <li>dadsadsa</li>
              <li>dadsadsa</li>
              <li>dadsadsa</li>
              <li>dadsadsa</li>
              <li>dadsadsa</li>
              <li>dadsadsa</li>
              <li>dadsadsa</li>
              <li>dadsadsa</li>
              <li>dadsadsa</li>
            </ul>
          </div>
          <div class="col">
            <h4>Sites</h4>
            <ul>
              <li>Terms of Use</li>
              <li>dadsadsa</li>
              <li>dadsadsa</li>
              <li>dadsadsa</li>
              <li>dadsadsa</li>
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
            <li>
              <a href="#"
                ><img src="../assets/img/footer-facebook.png" alt=""
              /></a>
            </li>
            <li>
              <a href="#"
                ><img src="../assets/img/footer-twitter.png" alt=""
              /></a>
            </li>
            <li>
              <a href="#"
                ><img src="../assets/img/footer-youtube.png" alt=""
              /></a>
            </li>
            <li>
              <a href="#"
                ><img src="../assets/img/footer-pinterest.png" alt=""
              /></a>
            </li>
            <li>
              <a href="#"
                ><img src="../assets/img/footer-periscope.png" alt=""
              /></a>
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
  }
  ul li {
    list-style-type: none;
    font-size: 0.7rem;
    color: grey;
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
  height: 100px;
}
#sign a,
#social a {
  text-transform: uppercase;
  padding: 10px 15px;
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