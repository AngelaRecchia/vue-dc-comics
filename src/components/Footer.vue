<template>
  <section>
      <main>
          <div class="container">
              <div class="lists" v-for="(list, index) in siteMap" :key="index">
                  <h3>{{list.title}}</h3>
                  <ul>
                      <li v-for="(elem, jindex) in list.elements" :key="jindex" class="listElem"><a href="elem.link">{{elem.text}}</a></li>
                  </ul>
              </div>
          </div>
      </main>
      <footer>
          <div class="container">
              <a href="#"><div class="btn">Sign-up now!</div></a>
              <div id="social">
                  <span>Follow Us</span>
                  <a href="#"><img src="../assets/img/footer-facebook.png" alt="fb icon"></a>
                  <a href="#"><img src="../assets/img/footer-twitter.png" alt="twitter icon"></a>
                  <a href="#"><img src="../assets/img/footer-youtube.png" alt="youtube icon"></a>
                  <a href="#"><img src="../assets/img/footer-pinterest.png" alt="pinterest icon"></a>
                  <a href="#"><img src="../assets/img/footer-periscope.png" alt="periscope icon"></a>
              </div>
          </div>
      </footer>
  </section>
</template>

<script>
import SiteMap from "@/data/SiteMap.js";
export default {
  name: "Footer",
  data() {
      return {
          siteMap: SiteMap,
      }
  }
};
</script>

<style lang="scss" scoped>
    @import "../style/vars.scss";
    @import "../style/mixins.scss";
    section {
        main {
            background: url("../assets/img/footer-bg.jpg") no-repeat;
            background-size: cover;
            
            .container {
                height: 410px;
                padding: 40px 0 20px;
                background: url("../assets/img/dc-logo-bg.png") no-repeat right;
                background-size: 60%;
                display: flex;
                flex-direction: column;
                flex-wrap: wrap;
                align-content: flex-start;
                .lists {
                    width: 200px;
                }
                h3 {
                    font-size: 30px;
                    text-transform: uppercase;
                    color: white;
                }

                ul {
                    list-style: none;
                    color: grey;
                    display: inline-block;
                    margin: 5px 0;
                    li {
                        margin: 3px 0;
                    }
                }
            }
            
        }
        footer {
            background-color: $grey;
            .container {
                height: 100px;
                display: flex;
                justify-content: space-between;
                align-items: center;
                .btn {
                    @include btn(transparent, 20px, 10px 15px);
                }
                #social {
                    display: flex;
                    align-items: center;
                    span {
                        font-size: 26px;
                        color: $blue;
                        font-weight: bold;
                        text-transform: uppercase;
                        margin-right: 20px;
                    }
                    a {
                        margin: 0 10px;
                    }
                }
            }
           
        }
    }
</style>
