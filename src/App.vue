<template>
  
  <div>
    <div class="buttonHome" @click="changeMenu('home')"></div>
    <div class="buttonSearch" @click="changeMenu('search')"></div>
    <div class="buttonTicket" @click="changeMenu('ticket')"></div>
    <div class="buttonProfile" @click="changeMenu('profile')"></div>

    <img v-if="activeMenu == 'home'" src="/src/assets/homeMenu.svg">
    <img v-if="activeMenu == 'search'" src="/src/assets/searchMenu.svg">
    <img v-if="activeMenu == 'ticket'" src="/src/assets/ticketMenu.svg">
    <img v-if="activeMenu == 'profile'" src="/src/assets/profileMenu.svg">
  </div>
  
</template>

<script setup>
  import { ref } from 'vue'

// hold current menu
  const activeMenu = ref('home')
// change menu with buttons
  function changeMenu(menu) {
    activeMenu.value = menu
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
  /* border-color: red;
  border-style: dashed; */ 
  top: 780px;
  left: 36px;
  width: 45px;
  height: 45px;
  position: absolute;
  cursor: pointer;
}

.buttonSearch{
  /* border-color: red;
  border-style: dashed; */
  top: 780px;
  left: 131px;
  width: 45px;
  height: 45px;
  position: absolute;
  cursor: pointer;
}


.buttonTicket{
  /* border-color: red;
  border-style: dashed; */ 
  top: 780px;
  left: 225px;
  width: 45px;
  height: 45px;
  position: absolute;
  cursor: pointer;
}

.buttonProfile{
  /* border-color: red;
  border-style: dashed; */
  top: 780px;
  left: 319px;
  width: 45px;
  height: 45px;
  position: absolute;
  cursor: pointer;
}



</style>
