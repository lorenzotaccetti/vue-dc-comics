<template>
  <div id="app">
    <Header />
    <MainContent />
    <InfoArea />
    <Footer />
  </div>
</template>

<script>
import Header from "../components/Header.vue";
import MainContent from "../components/MainContent.vue";
import InfoArea from "../components/InfoArea.vue";
import Footer from "../components/Footer.vue";

export default {
  name: "App",
  components: {
    Header,
    MainContent,
    InfoArea,
    Footer
  },
};
</script>

<style lang="scss">
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
</style>
