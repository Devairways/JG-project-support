<template>
  <Header />
  <about></about>
  <services></services>
  <contact></contact>
  <Footer />
</template>

<script>
import Header from "./layout/Header.vue";
import Footer from "./layout/Footer.vue";

import About from "./view/About.vue";
import Services from "./view/Services.vue";
import Contact from "./view/Contact.vue";

export default {
  name: "App",
  components: { Header, Footer, About, Services, Contact },
};
</script>

<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Poppins&display=swap");
@import "./assets/scss/variable.scss";

body {
  margin: 0;
}
#app {
  font-family: "Poppins", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;

  .header {
    font-size: 2rem;
    font-weight: bolder;
    line-height: 2.5rem;
    background: linear-gradient(35deg, #000 40%, #ff4d58 0);
    color: transparent;
    background-clip: text;
    text-transform: capitalize;
    width: fit-content;
    padding-left: 20px;
  }

  .subtext {
    text-align: start;
    padding-left: 20px;
  }

  .container {
    width: 90%;
    max-width: 1200px;
    margin: auto;
  }

  section {
    margin-top: 35px;
    margin-bottom: 35px;
  }

  p {
    color: #8c8c8c;
  }

  ul {
    list-style: none;
    padding: 0;
  }
}
</style>
