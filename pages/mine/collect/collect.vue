<template>
	<view class="content">
		<view v-for="(list , index) in lists" :key="index" class="flex">
			<checkbox value="msg"></checkbox>
			<view class="main">
				<image :src="list.img" class="scene"></image>
				<text class="text">{{ list.introText }}</text>
			</view>
		</view>
	</view>
</template>

<script>
export default {
	data() {
		return {
			lists: 
			[
				{ img: '../../../static/mine/collect/pho1.jpg', introText: '成都理工大学新教学楼，建于多少年我也不知道，我词穷，不知道写什么了，就等李大佬后端传数据了',msg:'' },
				{ img: '../../../static/mine/collect/pho1.jpg', introText: '成都理工大学新教学楼，建于多少年我也不知道，我词穷，不知道写什么了，就等李大佬后端传数据了',msg:''  },
				{ img: '../../../static/mine/collect/pho1.jpg', introText: '成都理工大学新教学楼，建于多少年我也不知道，我词穷，不知道写什么了，就等李大佬后端传数据了',msg:''  },
				{ img: '../../../static/mine/collect/pho1.jpg', introText: '成都理工大学新教学楼，建于多少年我也不知道，我词穷，不知道写什么了，就等李大佬后端传数据了',msg:''  },
			]
		};
	}
};
</script>

<style>
	checkbox{
		margin-top: 30px;
	}
	.flex{
		display: flex;
		padding: 15px;
	}

	.scene{
		width: 30%;
		height: 100px;
		border-radius: 15px;
	}
	.main{
		display: flex;
		height: 100px;	
	}
	.text{
		width: 65%;
		height: 100px;
		font-size: 16px;
		margin-left: 5%;
		margin-top: 10px;
	}
</style>
