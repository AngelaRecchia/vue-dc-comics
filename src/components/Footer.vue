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
          <div class="container"></div>
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
                height: 405px;
                padding: 50px 0;
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
                    margin: 10px 0;
                }
            }
            
        }
        footer {
            height: 90px;
            background-color: $grey;
        }
    }
</style>
