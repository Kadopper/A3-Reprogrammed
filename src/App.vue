<template>
  
  <div>
    <div class="buttonHome" @click="openMenu('home')"></div>
    <div class="buttonSearch" @click="openMenu('search')"></div>
    <div class="buttonTicket" @click="openMenu('ticket')"></div>
    <div class="buttonProfile" @click="openMenu('profile')"></div>

    <img v-if="activeMenu === 'home'" src="/src/assets/homeMenu.svg">
    <img v-if="activeMenu === 'search'" src="/src/assets/searchMenu.svg">
    <img v-if="activeMenu === 'ticket'" src="/src/assets/ticketMenu.svg">
    <img v-if="activeMenu === 'profile'" src="/src/assets/profileMenu.svg">
  </div>
  
</template>

<script setup>
  import { ref } from 'vue';
  
// hold current menu
  const activeMenu = ref('');

// change menu by using the click input menu function 
  function openMenu(menu) {
    activeMenu.value = menu;
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
