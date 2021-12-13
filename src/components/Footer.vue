<template>
  <footer>
    <div class="footer-top">
      <a
        :href="section.url"
        class="card"
        v-for="(section, i) in sections"
        :key="i"
      >
        <div class="icon">
          <img :src="getImgUrl(section.image)" :alt="section.text" />
        </div>
        <div class="section-name">{{ section.text }}</div>
      </a>
    </div>
    <div class="footer-mid"></div>
    <div class="footer-bot"></div>
  </footer>
</template>

<script>
export default {
  name: "Footer",
  data() {
    return {
      sections: [
        {
          url: "#",
          text: "digital comics",
          image: "buy-comics-digital-comics.png",
        },
        {
          url: "#",
          text: "dc merchandise",
          image: "buy-comics-merchandise.png",
        },
        {
          url: "#",
          text: "subscription",
          image: "buy-comics-subscriptions.png",
        },
        {
          url: "#",
          text: "comic shop locator",
          image: "buy-comics-shop-locator.png",
        },
        {
          url: "#",
          text: "dc power visa",
          image: "buy-dc-power-visa.svg",
        },
      ],
    };
  },
  methods: {
    getImgUrl(img) {
      return require("../assets/img/" + img);
    },
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/style/partials/variables.scss";

.footer-top {
  height: 200px;
  background-color: $lightblue;
  color: $light-text;
  display: flex;
  justify-content: space-around;
  align-items: center;

  .card {
    height: 70%;
    display: flex;
    align-items: center;
    cursor: pointer;

    .icon {
      img {
        height: 60px;
      }
    }

    .section-name {
      text-transform: uppercase;
      margin-left: 10px;
    }
  }
}
</style>