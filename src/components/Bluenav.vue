<template>
  <nav>
      <div class="container">
          <ul>
              <li v-for="(item, index) in li" :key="index">
                    <a href="#">
                        
                        <img :src="'../assets/' + item.linkImg" alt="">
                        {{item.text}}
                    </a>
                </li>
          </ul>
      </div>
  </nav>
</template>

<script>
export default {
  name: "Bluenav",
  data() {
      return {
          li: [
                {
                    text: "Digital Comics",
                    linkImg: "buy-comics-digital-comics.png",
                },
                {
                    text: "DC Merchandise",
                    linkImg: "buy-comics-marchandise.png",
                },
                {
                    text: "Subscription",
                    linkImg: "buy-comics-subscriptions.png",
                },
                {
                    text: "Comic Shop Locator",
                    linkImg: "buy-comics-shop-locator.png",
                },
                {
                    text: "DC Power Visa",
                    linkImg: "buy-comics-power-visa.svg",
                },
          ]
      }
  }
};
</script>

<style lang="scss" scoped>
@import "../style/vars.scss";
    nav {
        background-color: $blue;
        .container {
            height: 120px;
            display: flex;
            align-items: center;
        }
        ul {
            flex-grow: 1;
            display: flex;
            justify-content: space-evenly;
            list-style: none;
        }
        li {
            color: white;
            text-transform: uppercase;
        }
    }
</style>
