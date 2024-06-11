<template>
	<view>
		<button @click="testco()">请求云对象方法</button>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			}
		},
		methods:{
			async testco(){
				const helloco = uniCloud.importObject('helloco')
				try {
					const res = await helloco.sum(1,2)
					console.log(res)
				} catch (e){
					console.log(e)
				}
			}
		}
	}
</script>


