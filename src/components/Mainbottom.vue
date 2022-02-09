<template>
  <div>
    <div class="container">
      <div class="row justify-content-between">
        <div
          v-for="(item, index) in mainFunctionsList"
          :key="index"
          class="col-2 d-flex align-items-center"
        >
          <div class="figure">
            <img :src="require(`../assets/img/${item.url}`)" :alt="item.alt" />
          </div>
          <span class="fs-8 text-white">{{ item.text }}</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Mainbottom",
  data() {
    return {
      mainFunctionsList: [
        {
          url: "buy-comics-digital-comics.png",
          alt: "Digital-comics",
          text: "DIGITALS COMICS",
        },
        {
          src: "buy-comics-merchandise.png",
          alt: "DC maerchandise",
          text: "DC MERCHANDISE",
        },
        {
          src: "buy-comics-subscriptions.png",
          alt: "subscriptions",
          text: "SUBSCRIPTIONS",
        },
        {
          src: "buy-comics-shop-locator.png",
          alt: "shop locator",
          text: "COMIC SHOP LOCATOR",
        },
        {
          src: "buy-dc-power-visa.svg",
          alt: "DC power",
          text: "DC POWER",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.figure {
  width: 30px;
  margin-right: 10px;
}
</style>