<template>
  <div class="footer">
    <!--social links-->
    <div class="wrapper-social-links">
    <template v-for="link in links">
      <div class="social-links" :key="link.id">
      <a :href="link.link">
      <img :src="require('@/assets/icon__' + link.icon + '.svg')">
      </a>
      </div>
    </template>
    </div>
    <!--copyright text-->
    <p>{{ copyright }}</p>
  </div>
</template>

<script>
export default {
  name: "Footer",
  data() {
    return {
      copyright: "Copyright © 2018 Jason Media. All rights reserved.",
      links: [
        {
          link:
            "https://open.spotify.com/user/113261523?si=G0iggm-kRhe7WqHbJXMKyg",
          icon: "spotify"
        },
        {
          link: "https://www.linkedin.com/in/jasonpknott/",
          icon: "linkedin"
        },
        {
          link: "https://www.instagram.com/notjasonknott/?hl=en",
          icon: "instagram"
        },
        {
          link: "https://www.facebook.com/jason.knott.332",
          icon: "facebook"
        }
      ]
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
.wrapper-social-links {
  display: flex;
  justify-content: center;
  width: 100%;
}
.social-links {
  display: inline;
  margin: 0.5rem;
}
.footer {
  margin-top: 5%;
}
</style>
