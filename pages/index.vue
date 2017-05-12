<template lang="html">
  <div>
    <br>
    <div id="example" v-html="content"></div>
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
import $ from 'jquery'
  
export default {
  components : {
    VueEditor
  },
  mounted: function() {
    $(document).ready(function(){
    $.fn.animate_Text = function() {
      var string = this.text();
      return this.each(function(){
      var $this = $(this);
      $this.html(string.replace(/./g, '<span class="new">$&</span>'));
      $this.find('span.new').each(function(i, el){
        setTimeout(function(){ $(el).addClass('div_opacity'); }, 20 * i);
      });
      });
    };
    $('#example').show();
    $('#example').animate_Text();
    });
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

<style>
#example .new { opacity: 0; }
#example .div_opacity {
  -webkit-transition: opacity .2s ease-in-out;
  -moz-transition: opacity .2s ease-in-out;
  -ms-transition: opacity .2s ease-in-out;
  -o-transition: opacity .2s ease-in-out;
  transition: opacity .2s ease-in-out;
  opacity: 1;
}
</style>

