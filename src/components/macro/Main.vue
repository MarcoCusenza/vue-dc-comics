<template>
  <main>
    <div class="jumbo"></div>
    <div class="container">
      <MainSeries />
    </div>
  </main>
</template>

<script>
import MainSeries from "../sections/MainSeries.vue";

export default {
  name: "Main",
  components: {
    MainSeries,
  },
};
</script>

<style lang="scss" scoped>
@import "../../assets/style/partials/variables.scss";

main {
  .jumbo {
    height: 360px;
    width: 100%;
    background-image: url("../../assets/img/jumbotron.jpg");
    background-size: cover;
  }
}
</style>