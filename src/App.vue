<template>
  <navbar-section></navbar-section>
  <opening-section></opening-section>
  <header-section></header-section>
  <introducing-section></introducing-section>
</template>

<script setup>
import NavbarSection from "./components/NavbarSection.vue";
import OpeningSection from "./components/OpeningSection.vue";
import HeaderSection from "./components/HeaderSection.vue";
import IntroducingSection from "@/components/IntroducingSection.vue"

</script>


<style lang="scss" scoped>
  body {
    background-color: #F0EEED;
  }
</style>
