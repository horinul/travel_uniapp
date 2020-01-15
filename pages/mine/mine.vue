<template>
	<view>
		<view class="com_img">
			<view class="top_img"></view>
		</view>

		<navigator url="message/message">
			<view class="btn_msg spe">
				<image src="../../static/mine/btn1.png" class="btn_img"></image>
				<view class="msg_txt">个人信息</view>
				<view class="msg_icon"></view>
			</view>
		</navigator>

		<navigator url="collect/collect">
			<view class="btn_msg">
				<image src="../../static/mine/btn2.png" class="btn_img"></image>
				<view class="msg_txt">我的收藏</view>
				<view class="msg_icon"></view>
			</view>
		</navigator>
		
		
		<view class="btn_msg">
			<image src="../../static/mine/btn3.png" class="btn_img"></image>
			<view class="msg_txt">我的评论</view>
			<view class="msg_icon"></view>
		</view>
		
		<view class="btn_msg">
			<image src="../../static/mine/btn4.png" class="btn_img"></image>
			<view class="msg_txt">我的足迹</view>
			<view class="msg_icon"></view>
		</view>
		
		
		
	</view>
</template>

<script>
export default {
	data() {
		return {};
	},
	methods: {}
};
</script>

<style lang="scss">
.com_img {
	margin-top: 80px;
	width: 100%;
}
.top_img {
	height: 80px;
	width: 80px;
	margin: 0 auto;
	background-color: #5BC19A;
	border-radius: 50%;
	margin-top: 20px;
	background: url(../../static/mine/head.jpg) ;
	background-size: 100% 100%;
}

.btn_msg{
	height: 50px;
	width: 80%;
	margin: 0 auto;
	display: flex;
	margin-top: 15px;
	border: 1px solid #5BC19A;
	border-radius: 5px;
	line-height: 50px;
	position: relative;
}
.spe{
	margin-top: 40px;
}
.btn_img{
	margin-left: 10px;
	height: 20px;
	width: 20px;
	margin-top: 15px;
}

.msg_txt{
	width: 60%;
	height: 100%;
	margin-left: 15px;
}
.msg_icon{
	height:0;
	width: 0;
	border-top: 10px solid transparent;
	border-bottom:  10px solid transparent;
	border-left: 10px solid #5BC19A;
	margin-top: 15px;
	position: absolute;
	right: 20px;
}
</style>
