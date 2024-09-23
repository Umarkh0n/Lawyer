<script setup>
import { RouterView } from 'vue-router'
import Navbar from './components/navbar/Navbar.vue';
import FooterDown from './components/Footer/FooterDown.vue';
</script>

<template>
  <header class="lg:fixed  top-0 z-50 bg-white w-full ">
    <Navbar show-img="true " />
  </header>
  <main>
    <RouterView />  
  </main>
  <footer>
      <FooterDown/>
  </footer>

  
</template>

<style scoped>

</style>