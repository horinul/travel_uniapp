<template>
	<view class="content">
		<view v-for="(list , index) in lists" :key="index" class="flex">
			<!-- <checkbox value="msg"></checkbox> -->
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
				{ img: '../../../static/mine/collect/pho1.jpg', introText: '成都理工大学图书馆是学校的文献信息中心，是为教学和科学研究服务的学术性机构，是学校高等教育和文化建设的重要基地，是建设“双一流”大学的重要支撑平台。',msg:'' },
				{ img: '../../../static/mine/collect/pho1.jpg', introText: '成都理工大学图书馆是学校的文献信息中心，是为教学和科学研究服务的学术性机构，是学校高等教育和文化建设的重要基地，是建设“双一流”大学的重要支撑平台。',msg:''  },
				{ img: '../../../static/mine/collect/pho1.jpg', introText: '成都理工大学图书馆是学校的文献信息中心，是为教学和科学研究服务的学术性机构，是学校高等教育和文化建设的重要基地，是建设“双一流”大学的重要支撑平台。',msg:''  },
				{ img: '../../../static/mine/collect/pho1.jpg', introText: '成都理工大学图书馆是学校的文献信息中心，是为教学和科学研究服务的学术性机构，是学校高等教育和文化建设的重要基地，是建设“双一流”大学的重要支撑平台。',msg:''  },
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
		flex-direction: row;
		padding: 15px;
	}

	.scene{
		width: 20%;
		margin-left: 5%;
		border-radius: 15px;
		height: 120px;
	}
	.main{
		display: flex;
	}
	.text{
		width: 70%;
		margin-left: 5%;
		font-size: 16px;
		margin-left: 5%;
	}
</style>
