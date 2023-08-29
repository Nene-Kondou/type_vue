<script setup lang="ts">
import {ref} from "vue";

const name = ref("名無し");
</script>

<template>
  <section>
    <p>{{ name }}さんですね！</p>
    <input type="text" name="" id="" v-model="name">
  </section>
</template>

<style scoped>
section {
  border: orange 1px dashed;
  margin: 10px;
}
</style>
