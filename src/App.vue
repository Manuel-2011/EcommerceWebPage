<template>
  <v-app>
    <Header />
    <HomeComponent />
    <Intro />
    <Classes />
    <Contact />
    <Footer />
  </v-app>
</template>

<script>
import Footer from "./components/Footer";
import HomeComponent from "./components/Home.vue";
import Intro from "./components/Intro"
import Classes from "./components/Classes"
import Header from "./components/Header.vue";
import Contact from "./components/Contact";

export default {
  components: {
    Footer,
    HomeComponent,
    Header,
    Intro,
    Classes,
    Contact,
  },
};
</script>

<style lang="scss">
body {
  margin: 0;
  @media screen and (max-width: $breakpoint-tablet) {
    overflow-x: hidden;
  }
}
a {
  text-decoration: none;
  --v-anchor-base: $main-font-color;
}
</style>
