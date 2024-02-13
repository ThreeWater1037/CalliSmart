<template>
	<h1>请选择您练习的字体</h1>
  <div  class="font-select">
    <select :value="FontId" @change="changeFont">
      <option value="1">楷书</option>
      <option value="2">行书</option>
      <option value="3">隶书</option>
      <option value="4">草书</option>
      <option value="5">篆书</option>
    </select>
  </div>
</template>

<script>
export default {
  props: {
    FontId:String
	},
	methods:{
		changeFont(e){
			this.$emit('changeFont',e.target.value)
		}
	}
 }
</script>

<style scoped>
	
</style>
