<script setup>
import { RouterView } from 'vue-router'
import TheHeder from './views/TheHeder.vue';
import Menucord from './views/Menucord.vue';

</script>

<template>
<Menucord/>
<TheHeder/>
<RouterView/>
</template>

<style> 
*{
  font-family:'Courier New', Courier, monospace ;
  margin: 0;
  overflow: hidden;
}
body{
  background-image:url(./assets/otrazhenie-gor-v-lesnom-ozere.jpg);
  background-size: cover;
}

</style>
