<template>
  <div id="app">
    <Header :navBarData="navBarData" :phone="phone" :userInfo="userInfo"/>
    <Main :brands="brands" :phone="phone" :awards="awards"/>
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
      phone : "(555) 802-1234",
      userInfo : [
        {
          name : "Richard Madsen",
          info : "Marketing Consultant Expert",
          img : "marketing-consultant-expert.jpg"
        },
      ],
      brands : [
        {
          img : 'abstract.png'
        },
        {
          img : 'cglobal.png'
        },
        {
          img : 'next.png'
        },
        {
          img : 'hemisferio.png'
        },
        {
          img : 'spaces.png'
        },
        {
          img : 'digitalbox.png'
        },

      ],
      awards : [
        {
          img : 'a.png',
          title : 'Winner Seo Master MAGT',
          info : 'Smart Start Award 2017',
          color : 'light-blue'
        },
        {
          img : 'b.png',
          title : 'Top Social Media Agencies',
          info : 'Next Partner 2018'
        },
        {
          img : 'c.png',
          title : '10 Fastest Growing Abstract',
          info : 'Solution Providers 2019',
          color : 'red'
        },
        {
          img : 'd.png',
          title : 'National Excellence Agencie',
          info : 'Award Winner 2020',
          color : 'blu'
        },
      ]
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
  .ms_container {
    margin: 0 auto;
    max-width: 1300px;
    height: 100%;
  }
  .space-bet {
    display: flex;
    justify-content: space-between;
  }
  .align-center {
    display: flex;
    align-items: center;
  }
  .center {
    display: flex;
    justify-content: center;
  }
  .space-evenly {
    display: flex;
    justify-content: space-evenly;
  }
  .phone {
    display: flex;
    align-items: center;
    i {
      margin-right: 20px;
    }
  }
  .orange {
    color: $colorOrange;
    .btn &:hover {
      color: white;
      transition: 0.5s;
    }
  }
  .btnLightOrange {
    background-color: rgba($colorOrange, 0.2);
    &:hover {
      color: white;
      background-color: $colorOrange;
      transition: 0.5s;
      cursor: pointer;
    }
  }
  .btnOrange {
    color: white;
    background-color: $colorOrange;
    &:hover {
      background-color: #EB621F;
      transition: 0.5s;
    }
  }
  .btnWhite {
    background-color: white;
    color: black;
    &:hover {
      background-color: transparent;
      border: 1px solid white;
      color: white;
      transition: 0.5s;
      cursor: pointer;
    }
  }
  .btn {
    border-radius: 10px;
    padding: 15px 35px;
    font-size: 18px;
    &:hover {
      color: white;
      cursor: pointer;
    }
  }
  .btn-lg {
    width: 100%;
    text-align: center;
    font-size: 18px;
    border-radius: 10px;
    padding: 20px 0;
    cursor: pointer;
  }
  .w50 {
    width: 50%;
  }
  .txt-center {
    text-align: center;
  }
  .ball {
    height: 40px;
    width: 40px;
    border-radius: 50%;
    margin-right: 15px;
  }
  .blue {
    background-color: #223BCB;
  }
  .yellow {
    background-color: #EFD43F;
  }
  .green {
    background-color: #38C3A0;
  }
  .relative {
    position: relative;
  }
  .back {
    height: 450px;
    width: 100%;
    position: absolute;
    background-image: linear-gradient(to bottom, rgba(255,0,0,0), rgba($colorOrange,0.7));
    opacity: 0;
    top: 0;
    left: 0;
    &:hover {
      opacity: 1;
      transition: 0.5s;
    }
  }
</style>
