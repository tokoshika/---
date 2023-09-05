<template>
  <button @click="nanasanOpen" class="btn" :class="{ red: nanasanActive }">
    七三一部隊
  </button>

  <div v-if="nanasanActive">
    <p>
      日本軍による人体実験の舞台は中国でした。その中で最もよく知られている
      <br />七三一部隊（関東軍防疫給水部）は、石井四郎軍医中将（階級は終戦時）によって作られ、
      中国東北部のハルビン郊外にありました。
      <br />それは致死的な生体実験を秘密裏に行うための特別な一大研究施設でした。
    </p>
    <p>(1) 手術の練習台にする</p>
    <p>(2) 病気に感染させる</p>
    <p>(3) 確立されていない治療法を試す</p>
    <p>(4) 極限状態における人体の変化や限界を知る</p>
    <hr />
    <button class="nanjin" @click="museumOpen">
      侵華日軍第731部隊罪証陳列館
    </button>
  </div>
  <div v-if="museumActive">
    <h1>This is MuseamAvtive</h1>
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
    color: red;
    background-color: grey;
  }

  .nanjin {
    width: 300px;
    margin-bottom: 1rem;
    font-size: 1.3rem;
  }
</style>
