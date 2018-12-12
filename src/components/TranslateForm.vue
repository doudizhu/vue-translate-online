<template lang="pug">
  div
  	form(v-on:submit="formSubmit")
  		input(placeholder="请输入要翻译的内容" v-model="textToTranslate")
  		select
  			option(value="en") English
  		input(type="submit" value="翻译")
</template>

<script>
export default {
	data:function(){
		return {
			textToTranslate:"",
		}
	},
	methods:{
		formSubmit:function(e){
			e.preventDefault();
			// alert(this.textToTranslate)
			this.$emit("formSubmit",this.textToTranslate); // 注册事件
		}
	},
	
}
</script>

<style>

</style>