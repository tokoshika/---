<template>
  <button @click="showAns" class="btn" :class="{ red: onActive }">
    南京大虐殺(事件)
  </button>

  <div v-if="isActive">
    <p>
      日本政府としては、日本軍の南京入城（1937年）後、<br />
      非戦闘員の殺害や略奪行為等があったことは<span style="color: red"
        >否定できないと</span
      >考えています。<br />
      しかしながら、被害者の具体的な人数については諸説あり、<br />
      政府としてどれが正しい数かを認定することは困難であると考えています。
    </p>
    <p><span style="color: green">(日本国外務省ホームページより抜粋)</span></p>
  </div>

  <div v-if="isActive">
    <p>
      中国政府の主張では、<span style="color: red">約30万人</span><br />
      日本国内では、それを否定する声もあり。
    </p>
    <hr />
    <button class="nanjinjiken" @click="jikenOpen">南京城って？</button>
    <div v-if="jikenActive">
      <Nanjinjiken />
    </div>
    <br />
    <button class="nanjin" @click="nanjinOpen">南京大虐殺記念館</button>
  </div>

  <div v-if="nanjinActive">
    <Nanjin />
  </div>
</template>

<script setup>
  import { ref } from "vue";
  const isActive = ref(false);
  const onActive = ref(false);
  const nanjinActive = ref(false);
  const jikenActive = ref(false);

  const showAns = () => {
    isActive.value = !isActive.value;
    onActive.value = !onActive.value;
  };

  const nanjinOpen = () => {
    nanjinActive.value = !nanjinActive.value;
  };

  const jikenOpen = () => {
    jikenActive.value = !jikenActive.value;
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
    color:white;
    background-color: dimgrey;
  }

  .nanjin,
  .nanjinjiken {
    width: 300px;
    margin-bottom: 1rem;
    font-size: 1.3rem;
  }
</style>
