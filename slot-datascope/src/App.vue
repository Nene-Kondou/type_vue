<script setup lang="ts">
import {ref} from "vue";
import OneSection from "./components/OneSection.vue";

const taro = ref("田中太郎")
const jiro = ref("鈴木次郎")

</script>

<template>
  <section>
    <h2>Slotの利用</h2>
    <OneSection v-bind:name="taro">
      <p>{{ taro }}さんは連絡がつきません。</p>
    </OneSection>
    <OneSection v-bind:name="jiro"></OneSection>
  </section>
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
