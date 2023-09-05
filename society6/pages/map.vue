<template>
  <div class="asia">
    <button @click="changMap">アジア</button>
  </div>
  <div class="main-container">
    <img v-if="isOpen" class="img" src="~/assets/asia01.png" />
    <img v-if="mapOpen" class="img2" src="~/assets/asia02.png" />
  </div>
</template>

<script setup>
  import { ref } from "vue";
  const isOpen = ref(true);
  const mapOpen = ref(false);
  const map = () => {
    isOpen.value = !isOpen.value;
    mapOpen.value = !mapOpen.value;
  };

  const changMap = () => {
    setTimeout(() => {
      map();
    }, 500);
  };
</script>

<style scoped>
  .main-container {
    background-color: rgb(46, 52, 52);
  }
  .asia {
    text-align: center;
  }
  .main-container {
    display: flex;
    justify-content: center;
  }
  .img {
    width: 75%;
  }
  .img2 {
    width: 85%;
  }
</style>
