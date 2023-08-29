<script setup lang="ts">
import WidthModel from './components/WidthModel.vue'
</script>

<template>
  <section>
    <h1>コンポーネントの独立性</h1>
    <WidthModel></WidthModel>
    <WidthModel></WidthModel>
  </section>
</template>

<style>
section {
  border: blue 1px solid;
  margin: 10px;
}
</style>
