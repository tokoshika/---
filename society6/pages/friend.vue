<template>
  <div class="main-container">
    <div><h2>ぼくが出会ったアジアのヒトたち</h2></div>

    <div class="btn-container">
      <button class="japan" @click="japan">中国人女子(史学科)</button>
    </div>
    <p v-if="isOpenJapan">
      私のおじいちゃんは日本軍に撃たれて死にました。<br />
      おばあちゃんは、今でもそれを悲しんでいます。<br />
      でも悪いのは昔の戦争をした人たちです。<br />
      所さんは悪くありません<br />
      私が歴史を勉強するのは、日本を恨むためではなく<br />
      二度と悲しい戦争を起こさないために勉強をしています。<br />
      所さんも辛いでしょうが、日本軍のやった事に目を背けないで<br />
      戦争の悲惨さを伝えていって下さい。
    </p>
    <br />
    <div class="btn-container">
      <button class="china" @click="china">中国人男子(家電販売)</button>
      <p v-if="isOpen">
        日本の製品は素晴らしい。<br />
        戦争については、日本の政府がちゃんと謝らないから悪い。<br />
        日本人も日本製品も好きだ。でも日本政府は大嫌いだ。<br />
        ドラゴンボール最高。
      </p>
    </div>
    <br />
    <div class="btn-container">
      <button class="taiwan" @click="taiwan">韓国人女子(18歳家事手伝い)</button>
      <p v-if="isOpenTaiwan">
        いやーまじで日本人が大っ嫌いだったんだよねー。<br />
        ここに来た時は、そばに日本人がいるだけで、気持ち悪くて<br />
        吐きそうになって、まいった。<br />
        でも、少しずつ日本人と話すようになって、思ったんだけど<br />
        意外といい人が多いかもしれない。<br />
        戦争の事を話さなければ、仲良くなれるかもしれない。
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
  </div>
</template>

<script setup>
  import { ref } from "vue";
  const isOpen = ref(false);
  const isOpenJapan = ref(false);
  const isOpenTaiwan = ref(false);
  const isOpenAmerica = ref(false);
  const isOpenRussia = ref(false);
  const isOpenPutin = ref(false);
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
</script>

<style scoped>
  .japan,
  .america,
  .russia,
  .taiwan,
  .china,
  .putin {
    font-size: 1rem;
    width: 300px;
    margin-bottom: 0.5rem;
    margin-right: 1rem;
  }

  .main-container {
    margin: 0 auto;
    margin-left: 10%;
  }

  .btn-container {
    display: inline;
    /* text-align: center; */
  }
</style>
