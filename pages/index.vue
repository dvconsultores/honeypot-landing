<template>
  <div id="home" class="divcol">
    <img id="left" src="~/assets/sources/images/left_elipse.png" alt="Elipse">
    <img id="right" src="~/assets/sources/images/right_elipse.png" alt="Elipse">

    <section>
      <v-btn class="btn-berachain">
        <img src="~/assets/sources/images/berachain.png" alt="Berachain"> Built on Berachain
      </v-btn>  
      <h2>
        A Continuous <br> Innovative De-fi Hub
      </h2>

      <div class="center divrow mobile-div" style="gap: 10px; background-color: transparent;">
        <v-btn  v-for="(item, index) in dataBtns" :key="index" class="btn-data" :href="item.link" target="_blank">
          <img class="btn-img" :src="item.img" alt="Image"> <img class="btn-img-black" :src="item.img_black" alt="Image"> {{ item.text }}
        </v-btn>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  name: "HomePage",
  layout: "empty-layout",
  data() {
    return {
      dataBtns: [
        {
          text: "Twitter",
          img:  require("~/assets/sources/icons/twitter.svg"),
          img_black: require("~/assets/sources/icons/twitter-black.svg"),
          link:"https://twitter.com/honeypotfinance",
        },
        {
          text: "Frontend Work",
          img:  require("~/assets/sources/icons/frontend.svg"),
          img_black: require("~/assets/sources/icons/frontend-black.svg"),
          link:"https://honeypot-front-end-ten.vercel.app/swap",
        },
        {
          text: "Discord",
          img:  require("~/assets/sources/icons/discord.svg"),
          img_black: require("~/assets/sources/icons/discord-black.svg"),
          link:"https://discord.com/invite/pkh7shAPWB",
        },
        {
          text: "Prototype",
          img:  require("~/assets/sources/icons/arrow.svg"),
          img_black: require("~/assets/sources/icons/arrow-black.svg"),
          link:"https://yexlab.vercel.app/main",
        },
      ]
    }
  },
  head() {
    const title = 'Home';
    return {
      title,
    }
  },
  methods: {
  }
};
</script>

<style src="~/assets/styles/pages/index.scss" lang="scss" />
