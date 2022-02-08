<template>
  <main class="container-fluid">
    <section id="main-top">
      <div class="container">
        <p>-->Content goes here--></p>
      </div>
    </section>
    <section id="main-bottom">
      <div class="container">
        <div id="cards">
          <div class="card">
            <figure>
              <img src="../assets/img/buy-comics-digital-comics.png" alt="" />
            </figure>
            <a href="#">Digital comics</a>
          </div>
          <div class="card">
            <figure>
              <img src="../assets/img/buy-comics-merchandise.png" alt="" />
            </figure>
            <a href="#">dc merchandise</a>
          </div>
          <div class="card">
            <figure>
              <img src="../assets/img/buy-comics-subscriptions.png" alt="" />
            </figure>
            <a href="#">subscription</a>
          </div>
          <div class="card">
            <figure>
              <img src="../assets/img/buy-comics-shop-locator.png" alt="" />
            </figure>
            <a href="#">comic shop locator</a>
          </div>
          <div class="card">
            <figure>
              <img src="../assets/img/buy-dc-power-visa.svg" alt="" />
            </figure>
            <a href="#">dc power visa</a>
          </div>
        </div>
      </div>
    </section>
  </main>
</template>

<script>
export default {
  name: "Main",
};
</script>

<style lang="scss" scoped>
@import "../assets/sass/_vars.scss";
// ** Main-top
#main-top {
  background-color: $bg-black;
}
#main-top .container {
  display: flex;
  align-content: center;
  padding: 40px 0px;
  p {
    color: #fff;
    font-size: 1.2rem;
    font-weight: bold;
  }
}
// ** Main-bottom
#main-bottom {
  background-color: $bg-blue;
  padding: 35px 0px;
}
#cards {
  display: flex;
  justify-content: space-around;
  align-items: center;
  .card {
    flex-basis: calc(100% / 5);
    display: flex;
    align-items: center;
    a {
      text-decoration: none;
      color: #ffffff;
      text-transform: uppercase;
      font-size: 0.7rem;
    }
  }
}

figure {
  width: 30px;
  margin-right: 10px;
}
</style>