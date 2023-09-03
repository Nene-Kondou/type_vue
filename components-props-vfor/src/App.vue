<script setup lang="ts">
import {ref} from "vue";
import OneInfo from "./components/OneInfo.vue";

const weatherListInit = new Map<number, Weather>();
weatherListInit.set(1, {id: 1, title: "今日の天気", content: "今日は一日中、晴れでしょう。"});
weatherListInit.set(2, {id: 2, title: "明日の天気", content: "明日は一日中、雨でしょう。"});
weatherListInit.set(3, {id: 3, title: "明後日の天気", content: "明後日は一日中、雪でしょう。"});
const weatherList = ref(weatherListInit)

interface Weather {
  id: number,
  title: string,
  content: string,
}
</script>

<template>
  <div>
    <h1>Props基礎</h1>
    <section>
      <h2>ループでコンポーネントを生成</h2>
      <OneInfo
        v-for="[id, weather] in weatherList"
        :key="id"
        :title="weather.title"
        :content="weather.content"
      ></OneInfo>
    </section>
  </div>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
