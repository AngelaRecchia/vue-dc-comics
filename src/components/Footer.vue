<template>
  <section>
      <main></main>
      <footer></footer>
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
            background: url("../assets/img/dc-logo-bg.png") no-repeat right, url("../assets/img/footer-bg.jpg");
        }
        footer {
            height: 90px;
            background-color: #303030;
        }
    }
</style>
