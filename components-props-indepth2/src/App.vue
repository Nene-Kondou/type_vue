<script setup lang="ts">
import {ref,computed} from "vue";
import OneMemver from "./components/OneMemver.vue";

// 会員リストデータを用意
const memberListInit = new Map<number, Member>();
  memberListInit.set(33456, {id: 33456, name: "田中太郎", email: "bow@ezample.com", points: 35, note: "初回入会特典あり。"});
  memberListInit.set(44783, {id: 44783, name: "鈴木次郎", email: "mue@ezample.com", points: 53, });
  const memberList = ref(memberListInit);

  // 会員リスト内の全会員のポイント合計の算出プロパティ
  const totalPoints = computed(
    (): number => {
      let total = 0;
      for(const member of memberList.value.values()) {
        total += member.points;
      }
      return total;
    }
  );

  // 全会員情報インターフェース
  interface Member {
    id: number,
    name: string,
    email: string,
    points: number,
    note?: string
  }
</script>

<template>
  <section>
    <h1>会員リスト</h1>
    <p>全会員の保有ポイントの合計: {{ totalPoints }}</p>
    <OneMemver
      v-for="[id, member] in memberList"
      :key="id"
      :id="id"
      :name="member.name"
      :email="member.email"
      :points="member.points"
      :note="member.note"
    ></OneMemver>
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
