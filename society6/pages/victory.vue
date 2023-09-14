<template>
  <div class="main-container">
    <div><h2>終戦記念日を比べてみよう</h2></div>

    <div class="btn-container">
      <button class="japan" @click="japan">日本</button>
      <p v-if="isOpenJapan">
        8月15日 <span style="color: gray">終戦の日</span>
      </p>
    </div>
    <br />
    <div class="btn-container">
      <button class="china" @click="china">中国</button>
      <p v-if="isOpen">
        9月3日 <span style="color: gray">抗日戦争勝利記念日</span>
      </p>
    </div>
    <br />
    <div class="btn-container">
      <button class="taiwan" @click="taiwan">台湾</button>
      <p v-if="isOpenTaiwan">
        10月25日 <span style="color: gray">日本からの解放記念日</span>
      </p>
    </div>
    <br />
    <div class="btn-container">
      <button class="america" @click="america">アメリカ</button>
      <p v-if="isOpenAmerica">
        9月2日 <span style="color: gray">Victory over Japan Day</span>
      </p>
    </div>
    <br />
    <div class="btn-container">
      <button class="russia" @click="russia">ロシア</button>
      <p v-if="isOpenRussia">
        9月3日 <span style="color: gray">第二次世界大戦終結の日</span>
      </p>
    </div>
    <br />
    <h2>日本がウクライナを支援すると・・・</h2>
    <div class="btn-container">
      <button class="putin" @click="putin">プーチン</button>
      <p v-if="isOpenPutin">
        9月3日 <span style="color: gray">軍国主義日本に対する勝利の日</span>
      </p>
    </div>
    <br />

    <div class="btn-container">
      <button class="question" style="margin-top: 1rem" @click="question">
        ここで問題！
      </button>
      <p v-if="questionOpen" @click="questionAgain">
        韓国の終戦記念日はいつでしょう？
      </p>
    </div>
    <br />
    <h2 v-if="againOpen">8月15日・・・開放記念日（光復節）</h2>
    <br />
  </div>
  <br>
</template>

<script setup>
  import { ref } from "vue";
  const isOpen = ref(false);
  const isOpenJapan = ref(false);
  const isOpenTaiwan = ref(false);
  const isOpenAmerica = ref(false);
  const isOpenRussia = ref(false);
  const isOpenPutin = ref(false);
  const questionOpen = ref(false);
  const againOpen = ref(false);
  const china = () => {
    isOpen.value = !isOpen.value;
  };
  const taiwan = () => {
    isOpenTaiwan.value = !isOpenTaiwan.value;
  };
  const japan = () => {
    isOpenJapan.value = !isOpenJapan.value;
  };
  const america = () => {
    isOpenAmerica.value = !isOpenAmerica.value;
  };
  const russia = () => {
    isOpenRussia.value = !isOpenRussia.value;
  };
  const putin = () => {
    isOpenPutin.value = !isOpenPutin.value;
  };
  const question = () => {
    questionOpen.value = !questionOpen.value;
  };
  const questionAgain = () => {
    againOpen.value = !againOpen.value;
  };
</script>

<style scoped>
  .japan,
  .america,
  .russia,
  .taiwan,
  .china,
  .putin,
  .question {
    font-size: 2rem;
    width: 300px;
    margin-bottom: 0.5rem;
    margin-right: 1rem;
  }

  .main-container {
    margin: 0 auto;
    margin-left: 10%;
  }

  .btn-container > p {
    font-size: 1.5rem;
    color: red;
    display: table-cell;
    vertical-align: center;
  }

  .btn-container {
    display: inline;
    text-align: center;
  }
</style>
