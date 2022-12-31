<template>
  <div
    class="flex flex-col min-h-screen "
  >
    <SiteNavigation />
    <RouterView class="flex-1" v-slot="{ Component }">
      <Transition name="page">
        <component :is="Component" />
      </Transition>
    </RouterView>
  </div>
</template>

<script setup>
import { RouterView } from "vue-router";
import SiteNavigation from "./components/SiteNavigation.vue";
</script>

<style>
body{
  background-image: url("./assets/Z4CD0Ic-weather-wallpapers.jpg");
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center;
  font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
 
}
.page-enter-active {
  transition: 600ms ease all;
}

.page-enter-from {
  opacity: 0;
}
</style>
