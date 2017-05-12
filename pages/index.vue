<template>
<div>
  <br>
  <br>
  <div v-html="content"></div>
  <br>
  <hr> 
  <br>
  <button @click="saveContent">SEND in CONSOLE</button>
  <br>
  <br>
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
       content: 'Some initial content' 
     }
  },
  methods: {
    saveContent() {
      console.log(this.content)
    }
  }
}
</script>

