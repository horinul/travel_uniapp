<template>
	<view class="content">
		<image :src="img"></image>
		<text>{{text}}</text>
	</view>
</template>

<script>
	export default {
		data(){
			return {
				
			}
		},
		props:['img','text'],
		
		
	}
</script>

<style>
	.content{
		width: 100%;
	}
	image{
		width: 33.3%;
		height: 100px;
	}
	text{
		width: 33.3%;
		height: 25px;
		line-height: 25px;
		text-align: 18px;
		text-align: center;
		vertical-align: middle;
	}
</style>
