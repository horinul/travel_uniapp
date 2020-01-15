<template>
	<view>
		<view class="com_img"><view class="top_img"></view></view>
		
		<!-- 灰背景 -->
		<view>
			<view class="bac1"></view>
		</view>

		<view>
			<!-- <view class="main" v-for="(title,detail,index) in lists" :key="index" >
				<view>{{title}}</view>
				<input :placeholder="detail">
			</view> -->
			<view class='msg'>
				<text>昵称</text>
				<input class="input" v-model="nameChange" />
				<view class="icon"></view>
			</view>
			
			<view class='msg'>
				<text>性别</text>
				<input class="input" v-model="sex" />
				<view class="icon"></view>
			</view>
			<view class='msg'>
				<text>简介</text>
				<input class="input" v-model="intro"  placeholder="未填写" placeholder-style="color:'#CCCCCC"/>
				<view class="icon"></view>
			</view>
			<view class='msg'>
				<text>生日</text>
				<input class="input" v-model="birthday" placeholder="未填写" placeholder-style="color:'#CCCCCC"/>
				<view class="icon"></view>
			</view>
			<view class='msg' style="border-bottom: none;">
				<text>地区</text>
				<input class="input" v-model="area" placeholder="未填写" placeholder-style="color:'#CCCCCC"/>
				<view class="icon"></view>
			</view>
			
			<!-- 灰背景 -->
			<view>
				<view class="bac2"></view>
			</view>
			
			<view class='msg'>
				<text class="spe">真实姓名</text>
				<input class="input" v-model="realName" placeholder="未填写" placeholder-style="color:'#CCCCCC"/>
				<view class="icon"></view>
			</view>
			<view class='msg'>
				<text>学校</text>
				<input class="input" v-model="school" placeholder="未填写" placeholder-style="color:'#CCCCCC"/>
				<view class="icon"></view>
			</view>
		</view>
	</view>
</template>

<script>
export default {
	data() {
		return {
			nameChange: '安室透',
			sex: '男',
			intro:'',
			birthday:'',
			area:'',
			realName:'',
			school:''
		};
	}
};
</script>

<style>
	.bac1{
		width: 80%;
		margin: 0 auto;
		background-color: #FFFAFA;
		height: 15px;
		margin-top: 20px;
	}
	.bac2{
		width: 80%;
		margin: 0 auto;
		background-color: #FFFAFA;
		height: 10px;
		margin-top: 10px;
	}
	.msg{
		display: flex;
		width: 80%;
		margin: 0 auto;
		margin-top: 5px;
		height: 50px;
		line-height: 50px;
		border-bottom: 1px solid #F0F8FF;
	}
	text{
		font-size: 20px;
		height: 50px;
		width: 20%;
	}
	.spe{
		font-size: 20px;
		height: 50px;
		width: 40%;
	}
	.input{
		height: 50px;
		line-height: 50px;
		font-size: 18px;
		text-align: right;
		width: 80%;
	}
	.top_img {
		height: 100px;
		width: 100px;
		margin: 0 auto;
		border-radius: 50%;
		margin-top: 40px;
		background: url(../../../static/mine/head.jpg);
		background-size: 100% 100%;
	}
	.icon{
		height: 20px;
		width: 20px;
		margin: 14px 0 14px 14px;
		background: url(../../../static/mine/message/right.png);
		background-size: cover;
	}
</style>
