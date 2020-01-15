<template >
	<view id="content" >
		<image src="../../static/register/entrance.png" style="width: 100%;position: absolute;height: 100%;"></image>
		<!-- btn -->
		<view style="width: 100%;position: absolute;display: flex;bottom: 100px;z-index: 20;"  >
			<view style="width: 35%;margin-left: 10%;">
				<navigator url="login">
					<button class="login">登陆</button>
				</navigator>
			</view>
			<view style="width: 35%;margin-left: 10%;">
				<navigator url="regist">
					<button class="regist">注册</button>
				</navigator>
			</view>
		</view>
	</view>
</template>

<script>
	
	
	export default{
		data(){
			return {
				
			}
		}
	}
</script>

<style>

	.login .regist{
		height: 80px;
		text-align: center;
		line-height: 80px;
		font-size: 18px;
		background-color: white;
		border-radius: 10px;
	}
	.regist{
		background-color:#5BC19A;
		color: white;
	}
</style>
