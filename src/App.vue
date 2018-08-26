<template>
  <div id="app">
    <div class="outer-wrapper">
      <div class="wrapper">

    <!-- header navbar -->
      <header id="header">
        <nav id="main-navigation" class="main-nav">
        <div id="logo-wrapper">
          <img alt="Jason logo" src="@/assets/logo.svg">
        </div>
        <div id="nav-wrapper">
          <router-link to="/">Home</router-link> |
          <router-link to="/about">About</router-link>
        </div>
        </nav>
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

export default {
  components: {
    FooterSection
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

#header {
  position: fixed;
  top: 0;
  left: auto;
  margin: 0 auto;
  width: 1118px;
  padding: 40px 0 0;
  z-index: 1800;
  background-color: white;
}

#main-navigation {
  z-index: 500;
}

#nav-wrapper {
  padding: 30px;
  a {
    font-weight: bold;
    color: #2c3e50;
    &.router-link-exact-active {
      color: #42b983;
    }
  }
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
