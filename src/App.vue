<template>
  <div id="app">
    <div class="outer-wrapper">
      <div class="wrapper">

    <!-- header navbar -->
      <header id="header">
      <header-section/>
      </header>

    <!-- content -->
        <div class="content-inner-wrapper">
          <div class="main-content-wrapper">
            <router-view/>
          </div>
        </div>
      </div>
      <!-- end of .wrapper-->

    <footer id="footer">
      <footer-section/>
    </footer>
    </div>
    <!-- end of .outer-wrapper-->
  </div>
</template>

<script>
import FooterSection from "./components/Footer.vue";
import HeaderSection from "./components/Header.vue";

export default {
  components: {
    FooterSection,
    HeaderSection
  }
};
</script>


<style lang="scss">
body {
  height: 50%;
  color: #ffffff;
  margin: 0px;
  padding: 0px;
}
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.outer-wrapper {
  padding: 0;
  width: 1118px;
  margin: 0 auto;
  position: relative;
}

.outer-wrapper > .wrapper {
  padding: 0;
  background-color: #fff;
  position: relative;
}

.content-inner-wrapper {
  margin-top: 252px;
}

#footer {
  margin: 0 auto;
  padding: 45px 75px;
  background-color: #fff;
  position: relative;
}
</style>
