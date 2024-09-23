<script setup>
import { defineProps } from 'vue';
defineProps({
    text: String,

})



</script>

<template>
    <div class="containerr">
        <h2 class="mt-[120px] mb-3 text-3xl text-center uppercase text-[#4a4f55]">
            {{ text }}
        </h2>
        <div class="block w-full border !mb-[40px]">

        </div>
       


    </div>
</template>

<style scoped>
.profile {
  margin-bottom: 2rem;
}
</style>