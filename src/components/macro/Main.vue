<template>
  <main>
    <div class="jumbo"></div>
    <div class="container"></div>
  </main>
</template>

<script>
export default {
  name: "Main",
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