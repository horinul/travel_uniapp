<template>
	<view style="width: 100%;">
		
		<view class="icon">
			<image src="../../static/register/icon.jpg" style="width: 280px;height: 210px;margin: 0 auto;"></image>
		</view>
		
		<view class="input">
			<view style="position: relative;">
				<image src="../../static/register/user.png" class="icon-user"></image>
				<input type="number" placeholder="手机号" class="user" placeholder-style="font-size:20px"/>
			</view>
			
			<view style="position: relative;">
				<image src="../../static/register/get.png" class="icon-get"></image>
				<input type="number" placeholder="验证码" class="password" password="true" placeholder-style="font-size:20px"/>
				<view class="get">获取验证码</view>
			</view>
			
			<view style="position: relative;">
				<image src="../../static/register/password.png" class="icon-password"></image>
				<input type="number" placeholder="设置密码" class="password" password="true" placeholder-style="font-size:20px"/>
			</view>
			
		</view>
		<view class="forget-password">忘记密码</view>
		<view class="btn-view">
			<button class="btn">确定</button>
		</view>

	</view>
</template>

<script>
</script>

<style>
	.icon{
		margin: 0 auto;
		width: 280px;
		height: 210px;
	}
	.user{
		border: 1px solid #5BC19A;
		border-radius: 10px;
		width: 220px;
		height: 50px;
		padding-left: 60px;
	}
	.password{
		border: 1px solid #5BC19A;
		border-radius: 10px;
		width: 220px;
		height: 50px;
		margin-top: 20px;
		padding-left: 60px;
	}
	.input{
		width: 280px;
		margin: 0 auto;
	}
	.icon-user {
		height: 40px;
		width: 40px;
		position: absolute;
		padding-left: 5px;
		padding-top: 3px;
	}
	.icon-password{
		width: 40px;
		height: 40px;
		position: absolute;
		padding-left: 5px;
		padding-top: 3px;
	}
	.icon-get{
		width: 40px;
		height: 40px;
		position: absolute;
		padding-left: 5px;
		padding-top: 5px;
	}
	.btn-view{
		width: 290px;
		margin: 0 auto;
	}
	.btn{
		width: 290px;
		height: 45px;
		background-color: #5BC19A;
		color: white;
		font-size: 18px;
		border-radius: 5px;
		margin-top: 20px;
	}
	.forget-password{
		color: #5BC19A;
		font-size: 15px;
		line-height: 15px;
		height: 15px;
		width: 280px;
		text-align: right;
		margin: 0 auto;
		margin-top: 9px;
	}
	.get{
		height: 40px;
		line-height: 40px;
		font-size: 15px;
		color: #5BC19A;
		position: absolute;
		top: 5px;
		right: 10px;
	}
</style>
