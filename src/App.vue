<template>
  <v-app class="grey lighten-3">
    
    <Navbar/>
    <v-content class="mx-4 mt-3">
      <router-view/>
    </v-content>
    <Footer/>

  </v-app>
</template>

<script>
import Navbar from "./components/Navbar.vue"
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components:{
    Navbar,
    Footer
  },
  data () {
    return {
      //
    }
  }
}
</script>
<style>
*{
  box-sizing: border-box;
}
</style>

