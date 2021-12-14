<template>
  <!-- FOOTER BOT -->
  <div class="footer-bot">
    <div class="container">
      <a href="#" class="signup">sign-up now!</a>
      <div class="socials">
        <div class="follow-us">follow us</div>
        <a
          v-for="(social, i) in socials"
          :key="i"
          :href="social.url"
          class="social"
        >
          <img :src="getImgUrl(social.image)" :alt="social.name" />
        </a>
      </div>
    </div>
  </div>
</template>



<script>
export default {
  name: "FooteBot",

  data() {
    return {
      socials: [
        {
          name: "facebook",
          image: "footer-facebook.png",
          url: "#",
        },
        {
          name: "twitter",
          image: "footer-twitter.png",
          url: "#",
        },
        {
          name: "youtube",
          image: "footer-youtube.png",
          url: "#",
        },
        {
          name: "pinterest",
          image: "footer-pinterest.png",
          url: "#",
        },
        {
          name: "periscope",
          image: "footer-periscope.png",
          url: "#",
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

.footer-bot {
  background-color: $dark;

  .container {
    height: 110px;
    display: flex;
    justify-content: space-between;
    align-items: center;

    .signup {
      text-transform: uppercase;
      text-decoration: none;
      font-weight: bold;
      border: 2px solid $lightblue;
      padding: 15px 20px;
      color: $light-text;
    }

    .socials {
      display: flex;
      align-items: center;

      .follow-us {
        text-transform: uppercase;
        color: $lightblue;
        font-size: 20px;
        font-weight: bold;
        margin-right: 20px;
      }

      .social {
        margin: 0 10px;
      }
    }
  }
}
</style>