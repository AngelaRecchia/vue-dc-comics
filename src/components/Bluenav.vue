<template>
  <nav>
      <div class="container">
          <ul>
              <li v-for="(item, index) in li" :key="index">
                    <a href="#">
                        
                        <img :src="publicPath + 'img/' + item.linkImg" alt="">
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
          publicPath: process.env.BASE_URL,
          li: [
                {
                    text: "Digital Comics",
                    linkImg: "buy-comics-digital-comics.png",
                },
                {
                    text: "DC Merchandise",
                    linkImg: "buy-comics-merchandise.png",
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
                    linkImg: "buy-dc-power-visa.svg",
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
            white-space: nowrap;
            display: flex;
            align-items: center;
            img {
                max-height: 50px;
                max-width: 50px;
                margin-right: 5px;
                vertical-align: middle;
            }
        }
    }
</style>
