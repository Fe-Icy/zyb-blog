<template>
  <div class="date">2019年10月20日 12:44 <span v-if="action">{{action}}</span></div>
</template>

<script>
export default {
  props: ['timestamp', 'action']
}
</script>

<style scoped>
.date {
  font-size: 14px;
  letter-spacing: 0;
  color: rgba(0, 0, 0, .7);
}
</style>