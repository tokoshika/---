<template>
  <button @click="showAns" class="btn">広島原爆投下</button>

  <div v-if="isActive">
    <p>
      原爆投下後に様々な機関が調査を行っていますが、
      原爆によって死亡した人の数については、現在でも、
      正確には分かっていません。<br />本市では、放射線による
      急性障害が一応おさまった昭和20年（1945年） 12月末までに、<span
        style="color: red"
        >約14万人</span
      >が亡くなられたと推計しています。
    </p>
  </div>
  <p>(広島市ホームページより抜粋)</p>
</template>

<script setup>
  import { ref } from "vue";
  const isActive = ref(false);

  const showAns = () => {
    console.log("click");
    isActive.value = !isActive.value;
    return isActive;
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
