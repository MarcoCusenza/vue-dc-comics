<template>
  <main>
    <div class="container">
      <div class="wip">--> Content goes here</div>
    </div>
  </main>
</template>

<script>
export default {
  name: "Main",
};
</script>

<style lang="scss" scoped>
@import "../assets/style/partials/variables.scss";

main {
  line-height: 120px;
  background-color: $darkest;
  color: $light-text;
  font-size: 30px;
  text-align: center;
}
</style>