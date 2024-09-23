<script setup>
import { RouterLink } from 'vue-router'
import { ref, defineProps } from 'vue'

const props = defineProps({
  showImg: { type: Boolean, default: true },
  showLogo: { type: Boolean, default: true },
  isHamburger: { type: Boolean, default: false }
})

const isMenuOpen = ref(false)
const toggleMenu = () => {
  isMenuOpen.value = !isMenuOpen.value
}
</script>

<template>
  <nav class="flex items-center lg:justify-between containerr">
    <!-- Hamburger Icon (visible in mobile view) -->
    <button v-if="isHamburger" @click="toggleMenu" class="lg:hidden p-4 focus:outline-none">
      <i class="ri-menu-line text-xl text-[#cca876]"></i>
    </button>
    <div class="p-2" v-if="showLogo && showImg">
      <img src="https://lawyers-attorneys.vamtam.com/wp-content/uploads/2015/05/logo.png" alt="" height="70" width="270">
    </div>

    <!-- Desktop Menu -->
    <ul :class="['flex flex-wrap lg:flex items-center flex-wrap text-center justify-center lg:justify-between text-sm font-serif', { hidden: isHamburger }]">
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

    <!-- Mobile Hamburger Menu -->
    <div v-if="isHamburger && isMenuOpen" class="fixed top-0 left-0 w-1/2 h-full bg-white shadow-lg z-50 transition-transform duration-300 ease-in-out"
         :class="{ '-translate-x-full': !isMenuOpen, 'translate-x-0': isMenuOpen }">
      <div class="flex items-start justify-between">
        <ul class="flex flex-col items-start justify-start p-4 space-y-4 text-sm font-serif">
          <li @click="toggleMenu" class="hover:text-[#9b7b4d] transition">
            <RouterLink to="/" active-class="active">Home</RouterLink>
          </li>
          <li @click="toggleMenu" class="hover:text-[#9b7b4d] transition">
            <RouterLink to="/about" active-class="active">About</RouterLink>
          </li>
          <li @click="toggleMenu" class="hover:text-[#9b7b4d] transition">
            <RouterLink to="#">Attorneys</RouterLink>
          </li>
          <li @click="toggleMenu" class="hover:text-[#9b7b4d] transition">
            <RouterLink to="#">News</RouterLink>
          </li>
          <li @click="toggleMenu" class="hover:text-[#9b7b4d] transition">
            <RouterLink to="#">Features</RouterLink>
          </li>
          <li @click="toggleMenu" class="hover:text-[#9b7b4d] transition">
            <RouterLink to="#">Practice Areas</RouterLink>
          </li>
          <li @click="toggleMenu" class="hover:text-[#9b7b4d] transition">
            <RouterLink to="#">Q&A</RouterLink>
          </li>
          <li @click="toggleMenu" class="hover:text-[#9b7b4d] transition">
            <RouterLink to="#">Contacts</RouterLink>
          </li>
        </ul>
        <button class="p-4 text-xl backBtn" @click="toggleMenu">
          <i class="ri-arrow-left-line text-[#cca876]"></i>
        </button>
      </div>
    </div>
  </nav>
</template>

<style scoped>
.active {
  color: #9b7b4d;
}
</style>
