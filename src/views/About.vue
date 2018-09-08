<template>
  <div class="home">
    <div class="main-section-wrapper">
      <div class="content-column">
      <!--my image-->
      <img class="content__jason-image" alt="Jason profile" src="../assets/mischief.png">
      <!--my description-->
      <div>
        <p class="section-title" v-text="description"></p>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt
           ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation 
           ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in 
           reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur 
           sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id 
           est laborum.</p>
      </div>
      <div>
        <!--founded section-->
        <p class="section-title" v-text="founded"></p>
        <div class="founded__company-logos--wrapper">
        <template v-for="company in companies">
          <div class="founded__company-logos" :key="company.id">
          <img :src="require('@/assets/' + company.logo)">
          <p v-text="company.name"></p>
          </div>
        </template>
        </div>
      </div>
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: "home",
  data() {
    return {
      description: "UX/UI Designer | Startup Founder",
      founded: "Founded",
      companies: [
        {
          logo: "logo__chillabit.png",
          name: "Chillabit | First employee"
        },
        {
          logo: "logo__coin-and-crypto.svg",
          name: "Coin and Crypto"
        }
      ]
    };
  }
};
</script>

<style lang="scss" scoped>
.founded__company-logos--wrapper {
  display: flex;
  flex-flow: row wrap;
  justify-content: center;
}

.founded__company-logos {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  height: 150px;
  align-items: center;
  margin: 0 1.5rem;
  & > img {
    height: 96px;
    max-width: 96px;
  }
  & > p {
    margin: auto;
  }
}

.content__jason-image {
  width: 100%;
}

.main-section-wrapper {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.main-section-wrapper > .content-column {
  max-width: 40rem;
  text-align: initial;
}

.content-column > * {
  margin: 0.6rem 0rem;
  &:first-child {
    margin-top: 0;
  }
}

.section-title {
  border: 1px solid black;
  padding: 0.2rem;
  text-align: center;
  margin-bottom: 1.5rem;
}

p {
  margin-bottom: 3rem;
}
</style>
