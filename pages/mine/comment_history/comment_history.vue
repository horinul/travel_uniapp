<template>
	<view class="all">
		<view class="component" v-for="(item, index) in lists" :key="index">
			<view class="time">{{ item.time }}</view>
			<navigator url="../../detail/detail" class="comment_com">
				<view>
					<view class="comment">{{ item.comment }}</view>
					<view class="intro">
						<image :src="item.src" class="img"></image>
						<text class="text">{{ item.place }}</text>
						<image src="../../../static/mine/message/right.png" class="icon"></image>
					</view>
				</view>
			</navigator>
		</view>
	</view>
</template>

<script>
export default {
	data() {
		return {
			lists: [
				{
					time: '2020-1-4',
					comment: '第一次来成都理工大学，感觉这个新教图书馆真的好棒，里面位置多，大家都很安静，自己做自己的事情，成都理工大学牛逼！！！',
					place: '东风渠',
					src: '../../../static/detail/scenc.png'
				},
				{
					time: '2020-1-9',
					comment: '第一次来成都理工大学，感觉这里的风景好美，真希望以后来这里读书，成都理工大学牛逼！！！',
					place: '东风渠',
					src: '../../../static/detail/scenc.png'
				},
				{
					time: '2020-1-4',
					comment: '第一次来成都理工大学，感觉这个新教图书馆真的好棒，里面位置多，大家都很安静，自己做自己的事情，成都理工大学牛逼！！！',
					place: '东风渠',
					src: '../../../static/detail/scenc.png'
				},
				{
					time: '2020-1-9',
					comment: '第一次来成都理工大学，感觉这里的风景好美，真希望以后来这里读书，成都理工大学牛逼！！！',
					place: '东风渠',
					src: '../../../static/detail/scenc.png'
				}
			]
		};
	},
	methods: {}
};
</script>

<style>
.component {
	display: flex;
	margin-top: 5px;
}
.time {
	flex: 2;
	padding: 5px;
	font-size: 16px;
	padding-left: 5px;
}
.comment_com {
	flex: 8;
	font-size: 15px;
	padding: 5px;
}
.intro {
	width: 100%;
	background-color: #fbfbfb;
	margin-top: 8px;
	display: flex;
}
.img {
	height: 60px;
	width: 100px;
	margin: 5px;
}
.text {
	font-size: 15px;
	vertical-align: top;
	height: 70px;
	line-height: 70px;
	margin-left: 10px;
}
.icon {
	width: 20px;
	height: 20px;
	margin-top: 25px;
	margin-left: 10px;
}
</style>
