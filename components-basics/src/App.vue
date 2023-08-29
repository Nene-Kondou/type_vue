<script setup lang="ts">
// import OneSection from "./components/OneSection.vue";
import OneSection from "./components/OneSection.vue";
</script>

<template>
  <div>
    <h1>コンポーネント基礎</h1>
    <section>
      <h2>コンポーネント1個</h2>
      <OneSection />
    </section>
    <section>
      <h2>コンポーネントが複数</h2>
      <OneSection></OneSection>
      <OneSection></OneSection>
      <OneSection></OneSection>
    </section>
  </div>
</template>

<style scoped>
section {
  border: blue 1px solid;
  margin: 10px;
}
</style>
