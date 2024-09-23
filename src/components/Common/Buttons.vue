

<script setup>
import { defineProps } from 'vue';

const props = defineProps({
  text: String,
  variant: String,
  showIcon: { type: Boolean, default: false },
  iconClass: String // i tagiga dinamik class berish uchun
});

const buttonsStyles = () => {
  switch (props.variant) {
    case 'primary':
      return 'hover:bg-[#4a4f55;] transition-all text-white bg-[#cca876] text-sm px-8 py-3.5 ';
    case 'simpler':
      return 'py-[20px] px-[25px] text-white text-base bg-black !transition uppercase hover:bg-[#cca876] ';
    case 'unusual':
      return 'border border-[#cca876] text-[#cca876] text-sm pt-1 pb-0.5 px-6 hover:text-white hover:bg-[#cca876] transition-all';
    case 'modest':
      return 'border border-white text-white py-2 px-10 hover:border-[#CCA876] hover:bg-[#CCA876] group transition-all';
    default:
      return '';
  }
};
</script>

<template>
  <button :class="buttonsStyles()" class="flex items-center gap-2">
    <!-- i tagiga dinamik class uzatish -->
    <i v-if="showIcon" :class="iconClass"></i>  
    {{ text }}
  </button>
</template>





