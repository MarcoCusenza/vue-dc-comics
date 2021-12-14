<template>
  <header>
    <div class="container">
      <div class="logo">
        <img src="../../assets/img/dc-logo.png" alt="Logo DC" />
      </div>
      <nav>
        <ul>
          <li v-for="(link, i) in links" :key="i">
            <a :href="link.url">{{ link.text }}</a>
          </li>
        </ul>
      </nav>
    </div>
  </header>
</template>



<script>
export default {
  name: "Header",
  data() {
    return {
      //DATI COMPONENTE
      links: [
        {
          text: "characters",
          url: "#",
          current: false,
        },
        {
          text: "comics",
          url: "#",
          current: false,
        },
        {
          text: "movies",
          url: "#",
          current: false,
        },
        {
          text: "tv",
          url: "#",
          current: false,
        },
        {
          text: "games",
          url: "#",
          current: false,
        },
        {
          text: "collectibles",
          url: "#",
          current: false,
        },
        {
          text: "videos",
          url: "#",
          current: false,
        },
        {
          text: "fans",
          url: "#",
          current: false,
        },
        {
          text: "news",
          url: "#",
          current: false,
        },
        {
          text: "shop",
          url: "#",
          current: false,
        },
      ],
    };
  },
};
</script>



<style lang="scss" scoped>
@import "../../assets/style/partials/variables.scss";

header {
  background-color: $light;

  .container {
    height: 100px;
    display: flex;
    justify-content: space-between;
    align-items: center;

    img {
      margin-left: 30px;
      height: 70px;
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
          font-size: 14px;
          text-decoration: none;
          font-weight: bold;
          color: #494949;
        }
      }
    }
  }
}
</style>