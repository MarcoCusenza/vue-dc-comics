/* ---------------
HTML
----------------*/
<template>
  <footer>
    <!-- FOOTER TOP -->
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

    <!-- FOOTER MID -->
    <div class="footer-mid">
      <div class="container">
        <img
          id="dc-logo-bg"
          src="../assets/img/dc-logo-bg.png"
          alt="DC Logo Background"
        />
        <div class="links">
          <div class="col col-left">
            <div class="section foot-dc-comics">
              <h4>dc comics</h4>
              <ul>
                <li v-for="(el, i) in footDcCom" :key="i">
                  <a :href="el.url">{{ el.text }}</a>
                </li>
              </ul>
            </div>
            <div class="section foot-shop">
              <h4>shop</h4>
              <ul>
                <li v-for="(el, i) in footShop" :key="i">
                  <a :href="el.url">{{ el.text }}</a>
                </li>
              </ul>
            </div>
          </div>

          <div class="col col-mid">
            <div class="section foot-dc">
              <h4>dc comics</h4>
              <ul>
                <li v-for="(el, i) in footDc" :key="i">
                  <a :href="el.url">{{ el.text }}</a>
                </li>
              </ul>
            </div>
          </div>

          <div class="col col-right">
            <div class="section foot-sites">
              <h4>sites</h4>
              <ul>
                <li v-for="(el, i) in footSites" :key="i">
                  <a :href="el.url">{{ el.text }}</a>
                </li>
              </ul>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="footer-bot">
      <div class="container">
        <a href="#" class="signup">sign-up now!</a>
        <div class="socials">
          <div class="follow-us">follow us</div>
          <a
            v-for="(social, i) in socials"
            :key="i"
            :href="social.url"
            class="social"
          >
            <img :src="getImgUrl(social.image)" :alt="social.name" />
          </a>
        </div>
      </div>
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
      socials: [
        {
          name: "facebook",
          image: "footer-facebook.png",
          url: "#",
        },
        {
          name: "twitter",
          image: "footer-twitter.png",
          url: "#",
        },
        {
          name: "youtube",
          image: "footer-youtube.png",
          url: "#",
        },
        {
          name: "pinterest",
          image: "footer-pinterest.png",
          url: "#",
        },
        {
          name: "periscope",
          image: "footer-periscope.png",
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
    height: 160px;
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
        height: 55px;
      }
    }

    &:last-of-type .icon img {
      height: 40px;
    }

    .section-name {
      font-size: 15px;
      text-transform: uppercase;
      margin-left: 10px;
    }
  }
}

/* -------
FOOTER MID
------- */
.footer-mid {
  background-image: url("../assets/img/footer-bg.jpg");
  position: relative;
  z-index: -2;

  #dc-logo-bg {
    position: absolute;
    right: 200px;
    transform: translate(0, -20%);
    overflow: hidden;
    z-index: -1;
  }

  .links {
    display: flex;
    padding: 50px 0;

    .col {
      width: 170px;

      .section {
        margin: 10px 0;

        h4 {
          color: $light-text;
          text-transform: uppercase;
          font-size: 20px;
        }

        ul {
          list-style: none;
          margin: 10px 0;

          li {
            a {
              font-size: 14px;
              text-decoration: none;
              color: $medium-text;

              &:hover {
                color: $medium-text-hover;
              }
            }
          }
        }
      }
    }
  }
}

/* -------
FOOTER BOT
------- */
.footer-bot {
  background-color: $dark;

  .container {
    height: 110px;
    display: flex;
    justify-content: space-between;
    align-items: center;

    .signup {
      text-transform: uppercase;
      text-decoration: none;
      font-weight: bold;
      border: 2px solid $lightblue;
      padding: 15px 20px;
      color: $light-text;
    }

    .socials {
      display: flex;
      align-items: center;

      .follow-us {
        text-transform: uppercase;
        color: $lightblue;
        font-size: 20px;
        font-weight: bold;
        margin-right: 20px;
      }

      .social {
        margin: 0 10px;
      }
    }
  }
}
</style>