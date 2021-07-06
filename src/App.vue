/* Create un nuovo progetto utilizzando Vue CLI e definite i componenti
necessari per strutturare il layout come da screenshot allegato. Quando la
struttura a macroblocchi è pronta, popolate le voci di menu dinamicamente usando
i data del componente. Per oggi diamo priorità alla struttura: quando è tutto
bello solido, passiamo al Sass! Bonus: Creare un componente aggiuntivo per
gestire la fascia azzurra con le icone. */

<template>
  <div id="app">

    <Header/>
    <main>
      <Content/>
      <Bluenav/>
    </main>
    <Footer/>

  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Content from "./components/Content.vue";
import Bluenav from "./components/Bluenav.vue";
import Footer from "./components/Footer.vue";

export default {
  name: "App",
  components: {
    Header,
    Content,
    Bluenav,
    Footer,
  },
};
</script>

<style lang="scss">
  @import "style/commons.scss";
  @import "style/vars.scss";
</style>
