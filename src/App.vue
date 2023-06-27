<template>
  <Navbar/><!---navigation bar-->
 <router-view/>  <!-- all the contect shows here -->
 <Footer/> <!--the footer goes after router view because of the content--->
</template>

<script>
import Navbar from '@/components/Navbar.vue'
import Footer from '@/components/Footer.vue'

export default{
  components:{
  Navbar, Footer
  }

}

</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: black;
}

</style>
