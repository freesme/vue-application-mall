<template>
  <div id="home">
    <nav-bar class="home-nav">
      <div slot="center">蘑菇街</div>
    </nav-bar>
    <home-swiper :banners="banners"
                 ref="hSwiper"></home-swiper>
  </div>
</template>

<script>
  import {getHomeMultidata} from "network/home";
  import HomeSwiper from './childComps/HomeSwiper'
  import NavBar from 'components/common/navbar/NavBar'

  export default {
    name: "Home",
    components: {
      NavBar,
      HomeSwiper
    },
    data(){
      return{
        // result:null
        banners:[],
        recommeds:[]
      }
    },
    created() {
      getHomeMultidata().then(res=>{
        console.log(res);
        // this.result = res
        this.banner = res.data.banner.list
        this.recommeds = res.data.recommend.list
      })
    }
  }
</script>

<style scoped>
  .home-nav {
    background-color: #fd5777;
    color: #f6f6f6;
  }

</style>
