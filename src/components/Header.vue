<template>
  <div id="header">
    <nav id="main-navigation" class="main-nav">
    <div id="logo-wrapper">
        <img alt="Jason logo" src="@/assets/logo.svg">
    </div>
    <div id="nav-wrapper">
        <router-link to="/">Home</router-link> |
        <router-link to="/about">About</router-link>
    </div>
    </nav>
  </div>
</template>

<script>
export default {
  name: "Header",
  data() {
    return {

    };
  }
};
</script>

<style lang="scss" scoped>

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

</style>
