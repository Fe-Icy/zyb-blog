<template>
  <div class="quill-editor-container">
    <div class="quill-editor"
      name="editor"
      :content="content"
      v-quill:myQuillEditor="editorOption"
      @change="onEditorChange($event)"
    />
  </div>
</template>

<script>
import hljs from 'highlight.js'
export default {
  props: ['content'],
  data() {
    return {
      editorOption: {
        modules: {
          toolbar: [
            ['bold', 'italic', 'underline', 'strike'],
            ['blockquote', 'code-block'],
            // [{ 'header': 1 }, { 'header': 2 }],
            [{ 'list': 'ordered' }, { 'list': 'bullet' }],
            // [{ 'script': 'sub' }, { 'script': 'super' }],
            [{ 'indent': '-1' }, { 'indent': '+1' }],
            [{ 'direction': 'rtl' }],
            // [{ 'size': ['small', false, 'large', 'huge'] }],
            [{ 'header': [1, 2, 3, 4, 5, 6, false] }],
            // [{ 'font': [] }],
            [{ 'color': [] }, { 'background': [] }],
            // [{ 'align': [] }],
            ['clean'],
            ['link', 'image', 'video']
          ],
          syntax: {
            highlight: text => hljs.highlightAuto(text).value
          }
        }
      }
    }
  },
  methods: {
    onEditorChange(e) {
      this.$emit('onEditorChange', e)
    }
  },
}
</script>

<style scoped>
.quill-editor-container {
  border: 1px solid #0084ff;
  border-radius: 3px;
}

.quill-editor {
  border-color: transparent;
}
</style>
