<template>
  <button @click="showAns" class="btn">長崎原爆投下</button>
  <div v-if="isActive">
    <p>
      <span style="color: red">死者: 73,884人</span><br />
      重軽傷者 :74,909人<br />
      合計 148,793人
    </p>
  </div>
  <p>（ながさきの平和（長崎市平和推進課）HPより抜粋）</p>
</template>

<script setup>
  import { ref } from "vue";
  const isActive = ref(false);
  const showAns = () => {
    isActive.value = !isActive.value;
  };
</script>

<style scoped>
  .btn {
    width: 400px;
    margin-bottom: 1rem;
    font-size: 1.5rem;
    border: none;
    color: white;
    background-color: rgb(49, 48, 48);
    border-radius: 2px;
  }
</style>
