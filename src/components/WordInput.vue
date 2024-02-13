<template>
  <div class="wort-input">
    <h1>请输入您练习的字</h1>
    <input :value="Word" @change="changeWord"
    type="text" placeholder="请只输入一个字">
  </div>
</template>

<script>
export default {
  props:{
    Word:String,
  },
  methods:{
    changeWord(e){
      let value = e.target.value
      if(value){
        value = value.replace(/\s/g,"")
      }
      this.$emit('changeWord',value)
    }
  }
  
}

</script>

<style>

</style>
