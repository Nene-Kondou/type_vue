<script setup lang="ts">
import WidthModel from './components/WidthModel.vue'
</script>

<template>
  <div>
    <h1>コンポーネントの独立性</h1>
    <WidthModel></WidthModel>
    <WidthModel></WidthModel>
  </div>
</template>

<style scoped>
section {
  border: blue 1px solid;
  margin: 10px;
}
</style>
