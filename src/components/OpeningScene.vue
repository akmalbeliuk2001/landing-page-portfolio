<template>
  <div class="opening absolute h-screen w-screen bg-[#F44F1A] text-center poppins font-extrabold" :class="{ close: CloseOpening }">
    <div class="pt-[230px] lg:pt-[150px]">
      <p class="text-[25px] lg:text-[39.06px] text-[#fff]">Provcerb says:</p>
      <p class="text-[39.06px] lg:text-[76.29px] text-[#000] leading-tight mt-2 lg:mt-4">"Do not know,<br />then do not love!"</p>
      <img class="wiggle w-[40px] lg:w-[50px] h-[40px] lg:h-[50px] ml-auto mr-auto mt-2 lg:mt-4 cursor-pointer" src="@/assets/portofolio_arrow.png" alt="Opening arrow starting" @click="close"/>  
    </div>
    <img class="fixed bottom-0 left-[30%] lg:left-[40%] translate-x-[-50%] w-[200px] 2xl:w-[330px]" src="@/assets/peace_hand.png" alt="Opening peace hand">
    <img class="fixed bottom-0 left-[70%] lg:left-[60%] translate-x-[-50%] w-[260px] 2xl:w-[418px]" src="@/assets/hey_hand.png" alt="Opening hey hand">
  </div>
</template>

<script setup>
import { ref } from 'vue';

let CloseOpening = ref(false);

function close () {
  CloseOpening.value = true;
}
</script>

<style scoped>
.opening {
  transition: all 1.5s ease-out;
}
.close {
  transform: translateX(-100vw);
}
</style>
