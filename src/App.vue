<template>
  <div id="app">
    <HeaderDriving />
    <MainDriving />
    <FooterDriving />
  </div>
</template>

<script>
import HeaderDriving from "./components/HeaderDriving.vue";
import MainDriving from "./components/MainDriving.vue";
import FooterDriving from "./components/FooterDriving.vue";

export default {
  name: "App",
  components: {
    HeaderDriving,
    MainDriving,
    FooterDriving,
  },
};
</script>

<style lang="scss">
* {
  margin: 0px;
  padding: 0px;
  box-sizing: border-box;
  font-family: "Roboto", sans-serif;
  scroll-behavior: smooth;
}

html {
  scroll-behavior: smooth;
}

.container {
  width: 75%;
  margin: auto;
}
</style>
