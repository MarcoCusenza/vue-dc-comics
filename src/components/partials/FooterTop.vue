<template>
  <!-- FOOTER TOP -->
  <div class="footer-top">
    <div class="container">
      <a
        class="card"
        v-for="(section, i) in sectionsBuy"
        :key="i"
        :href="section.url"
      >
        <div class="icon">
          <img :src="getImgUrl(section.image)" :alt="section.text" />
        </div>
        <div class="section-name">{{ section.text }}</div>
      </a>
    </div>
  </div>
</template>



<script>
export default {
  name: "FooterTop",
  data() {
    return {
      sectionsBuy: [
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
  background-color: $lightblue;
  color: $light-text;

  .container {
    height: 160px;
    display: flex;
    justify-content: space-around;
    align-items: center;
  }

  a {
    text-decoration: none;
    color: $light-text;
  }

  .card {
    height: 70%;
    display: flex;
    align-items: center;
    border-radius: 10px;
    padding: 50px 25px;
    cursor: pointer;

    &:hover {
      background-color: #0d6ac7;
      transition: 0.4s;
    }

    .icon {
      img {
        height: 55px;
      }
    }

    &:last-of-type .icon img {
      height: 40px;
    }

    .section-name {
      font-size: 15px;
      text-transform: uppercase;
      margin-left: 10px;
    }
  }
}
</style>


