<template>
	<view class="all">
		<view class="component" v-for="(item, index) in lists" :key="index">
			<image :src="item.src" class="img"></image>
			<text class="text">{{ item.text }}</text>
		</view>
	</view>
</template>

<script>
export default {
	data() {
		return {
			lists: [
				{ text: '成都理工大学传播科学与艺术学院下设影视编导系、戏剧影视文学系、播音主持系、表演系、音乐系、视觉艺术系、现代设计系、广播电视系、广告系9个教学系', src: '../../../static/index/library.jpg' },
				{ text: '成都理工大学体育学院成立于2010年，是成都理工大学最年轻、最活力的学院之一，学院以“术学同体，才德共育”为院训，依托学校优势学科专业', src: '../../../static/index/sport.jpg' }
			]
		};
	}
};
</script>

<style>
.component {
	display: flex;
}
.img {
	height: 130px;
	flex: 4;
	margin: 10px;
	border-radius: 10px;
}
.text {
	flex: 6;
	margin: 12px;
	font-size: 18px;
}
</style>
