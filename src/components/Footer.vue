/* ---------------
HTML
----------------*/
<template>
  <footer>
    <div class="footer-top">
      <div class="container">
        <a
          class="card"
          v-for="(section, i) in sectionsBuy"
          :key="i"
          :href="section.url"
        >
          <div class="icon">
            <img :src="getImgUrl(section.image)" :alt="section.text" />
          </div>
          <div class="section-name">{{ section.text }}</div>
        </a>
      </div>
    </div>
    <div class="footer-mid">
      <div class="container">
        <div class="links">

          <div class="col-left">
            <div class="foot-dc-comics">
              <h4>dc comics</h4>
              <ul>
                <li v-for="(el, i) in footDcCom" :key="i">
                  <a href="">{{ el.text }}</a>
                </li>
              </ul>
            </div>
            <div class="foot-shop">
              <h4>shop</h4>
              <ul>
                <li v-for="(el, i) in footShop" :key="i">
                  <a href="">{{ el.text }}</a>
                </li>
              </ul>
            </div>
          </div>

          <div class="col-mid">
            <div class="foot-dc">
              <h4>dc comics</h4>
              <ul>
                <li v-for="(el, i) in footDc" :key="i">
                  <a href="">{{ el.text }}</a>
                </li>
              </ul>
            </div>
          </div>

          <div class="col-right">
            <div class="foot-sites">
              <h4>sites</h4>
              <ul>
                <li v-for="(el, i) in footSites" :key="i">
                  <a href="">{{el.text}}</a>
                </li>
              </ul>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="footer-bot">
      <div class="container"></div>
    </div>
  </footer>
</template>



/* ---------------
SCRIPT
----------------*/
<script>
export default {
  name: "Footer",
  data() {
    return {
      sectionsBuy: [
        {
          url: "#",
          text: "digital comics",
          image: "buy-comics-digital-comics.png",
        },
        {
          url: "#",
          text: "dc merchandise",
          image: "buy-comics-merchandise.png",
        },
        {
          url: "#",
          text: "subscription",
          image: "buy-comics-subscriptions.png",
        },
        {
          url: "#",
          text: "comic shop locator",
          image: "buy-comics-shop-locator.png",
        },
        {
          url: "#",
          text: "dc power visa",
          image: "buy-dc-power-visa.svg",
        },
      ],
      footDcCom: [
        {
          text: "Characters",
          url: "#",
        },
        {
          text: "Comics",
          url: "#",
        },
        {
          text: "Movies",
          url: "#",
        },
        {
          text: "TV",
          url: "#",
        },
        {
          text: "Games",
          url: "#",
        },
        {
          text: "Videos",
          url: "#",
        },
        {
          text: "News",
          url: "#",
        },
      ],
      footShop: [
        {
          text: "Shop DC",
          url: "#",
        },
        {
          text: "Shop DC Collectibles",
          url: "#",
        },
      ],
      footDc: [
        {
          text: "Terms Of Use",
          url: "#",
        },
        {
          text: "Privacy policy (New)",
          url: "#",
        },
        {
          text: "Ad Choices",
          url: "#",
        },
        {
          text: "Advertising",
          url: "#",
        },
        {
          text: "Jobs",
          url: "#",
        },
        {
          text: "Subrsciptions",
          url: "#",
        },
        {
          text: "Talent Workshops",
          url: "#",
        },
        {
          text: "CPSC Certificates",
          url: "#",
        },
        {
          text: "Ratings",
          url: "#",
        },
        {
          text: "Shop Help",
          url: "#",
        },
        {
          text: "Contact Us",
          url: "#",
        },
      ],
      footSites: [
        {
          text: "DC",
          url: "#",
        },
        {
          text: "MAD Magazine",
          url: "#",
        },
        {
          text: "DC Kids",
          url: "#",
        },
        {
          text: "DC Universe",
          url: "#",
        },
        {
          text: "DC Power Visa",
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



/* ---------------
CSS
----------------*/
<style lang="scss" scoped>
@import "../assets/style/partials/variables.scss";

/* -------
FOOTER TOP
------- */
.footer-top {
  background-color: $lightblue;
  color: $light-text;

  .container {
    height: 200px;
    display: flex;
    justify-content: space-around;
    align-items: center;
  }

  a {
    text-decoration: none;
    color: $light-text;
  }

  .card {
    height: 70%;
    display: flex;
    align-items: center;
    border-radius: 10px;
    padding: 50px 25px;
    cursor: pointer;

    &:hover {
      background-color: #0d6ac7;
      transition: 0.4s;
    }

    .icon {
      img {
        height: 60px;
      }
    }

    &:last-of-type .icon img {
      height: 45px;
    }

    .section-name {
      text-transform: uppercase;
      margin-left: 10px;
    }
  }
}

/* -------
FOOTER MID
------- */
.footer-mid {
}

/* -------
FOOTER BOT
------- */
.footer-bot {
}
</style>