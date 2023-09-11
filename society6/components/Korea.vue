<template>
  <button @click="nanasanOpen" class="btn" :class="{ red: nanasanActive }">
    韓国併合
  </button>
  <br />
  <button @click="nanasanOpen" class="btn" :class="{ red: nanasanActive }">
    徴用工・従軍慰安婦問題
  </button>

  <!-- <div v-if="nanasanActive"></div> -->
  <div v-if="museumActive">
    <h1>This is MuseamAvtive</h1>
    <img src="~/assets/731.jpg" />
  </div>
</template>

<script setup>
  import { ref } from "vue";
  const nanasanActive = ref(false);
  const museumActive = ref(false);

  const nanasanOpen = () => {
    nanasanActive.value = !nanasanActive.value;
  };

  const museumOpen = () => {
    museumActive.value = !museumActive.value;
  };
</script>

<style scoped>
  .btn {
    width: 400px;
    margin-bottom: 1rem;
    font-size: 1.5rem;
    border: none;
    color: rgb(49, 48, 48);
    background-color: rgb(49, 48, 48);
    border-radius: 2px;
  }

  .red {
    color: white;
    background-color: grey;
  }

  .nanjin {
    width: 400px;
    margin-bottom: 1rem;
    font-size: 1.3rem;
  }
</style>
