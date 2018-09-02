<template>
  <header id="header">
    <nav id="main-navigation" class="main-nav">
    <div 
    v-on:scroll="handleScroll" 
    :class="{'small': scrolled}" 
    class="logo-wrapper">
        <p v-if="scrolled" class="logo-text">JASON KNOTT</p>
        <img v-else alt="Jason logo" src="@/assets/logo.svg">
    </div>
    <div id="nav-wrapper">
      <div class="nav-links">
        <router-link to="/">Home</router-link>
        <router-link to="/about">About</router-link>
        <router-link to="/work">Work</router-link>
        <router-link to="/vlogs">Vlogs</router-link>

      </div>
    </div>
    </nav>
  </header>
</template>

<script>
export default {
  name: "Header",
  data() {
    return {
      scrolled: false
    };
  },
  methods: {
    handleScroll() {
      this.scrolled = window.pageYOffset > 38;
    }
  },
  created() {
    window.addEventListener("scroll", this.handleScroll);
  },
  destroyed() {
    window.removeEventListener("scroll", this.handleScroll);
  }
};
</script>

<style lang="scss" scoped>
.logo-wrapper {
  width: 100%;
  height: 60px;
  margin: 40px 0;
  transition: height 0.1s ease-in-out;

  & > img {
    height: 100%;
    width: auto;
  }
}

.logo-text {
  margin: 0;
  font-weight: bold;
  text-transform: uppercase;
}

.small {
  height: 10px;
}

#header {
  position: fixed;
  top: 0;
  left: auto;
  margin: 0 auto;
  width: 1118px;
  background: #fff;
  height: auto;
  padding: 20px 0 0;
  z-index: 1800;
}

.small {
  height: 20px;
  margin: 0px;
}

.main-nav {
  z-index: 500;
}

#nav-wrapper {
  display: flex;
  justify-content: center;
  max-height: 8em;
  padding: 30px;
}

.nav-links {
  margin-top: auto;

  > * {
    margin: 1rem 1rem 0 1rem;
  }
  a {
    font-weight: light;
    color: #000;
    text-decoration: none;
    display: inline-block;
    text-transform: uppercase;
    &.router-link-exact-active {
      color: #a59275;
    }
  }
}
</style>
