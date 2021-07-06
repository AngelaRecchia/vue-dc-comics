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
              <a href="#"><div id="btn">Sign-up now!</div></a>
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
export default {
  name: "Footer",
  data() {
      return {
          siteMap: [
              {
                  title: "DC Comics",
                  elements: [
                      {
                          text: "Characters",
                          link: "#"
                      },
                      {
                          text: "Comics",
                          link: "#"
                      },
                      {
                          text: "Movies",
                          link: "#"
                      },
                      {
                          text: "TV",
                          link: "#"
                      },
                      {
                          text: "Games",
                          link: "#"
                      },
                      {
                          text: "Videos",
                          link: "#"
                      },
                      {
                          text: "News",
                          link: "#"
                      }
                  ],
              },
              {
                  title: "Shop",
                  elements: [
                      {
                          text: "Shop DC",
                          link: "#"
                      },
                      {
                          text: "Shop DC Collectibles",
                          link: "#"
                      }
                  ]
              },
              {
                  title: "DC",
                  elements: [
                      {
                          text: "Terms Of Use",
                          link: "#"
                      },
                      {
                          text: "Privacy Policy (New)",
                          link: "#"
                      },
                      {
                          text: "Ad Choices",
                          link: "#"
                      },
                      {
                          text: "Advertising",
                          link: "#"
                      },
                      {
                          text: "Jobs",
                          link: "#"
                      },
                      {
                          text: "Subscriptions",
                          link: "#"
                      },
                      {
                          text: "Talent Workshops",
                          link: "#"
                      },
                      {
                          text: "CPSC Certificates",
                          link: "#"
                      },
                      {
                          text: "Ratings",
                          link: "#"
                      },
                      {
                          text: "Shop Help",
                          link: "#"
                      },
                      {
                          text: "Contact Us",
                          link: "#"
                      }
                  ]
              },
              {
                  title: "Sites",
                  elements: [
                      {
                          text: "DC",
                          link: "#"
                      },
                      {
                          text: "MAD Magazine",
                          link: "#"
                      },
                      {
                          text: "DC Kids",
                          link: "#"
                      },
                      {
                          text: "DC Universe",
                          link: "#"
                      },
                      {
                          text: "DC Power Visa",
                          link: "#"
                      }
                  ]
              }
          ]
      }
  }
};
</script>

<style lang="scss" scoped>
    @import "../style/vars.scss";
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
                #btn {
                    color: white;
                    font-size: 20px;
                    font-weight: bold;
                    text-transform: uppercase;
                    padding: 10px 15px;
                    border: 2px solid $blue;
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
