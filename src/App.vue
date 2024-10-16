<template>
  <div>
    <button @click="openMenu1">Open menu 1</button>
    <div v-if="menu1" class="menu1">
      
    </div>
  </div>
</template>

<script setup>
  import { ref } from 'vue';
  
  const menu1IsOpen = ref(false)

  function openMenu1() {
    menu1IsOpen = !menu1IsOpen
  }

</script>


<style scoped>
.menu1{
  width: 100px;
  height: 100px;
  background-color: red;
  position: relative;
}

</style>
