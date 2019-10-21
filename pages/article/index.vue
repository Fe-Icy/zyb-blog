<template>
  <RichText :data="article" />
</template>

<script>
import RichText from '~/components/RichText.vue'

export default {
  components: { RichText },
  data() {
    return {
      article: 132
    }
  }
}
</script>

<style scoped>

</style>