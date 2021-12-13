<template>
  <header>
    <div class="logo">
      <img src="../assets/img/dc-logo.png" alt="Logo DC" />
    </div>
    <nav>
      <ul>
        <li>
          <a href="#">characters</a>
        </li>
        <li>
          <a href="#">comics</a>
        </li>
        <li>
          <a href="#">movies</a>
        </li>
        <li>
          <a href="#">tv</a>
        </li>
        <li>
          <a href="#">games</a>
        </li>
        <li>
          <a href="#">collectibles</a>
        </li>
        <li>
          <a href="#">videos</a>
        </li>
        <li>
          <a href="#">fans</a>
        </li>
        <li>
          <a href="#">news</a>
        </li>
        <li>
          <a href="#">shop</a>
        </li>
      </ul>
    </nav>
  </header>
</template>



<script>
export default {
  name: "Header",
};
</script>



<style lang="scss" scoped>
@import "../assets/style/partials/variables.scss";

header {
  height: 100px;
  display: flex;
  justify-content: space-between;
  align-items: center;

  img {
    margin-left: 30px;
    transform: scale(0.8);
  }

  nav {
    ul {
      list-style: none;
      display: flex;
    }

    li {
      margin: 0 10px;
      text-transform: uppercase;

      a {
        text-decoration: none;
        font-weight: bold;
        color: #494949;
      }
    }
  }
}
</style>