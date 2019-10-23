<template>
  <div class="article-container">
    <div class="article-body">
      <input v-model="title" class="article-title" />
      <Editor
        class="article-content"
        :content="content"
        @onEditorChange="onEditorChange"
      />
    </div>
    <div class="article-preview">
      <h1>{{title}}</h1>
      <RichText :text="content" />
    </div>
  </div>
</template>

<script>
import Editor from '~/components/Editor.vue'
import RichText from '~/components/RichText.vue'

export default {
  components: {
    Editor,
    RichText
  },
  data() {
    return {
      content: `<p>123</p>`,
      title: ''
    }
  },
  methods: {
    onEditorChange(e) {
      this.content = e.html
    }
  },
}
</script>

<style scoped>
.article-container {
  margin: 200px auto;
  max-width: 1200px;
  display: flex;
}

.article-body {
  width: 50%;
}

.article-preview {
  width: 50%;
  margin-left: 20px;
}
</style>