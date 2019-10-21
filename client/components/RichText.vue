<template>
  <div class="richtext" v-html="text" />
</template>

<script>
export default {
  props: ['text'],
}
</script>

<style scoped>
.richtext {
  font-size: 18px;
  line-height: 1.8;
}
</style>