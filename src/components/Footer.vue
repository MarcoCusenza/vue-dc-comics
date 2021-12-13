<template>
  <footer>
    <div class="footer-top">
      <div class="card">
        <div class="icon">
          <img src="../assets/img/buy-comics-digital-comics.png" alt="" />
        </div>
        <div class="section-name">digital comics</div>
      </div>
      <div class="card">
        <div class="icon">
          <img src="../assets/img/buy-comics-merchandise.png" alt="" />
        </div>
        <div class="section-name">digital comics</div>
      </div>
      <div class="card">
        <div class="icon">
          <img src="../assets/img/buy-comics-digital-comics.png" alt="" />
        </div>
        <div class="section-name">digital comics</div>
      </div>
      <div class="card">
        <div class="icon">
          <img src="../assets/img/buy-comics-digital-comics.png" alt="" />
        </div>
        <div class="section-name">digital comics</div>
      </div>
      <div class="card">
        <div class="icon">
          <img src="../assets/img/buy-comics-digital-comics.png" alt="" />
        </div>
        <div class="section-name">digital comics</div>
      </div>
    </div>
    <div class="footer-mid"></div>
    <div class="footer-bot"></div>
  </footer>
</template>

<script>
export default {
  name: "Footer",
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
}

.card {
  height: 70%;
  display: flex;
  align-items: center;
  cursor: pointer;
}

.icon img {
  height: 60px;
}

.section-name {
  text-transform: uppercase;
  margin-left: 10px;
}
</style>