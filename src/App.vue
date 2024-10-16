<template>
  

  <div>
    <div
      class="buttonHome" @click="openMenu1">
    </div>
    <div
      class="buttonSearch" @click="openMenu1">
    </div>
    <div
      class="buttonTicket" @click="openMenu1">
    </div>
    <div
      class="buttonProfile" @click="openMenu1">
    </div>
      <img v-if="!menu1IsOpen" src="/src/assets/hovedMenu.svg">
      <img v-if="menu1IsOpen" src="/src/assets/billetMenu.svg">
  </div>
  
</template>

<script setup>
  import { ref } from 'vue';
  
  // fix
  //let menu =  ["home","seach","ticket","profile"]
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
  border-color: red;
  border-style: dashed;
  top: 782px;
  left: 36px;
  width: 45px;
  height: 45px;
  position: absolute;
}

.buttonSearch{
  border-color: red;
  border-style: dashed;
  top: 782px;
  left: 131px;
  width: 45px;
  height: 45px;
  position: absolute;
}


.buttonTicket{
  border-color: red;
  border-style: dashed;
  top: 782px;
  left: 227px;
  width: 45px;
  height: 45px;
  position: absolute;
}

.buttonProfile{
  border-color: red;
  border-style: dashed;
  top: 782px;
  left: 322px;
  width: 45px;
  height: 45px;
  position: absolute;
}



</style>
