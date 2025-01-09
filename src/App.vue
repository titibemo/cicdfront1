<template>
  <Navbar
    colorNavBar='orange'
  ></Navbar>
  <router-view/>
</template>

<script setup>
/* eslint-disable */
import Navbar from './components/NavbarComp.vue';
</script>

<style scoped>
body{
  background-color: #111111;
  color: white;
}

</style>
