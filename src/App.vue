<template>
  <div class="buttonHome" >

    <button @click="openMenu1">Open menu 1</button>
  </div>

  <div>
    <img v-if="!menu1IsOpen" src="/src/assets/hovedMenu.svg">
    <img v-if="menu1IsOpen" src="/src/assets/billetMenu.svg">
  </div>
  
</template>

<script setup>
  import { ref } from 'vue';
  
  const menu1IsOpen = ref(false)

  function openMenu1() {
    menu1IsOpen.value = !menu1IsOpen.value
  }

</script>


<style scoped>
.menu1{
  width: 100px;
  height: 100px;
  background-color: red;
  position: relative;
}

.buttonHome{
  border-radius: 5px;
  border-color: red;
  width: 100px;
  height: 100;
  position: absolute;
}



</style>
