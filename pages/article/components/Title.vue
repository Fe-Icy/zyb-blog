<template>
  <h1 class="title">
    {{title}}
  </h1>
</template>

<script>
export default {
  props: ['title']
}
</script>

<style scoped>
.title {
  margin-bottom: 16px;
  font-size: 42px;
  color: #1a1a1a;
  opacity: 0.85;
}
</style>