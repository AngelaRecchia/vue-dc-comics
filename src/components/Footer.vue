<template>
  <section>
      <main>
          <div class="container"></div>
      </main>
      <footer>
          <div class="container"></div>
      </footer>
  </section>
</template>

<script>
export default {
  name: "Footer",
};
</script>

<style lang="scss" scoped>
    section {
        main {
            height: 300px;
            background: url("../assets/img/footer-bg.jpg") no-repeat;
            background-size: cover;
            .container {
                height: 100%;
                background: url("../assets/img/dc-logo-bg.png") no-repeat right;
                background-size: 60%;
            }
            
        }
        footer {
            height: 90px;
            background-color: #303030;
        }
    }
</style>
