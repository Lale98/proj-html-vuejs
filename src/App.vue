<template>
  <div id="app">
    <Header :navBarData="navBarData"/>
    <Main />
    <Footer />
  </div>
</template>

<script>
import Header from './components/Header.vue';
import Main from './components/Main.vue';
import Footer from './components/Footer.vue';


export default {
  name: 'App',
  components: {
    Header,
    Main,
    Footer,
  },
  data : function () {
    return {
      navBarData : [
        {
          name : "Home",
          list : true,
        },
        {
          name : "Services",
          list : true,
        },
        {
          name : "Why Us",
          list : false,
        },
        {
          name : "Case Studies",
          list : false,
        },
        {
          name : "About",
          list : false,
        },
        {
          name : "Blog",
          list : false,
        },
      ],

    }
  }
}
</script>

<style lang="scss">
  @import './assets/variables';
  @import './assets/generals';
  @import '~@fontsource/roboto/400.css';
  @import '~@fontsource/roboto/500.css';
  @import '~@fontsource/roboto/700.css';

  * {
    font-family: "Roboto";
  }
  .orange {
    color: $colorOrange;
  }
  .backLightOrange {
    background-color: rgba($colorOrange, 0.2);
  }
  .btn {
    border-radius: 10px;
    padding: 15px 35px;
    font-size: 18px;
  }
</style>
