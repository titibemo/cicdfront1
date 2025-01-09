<template>
  <div class="about">
    <h1 class="title">Hey la qui va la !</h1>
  </div>
  <p class="inspector">inspecteur gadget</p>
  <div class="damier">
    <template v-for="c in cases" :key="c">
      <div class="case"></div>
    </template>
  </div>
  <p>{{count}}</p>
</template>

<script setup>
import { ref } from 'vue';

const count = ref(0);
const cases = ref([]);

// eslint-disable-next-line
for (let index = 0; index < 100; index++) {
  cases.value.push(index);
  console.log(cases.value);
}
</script>

<style scoped>
* {
  margin: 0;
  padding: 0;
}
.title{
  text-align: center;
  background-color: rgba(10, 10, 10, 0.1);
  animation: customAni 5s ease 0s infinite normal none;
}
.inspector{
  color: green;
  font-size: 1.2em;
}
.damier{
  display: flex;
  flex-wrap: wrap;
  gap: 1px;
  justify-content: center;
  width: 530px;
  height: 530px;
  border: 1px solid black;
  background-color: beige;
}
.case{
  width: 50px;
  height: 50px;
  background-color: #ffffff;
  border: 1px solid black;
}
.case:nth-child(odd){
  background-color: rgba(0, 0, 0, 0.616);
}

@keyframes customAni {
  0%,
  50%,
  100% {
opacity: 1;
  }

  25%,
  75% {
opacity: 0;
  }
}
</style>
