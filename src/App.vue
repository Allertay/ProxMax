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
   margin: 0;
  font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
   overflow: hidden;
}
body{
background-color: #FFFAFA;
}

</style>
