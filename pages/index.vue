<template lang="html">
<div>
  <h1>
    vue 2 editor with nuxt.js
  </h1>  
  <vue-editor v-model="content"></vue-editor>
</div>
</template>

<script>
  
import VueEditor from '../components/vueeditor.vue'
  
export default {
  components : {
    VueEditor
  },
  data() {
     return {
       content: '<h1>Some initial content</h1>'  
     }
  },
  head: {
    title : 'Vue 2 editor with nuxt.js'
  }
}
</script>

<style lang="css">
</style>

