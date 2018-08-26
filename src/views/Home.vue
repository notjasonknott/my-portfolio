<template>
  <div class="home">
    <img alt="Jason profile" src="../assets/mischief.png">
    <div class="main-section-wrapper">
      <div class="section-title" v-text="description"></div>
      <div class="section-title" v-text="founded"></div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: "home",
  data () {
    return {
      description: 'UX Design & Development | Startup Founder',
      founded: 'Founded'
    }
  }
};
</script>

<style lang="scss" scoped>

img {
  max-width: 40rem;
}

.main-section-wrapper {
  
}

.section-title {
  border: 1px solid black;
  padding: .2rem;
}

</style>

