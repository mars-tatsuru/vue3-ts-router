<script setup lang="ts">
import { RouterLink } from 'vue-router';
</script>

<template>
  <h1>TOP</h1>
  <section>
    <RouterLink :to="{name: 'about'}">
      <p>会員管理はこちら</p>
    </RouterLink>
  </section>
</template>


<style scoped>

</style>