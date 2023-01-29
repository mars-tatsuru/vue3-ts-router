<script setup lang="ts">
import { RouterLink } from 'vue-router';
import { inject } from 'vue';
import type { Member } from 'interfaces';


const memberList = inject('memberList') as Map<number, Member>
</script>

<template>
  <h1>ABOUT</h1>
  <section>
    <ul>
      <li
        v-for="[id,member] in memberList"
        :key="member.id"
      >
        <RouterLink
          :to="{name:'MemberDetail', params: {id: id}}"
        >
         IDが{{ id }}の{{member.name}}さん
        </RouterLink>
      </li>
    </ul>
  </section>
</template>

