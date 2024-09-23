<script setup>
import { RouterLink } from 'vue-router'
defineProps({
  showImg: { type: Boolean, default: true }
})
</script>

<template>
  <nav class="flex items-center justify-between containerr ">
    <div class="p-2">
      <RouterLink to="/git init ">
        <img v-if="showImg" src="https://lawyers-attorneys.vamtam.com/wp-content/uploads/2015/05/logo.png" alt=""
        height="70" width="270">
      </RouterLink>
    </div>
    <ul class="lg:flex items-center justify-between text-sm font-serif hidden ">
      <li class="ml-6 hover:text-[#9b7b4d] transition">
        <RouterLink to="/" active-class="active">Home</RouterLink>
      </li>
      <li class="ml-6 hover:text-[#9b7b4d] transition">
        <RouterLink to="/about" active-class="active">About</RouterLink>
      </li>
      <li class="ml-6 hover:text-[#9b7b4d] transition">
        <RouterLink to="#">Attorneys</RouterLink>
      </li>
      <li class="ml-6 hover:text-[#9b7b4d] transition">
        <RouterLink to="#">News</RouterLink>
      </li>
      <li class="ml-6 hover:text-[#9b7b4d] transition">
        <RouterLink to="#">Features</RouterLink>
      </li>
      <li class="ml-6 hover:text-[#9b7b4d] transition">
        <RouterLink to="#">Practice Areas</RouterLink>
      </li>
      <li class="ml-6 hover:text-[#9b7b4d] transition">
        <RouterLink to="#">Q&A</RouterLink>
      </li>
      <li class="ml-6 hover:text-[#9b7b4d] transition">
        <RouterLink to="#">Contacts</RouterLink>
      </li>
    </ul>
  </nav>

</template>

<style scoped>
.active {
  color: #9b7b4d;
}
</style> 





