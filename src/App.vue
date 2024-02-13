<template>
  <div class="app">
    <FontSelect :FontId="fontID" @changeFont="changeFont"></FontSelect>
    <WordInput :Word="word" @changeWord="changeWord"></WordInput>
    <PictureSubmit></PictureSubmit>
  </div>
</template>

<script>
import FontSelect from './components/FontSelect.vue'
import WordInput from './components/WordInput.vue'
import PictureSubmit from './components/PictureSubmit.vue'
// import axios from 'axios'

export default {
  data(){
    return {
      fontID:"1",
      word:"",
    }
  },
  methods:{
    changeFont(val){
      this.fontID=val
    },
    changeWord(val){
      this.word=val
    },
},
  components:{
    FontSelect,
    WordInput,
    PictureSubmit
  }
}
</script>

<style>
.hide_file{
    display:none;
}
.camera{
    position: relative;
    z-index: 2;
    margin: 0 auto;
    margin-bottom: 10px;
    width: 138px;
    height: 138px;
    background: #E7E7E7;
    border-radius: 6px;
    text-align: center;
    .bigImg{
        width: 138px;
        height: 138px;
    }
    .icon{
        width: 40px;
        margin-top: 40px;
    }
    .text{
        display: block;
        line-height: 22px;
        font-size: 15px;
        color: #999;
        margin-top: 8px;
    }
}
</style>
