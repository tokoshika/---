<template>
  <div class="main-container">
    <div><h2>ぼくが出会ったアジアのヒトたち</h2></div>

    <div class="btn-container">
      <button class="china-f" @click="chinaF">中国人女子(史学科学生)</button>
    </div>
    <p v-if="chinaFemale">
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
      <button class="china-m" @click="chinaM">中国人男子(家電販売)</button>
      <p v-if="chinaMale">
        日本の製品は素晴らしい。<br />
        戦争については、日本の政府がちゃんと謝らないから悪い。<br />
        日本人も日本製品も好きだ。でも日本政府は大嫌いだ。<br />
        ドラゴンボール最高。
      </p>
    </div>
    <br />
    <div class="btn-container">
      <button class="korea-f" @click="koreaF">
        韓国人女子(18歳家事手伝い)
      </button>
      <p v-if="koreaFemale">
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
      <button class="korea-m" @click="koreaM">韓国人男子(23歳学生)</button>
      <p v-if="koreaMale">
        戦争の話しは難しい。日本政府の態度は我慢できない<br />
        韓国人としては容認できない。日本政府のいう事はクソ！<br />
        でも日本人はいいやつが多いし、日本のアニメも大好きだ。<br />
        政治家じゃなければ仲良くなれる。
      </p>
    </div>
    <br />
    <div class="btn-container">
      <button class="north-korea" @click="northK">
        北朝鮮夫婦(夫婦で留学)
      </button>
      <p v-if="northKorea">
        我々朝鮮民族は、日本の帝国主義によって無理やり日本の兵士として<br />
        ・・・(約1時間)・・・<br />
        つまり日本政府は国民とともに我々の国家に<br />
        ・・・(約1時間)・・・<br />
        ということなのですが、これは私たちの友好の印として、<br />
        妻の手作りキムチをあなたにあげます。食べて下さい。<br />
        <span style="color: red">えっ・・・</span>
      </p>
    </div>
    <br />
    <div class="btn-container">
      <button class="taiwan" @click="taiwan">
        台湾人男子(中卒、兵役前15歳)
      </button>
      <p v-if="taiwanOpen">
        日本大好き。おじさん、やくざ、スリッパ、めしめし。<br />
        昔のこと？そんなの知らねー。おれ生まれてないし。<br />
        今が平和ならいいんじゃない？<br />
        ていうか今やばいのは大陸の奴らだし。<br />
        日本人、ロシア人は好き。韓国人は台湾くるな。
      </p>
    </div>
    <br />
    <div class="btn-container">
      <button class="america" @click="america">
        アメリカ人男子(おそらく小学生)
      </button>
      <p v-if="americaOpen">アメリカイズナンバーワン！</p>
    </div>
    <br />
    <div class="btn-container">
      <button class="russia" @click="russia">ロシア人（男子19歳）</button>
      <p v-if="russiaOpen">
        うーん、とりあえずタバコ1本くれない？ビールもあると嬉しいな。<br />
        戦争について？OK、ダヴァイ、ダヴァイ!<br />
        それじゃぁ、酒もっと買ってこようか。
      </p>
    </div>
    <br />
  </div>
  
</template>

<script setup>
  import { ref } from "vue";
  const chinaFemale = ref(false);
  const chinaMale = ref(false);
  const koreaFemale = ref(false);
  const koreaMale = ref(false);
  const northKorea = ref(false);
  const taiwanOpen = ref(false);
  const americaOpen = ref(false);
  const russiaOpen = ref(false);
  const chinaF = () => {
    chinaFemale.value = !chinaFemale.value;
  };
  const chinaM = () => {
    chinaMale.value = !chinaMale.value;
  };
  const koreaF = () => {
    koreaFemale.value = !koreaFemale.value;
  };
  const koreaM = () => {
    koreaMale.value = !koreaMale.value;
  };
  const northK = () => {
    northKorea.value = !northKorea.value;
  };
  const taiwan = () => {
    taiwanOpen.value = !taiwanOpen.value;
  };
  const america = () => {
    americaOpen.value = !americaOpen.value;
  };
  const russia = () => {
    russiaOpen.value = !russiaOpen.value;
  };
</script>

<style scoped>
  .china-f,
  .china-m,
  .korea-f,
  .korea-m,
  .taiwan,
  .america,
  .russia,
  .north-korea {
    font-size: 1rem;
    width: 300px;
    margin-bottom: 0.5rem;
    margin-right: 1rem;
  }

  .main-container {
    margin: 0 auto;
    margin-left: 10%;
    background-color: bisque;
    width:800px;
    padding: 1rem;
  }

  .btn-container {
    display: inline;
    /* text-align: center; */
  }
  p {
    margin-top: 0;
  }
</style>
