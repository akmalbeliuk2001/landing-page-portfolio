<template>
  <div
    :style="{ 'border-color': borderColor }"
    :class="changeBackgroundColor ? 'bg-[#F44F1A]' : 'bg-[#FFF]'"
    class="navbar fixed z-[99] h-[60px] w-full border-b-[1px] border-solid transition-all duration-500"
  >
    <div class="mx-auto px-4 md:px-7 lg:px-0 lg:max-w-[1064px] overflow-hidden">
      <div
        class="flex nunito font-normal text-xs lg:text-base justify-between items-center pt-[16px] lg:pt-[13px]"
      >
        <p
          :style="{ 'border-color': borderColor, color: borderColor }"
          class="border-[1px] rounded-[30px] px-[8px] py-[4px]"
        >
          Portfolio
        </p>
        <p
          :style="{ 'border-color': borderColor, color: borderColor }"
          class="border-[1px] rounded-[30px] px-[8px] py-[4px]"
        >
          2023
        </p>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from "vue";

const changeBackgroundColor = ref(false);
const borderColor = ref("#F44F1A");

const handleScroll = () => {
  if (window.scrollY > 300) {
    changeBackgroundColor.value = true;
    borderColor.value = "#FFF";
  } else {
    changeBackgroundColor.value = false;
    borderColor.value = "#F44F1A";
  }
};

onMounted(() => {
  window.addEventListener("scroll", handleScroll);
});

onUnmounted(() => {
  window.removeEventListener("scroll", handleScroll);
});
</script>

<style></style>
