<template>
<v-app> 
  <Navbar/>
  <Rightnav />

  <v-content class="ma-4">
    <router-view></router-view>
  </v-content>
  <Footer/>

</v-app>

</template>

<script>
import Navbar from '@/components/Navbar'
import Footer from '@/components/Footer'
import Rightnav from "@/components/Rightnav";

export default {
    name: 'App',
    components:{
      Navbar,
      Footer,
      Rightnav
    }

  
};
</script>
