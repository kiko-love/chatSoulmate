<script setup>
import { RelievedFace } from '@icon-park/vue'
</script>

<template>
  <div class="container">
    <relieved-face theme="outline" size="24" fill="#333" :stroke-width="3" />
    <h1 class="main-title">ChatSoulmate</h1>
    <div>An intelligent dialogue assistant and intimate mate</div>
  </div>
</template>

<style lang="less" scoped>
.container {
  display: flex;
  align-items: baseline;
  justify-content: flex-start;
  flex-direction: column;
  padding: 1rem 1rem;
}

.main-title {
  font-weight: 700;
  text-align: center;
}
</style>
