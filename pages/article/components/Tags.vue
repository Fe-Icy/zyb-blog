<template>
  <ul class="tags">
    <li class="tag" v-for="(tag, index) in tags" :key="index">{{tag}}</li>
  </ul>
</template>

<script>
export default {
  props: ['tags']
}
</script>

<style scoped>
.tags {
  display: flex;
  align-items: center;
}

.tag {
  font-size: 16px;
  color: #1a1a1a;
  padding: 5px 9px;
  border: 1px solid rgba(95, 122, 175, 0.6);
  border-radius: 4px;
  line-height: 1;
  cursor: pointer;
}

.tag:hover {
  border: 1px solid rgba(35, 72, 75, 0.75);
}

.tag + .tag {
  margin-left: 10px;
}
</style>