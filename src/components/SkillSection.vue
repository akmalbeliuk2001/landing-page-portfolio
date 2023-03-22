<template>
  <div class="bg-[#F0EEED] h-screen w-full">
    <div class="relative mx-4 md:mx-7 lg:mx-auto lg:max-w-[1064px] h-full">
      <div class="flex justify-between items-center flex-col lg:flex-row absolute left-[50%] translate-x-[-50%] top-[55%] translate-y-[-50%] w-full">
        <div>
          <p class="poppins font-semibold text-[25px] lg:text-[31.25px] text-[#000] leading-[100%]">Soft <br> Skills</p>
          <div class="flex flex-wrap max-w-[550px] mt-8">
            <p v-for="(data, index) in softSkill" :key="index" class="poppins font-normal text-[12px] lg:text-[16px] text-[#F44F1A] px-4 py-2 border-solid border-[1px] border-[#F44F1A] rounded-[30px] w-max mr-2 mb-4">{{ data }}</p>
          </div>
          <p class="poppins font-semibold text-[25px] lg:text-[31.25px] text-[#000] leading-[100%] mt-8 lg:mt-4">Hard <br> Skills</p>
          <div class="flex flex-wrap max-w-[550px] mt-8">
            <p v-for="(data, index) in hardSkill" :key="index" class="poppins font-normal text-[12px] lg:text-[16px] text-[#F44F1A] px-4 py-2 border-solid border-[1px] border-[#F44F1A] rounded-[30px] w-max mr-2 mb-4">{{ data }}</p>
          </div>
        </div>
        <img class="h-[609px] w-[451px] hidden lg:block" src="@/assets/skill_figure.png" alt="skill figure">
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const softSkill  = ref (['Comunication', 'Team Work', 'Responsibility', 'Leadership', 'Coriosity']);
const hardSkill  = ref (['HTML', 'CSS', 'JavaScript', 'Vue Js', 'Tailwind', 'Bootstrap', 'SCSS', 'Microsoft Office', 'Figma', 'Photoshop']);
</script>

<style>
</style>