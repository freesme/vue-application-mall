<template>
  <div id="home">
    <nav-bar class="home-nav"><div slot="center">蘑菇街</div></nav-bar>
  </div>
</template>

<script>
import NavBar from 'components/common/navbar/NavBar'
export default {
		name: "Home",
    components: {
      NavBar
    }
	}
</script>

<style scoped>
  .home-nav{
    background-color: #fd5777;
    color: #f6f6f6;
  }

</style>
