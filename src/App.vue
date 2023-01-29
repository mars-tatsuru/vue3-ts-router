<script setup lang="ts"> 
import { reactive, provide } from 'vue';
import { RouterLink, RouterView } from 'vue-router'
import type {Member} from '../interfaces/index'


const memberList = new Map<number,Member>()
provide('memberList',reactive(memberList))

memberList.set(33456,
  {
  id: 1,
  name: 'user1'
  }
)

memberList.set(47783,
  {
  id: 2,
  name: 'user2'
  }
)

</script>

<template>
  <h1>Vue router サンプル</h1>
  <main>
    <RouterView />
  </main>
</template>

<style scoped>
</style>
