<template>
  <div class="frontend">
  </div>
</template>

<script>
import Header from '~/components/Header.vue'

export default {
  components: {
    'v-header': Header
  },
  created() {
  }
}
</script>

<style scoped>
.frontend {
  margin: 0 auto;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  height: 100vh;
}
</style>
