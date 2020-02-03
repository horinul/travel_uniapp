<template>
	<view>
		<view>
			<image src="../../static/detail/scenc.png" class="photo"></image>
		</view>
		<view class="com2">
			<textarea type="text" v-model="tmp.comment" class="input" placeholder="快点评价吧~" placeholder-style="font-size:18px;line-height:16px;padding-right:20px;"></textarea>
			<button @click="sub" class="btn">提交</button>
		</view>
		<view style="margin-top: 10px;">
			<view v-for="(item, i) in list" :key="i" class="compon">
				<view style="display: flex; height: 25px;line-height: 25px;">
					<image :src="item.url" class="img"></image>
					<view class="name">{{ item.name }}</view>
					<view class="time">{{ item.time }}</view>
				</view>
				<view class="comment" style="margin-left: 53px;font-size: 17px;">{{ item.comment }}</view>
			</view>
		</view>
	</view>
</template>

<script>
export default {
	data() {
		return {
			list: [
				{
					name: '111',
					time: '2019-01-01',
					comment: '常欲栖山岛，闲眠玉洞寒。',
					url: '../../static/mine/head.jpg'
				},
				{
					name: '222',
					time: '2019-02-02',
					comment: '丹哥时引舞，来去跨云鸾。',
					url: '../../static/mine/head.jpg'
				},
				{
					name: '333',
					time: '2019-03-03',
					comment: '共骇群龙水上游，不知原是木兰舟。',
					url: '../../static/mine/head.jpg'
				}
			],
			tmp: {
				name: '444',
				time: '2019-04-04',
				comment: '',
				url: '../../static/index/introTest.jpg'
			}
		};
	},
	methods: {
		sub: function() {
			if (this.tmp.comment === '') {
				console.log('null');
			} else {
				this.list.push(this.tmp);
				this.tmp = {
					name: '444',
					time: '2019-04-04',
					comment: '',
					url: '../../static/index/introTest.jpg'
				};
			}
		}
	}
};
</script>

<style>
.photo{
	width: 100%;
}
.compon {
	width: 90%;
	margin: 0 auto;
	margin: 0 auto;
	border: 1px solid #5BC19A;
	border-radius: 5px;
	margin-top: 10px;
}
.img {
	height: 30px;
	width: 30px;
	border-radius: 50%;
	margin: 10px;
}
.name {
	color: #2c405a;
	font-weight: bold;
	font-size: 15px;
	margin-left: 5px;
}
.time {
	font-size: 12px;
	color: #999999;
	margin-left: 25px;
}
.com2 {
	height: 100px;
	width: 90%;
	margin: 0 auto;
	background-color: #edf7fa;
	margin-top: 10px;
	border: 1px solid #5BC19A;
	border-radius: 10px;
	position: relative;
}
.input {
	height: 100px;
	width: 100%;
	border-radius: 5px;
	margin-left: 5px;
	margin-top: 5px;
	padding-right: 20px;
}
.btn {
	height: 25px;
	line-height: 25px;
	width: 60px;
	padding: 0;
	border: 1px solid #fff;
	border-radius: 10px;
	background: #5BC19A;
	color: #ffffff;
	font-size: 15px;
	position: absolute;
	bottom: 2px;
	right: 2px;
	z-index: 10;
}
</style>
