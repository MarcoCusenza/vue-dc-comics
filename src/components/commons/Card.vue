<template>
  <a class="card" href="#">
    <img :src="obj.thumb" :alt="obj.series" />
    <div class="text">{{ obj.series }}</div>
  </a>
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
  &:hover img {
    opacity: 1;
    transition: .5s
  }
  img {
    width: 80%;
    opacity: .9;
  }
  .text {
    width: 80%;
    margin-top: 5px;
    color: $light-text;
    font-size: 13px;
    text-transform: uppercase;
  }
}
</style>