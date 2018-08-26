<template>
  <div class="home">
    <div class="main-section-wrapper">
      <div class="content-column">
      <!--my image-->
      <img class="content__jason-image" alt="Jason profile" src="../assets/mischief.png">
      <!--my description-->
      <div>
        <p class="section-title" v-text="description"></p>
        <p>In January of 2011, the first episode of Soulection Radio aired one hour outside of Los Angeles
           on Long Beach college radio station, KBEACH and 175 shows later, Soulection made the progression 
           to London-based Rinse.fm to expand the brand further worldwide lead by Soulection’s Head A&R, Co-Founder 
           and radio show host/creator Joe Kay. Shortly after, Red Bull Studios LA opened up their doors to 
           help us take Soulection Radio and our creative collaborations to the next level. July 4, 2015 marks the 
           first day of Soulection Radio broadcasting to over 100 countries on Beats1 via Apple Music.  
           Tune in to Soulection Radio weekly: Saturday | 7-9pm Pacific on Beats 1 via Apple Music</p>
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
      description: "UX Design & Development | Startup Founder",
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
