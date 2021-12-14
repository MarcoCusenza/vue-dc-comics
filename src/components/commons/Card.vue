<template>
  <div class="card">
    <img :src="obj.thumb" :alt="obj.series" />
    <div class="text">{{ obj.series }}</div>
  </div>
</template>

<script>
export default {
  name: "Card",
  props: {
    obj: Object,
  },
};
</script>

<style lang="scss" scoped>
@import "../../assets/style/partials/variables.scss";

.card {
  img {
    height: 250px;
  }
  .text {
    color: $light-text;
    font-size: 13px;
    text-transform: uppercase;
  }
}
</style>