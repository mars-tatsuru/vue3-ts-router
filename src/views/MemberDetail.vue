<script setup lang="ts">
import { RouterLink } from 'vue-router';
import { inject, computed } from 'vue';
import type { Member } from 'interfaces';

interface Props {
  id: number
}

const props = defineProps<Props>()
const memberList = inject('memberList') as Map<number, Member>

const member = computed((): Member => {
  return memberList.get(props.id) as Member
})

</script>

<template>
  <h1>Detail</h1>
  <section>
    <h2>会員情報</h2>
    <p>{{member.id}}</p>
  </section>
</template>

