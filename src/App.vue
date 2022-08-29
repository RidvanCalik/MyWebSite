<script setup>
import { RouterView } from 'vue-router'
import Header from './components/Header.vue';

</script>

<template>

  <Header></Header>

  <RouterView />

</template>

<style>
@import '@/assets/base.css';

#app {
  position: absolute;
  top: 0;
  margin: 0;
  height: 100%;
  width: 100%;
  display: grid;

  grid-template-columns: 100%;
  grid-template-rows: 10% 90%;
}

@media (max-width: 846px) {
  #app {
    grid-template-rows: 10% 100%;
  }

}
</style>
