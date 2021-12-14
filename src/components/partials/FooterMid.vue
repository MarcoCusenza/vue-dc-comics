<template>
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
</template>

<script>
export default {
  name: "FooterMid",

  data() {
    return {
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
};
</script>



<style lang="scss" scoped>
@import "../assets/style/partials/variables.scss";

.footer-mid {
  background-image: url("../assets/img/footer-bg.jpg");
  position: relative;
  z-index: -2;

  .container {
    position: relative;
    z-index: -2;
  }

  #dc-logo-bg {
    position: absolute;
    right: 0px;
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
</style>