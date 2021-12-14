/* ---------------
HTML
----------------*/
<template>
  <footer>
    <FooterTop />
    <FooterMid />
    <FooterBot />
  </footer>
</template>



/* ---------------
SCRIPT
----------------*/
<script>
import FooterTop from "../sections/FooterTop.vue";
import FooterMid from "../sections/FooterMid.vue";
import FooterBot from "../sections/FooterBot.vue";

export default {
  name: "Footer",

  components: {
    FooterTop,
    FooterMid,
    FooterBot,
  },

  methods: {
    getImgUrl(img) {
      return require("../../assets/img/" + img);
    },
  },
};
</script>



/* ---------------
CSS
----------------*/
<style lang="scss" scoped>
@import "../../assets/style/partials/variables.scss";
</style>