<template>
  <div class="root">
    <v-logo />
  </div>
</template>

<script>
import Logo from '~/components/Logo.vue'

export default {
  components: {
    'v-logo': Logo
  },
  created() {
  }
}
</script>

<style scoped>
.root {
  margin: 0 auto;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}
</style>
