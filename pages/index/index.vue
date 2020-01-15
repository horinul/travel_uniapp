<template>
	<view class="content">
		<view class="top" style="width: 100%;display: flex;">
			<view class="top-left">
				<text>{{ pickerText }}</text>
				<image style="width: 30px;width: 100px;" @tap="openAddres" src="../../static/index/down.png" class="choose_image"></image>
				<simple-address ref="simpleAddress" :pickerValueDefault="cityPickerValueDefault" @onConfirm="onConfirm" themeColor="#007AFF"></simple-address>
			</view>

			<view class="top-right">
				<image src="../../static/index/search.png" class="search"></image>
				<input type="text" class="input-top" placeholder="搜索有趣的美景/美食" />
			</view>
		</view>

		<view class="middle">
			<navigator url="../detail/detail">
				<swiper indicator-dots="true" indicator-active-color="#5BC19A" autoplay="true">
					<swiper-item><image :src="swiper1"></image></swiper-item>
					<swiper-item><image :src="swiper2"></image></swiper-item>
					<swiper-item><image :src="swiper3"></image></swiper-item>
					<swiper-item><image :src="swiper4"></image></swiper-item>
				</swiper>
			</navigator>
		</view>
		<!-- url导向的标志 -->
		<view class="middle-content">
			<navigator url="" class="line">
				<image class="img-line" src="../../static/index/foot.png"></image>
				<view style="font-size:14px">闲逛</view>
			</navigator>
			<navigator url="" class="line">
				<image class="img-line" src="../../static/index/sport.png"></image>
				<view style="font-size:14px">运动</view>
			</navigator>
			<navigator url="" class="line">
				<image class="img-line" src="../../static/index/science.png"></image>
				<view style="font-size:14px">科技</view>
			</navigator>
			<navigator url="" class="line">
				<image class="img-line" src="../../static/index/study.png"></image>
				<view style="font-size:14px">学习</view>
			</navigator>
			<navigator url="" class="line">
				<image class="img-line" src="../../static/index/rice.png"></image>
				<view style="font-size:14px">吃饭</view>
			</navigator>
		</view>

		<view class="intro">
			<uni-grid :column="3" :show-border="false" :square="false">
				<uni-grid-item>
					<image src="../../static/index/eat.png" class="intro-img"></image>
					<text class="intro-text">美食</text>
				</uni-grid-item>
				<uni-grid-item>
					<image src="../../static/index/event.jpg" class="intro-img"></image>
					<text class="intro-text">活动</text>
				</uni-grid-item>
				<uni-grid-item>
					<image src="../../static/index/sight.jpg" class="intro-img"></image>
					<text class="intro-text">景点</text>
				</uni-grid-item>
				<uni-grid-item>
					<image src="../../static/index/sport.jpg" class="intro-img"></image>
					<text class="intro-text">运动</text>
				</uni-grid-item>
				<uni-grid-item>
					<image src="../../static/index/canteen.jpg" class="intro-img"></image>
					<text class="intro-text">饭堂</text>
				</uni-grid-item>
				<uni-grid-item>
					<image src="../../static/index/library.jpg" class="intro-img"></image>
					<text class="intro-text">图书馆</text>
				</uni-grid-item>
			</uni-grid>
		</view>
	</view>
</template>

<script>
import simpleAddress from '../../components/simple-address/simple-address.nvue';
import uniGrid from '@/components/uni-grid/uni-grid.vue';
import uniGridItem from '@/components/uni-grid-item/uni-grid-item.vue';

export default {
	data() {
		return {
			cityPickerValueDefault: [0, 0, 1],
			pickerText: '东城区',

			swiper1: '../../static/index/swiper1.png',
			swiper2: '../../static/index/swiper2.png',
			swiper3: '../../static/index/swiper3.png',
			swiper4: '../../static/index/swiper4.png'
		};
	},
	components: {
		simpleAddress,
		uniGrid,
		uniGridItem
	},
	methods: {
		openAddres() {
			this.$refs.simpleAddress.open();
			console.log('ok');
		},
		onConfirm(e) {
			this.pickerText = e.label.split('-')[2];
		}
	}
};
</script>
<style>
.middle-content {
	display: flex;
	width: 90%;
	margin: 0 auto;
	height: 55px;
	text-align: center;
	vertical-align: middle;
	margin-top: 15px;
}
.line {
	flex: 2;
}
.img-line {
	height: 30px;
	width: 30px;
}
.top {
	margin-top: 10px;
	height: 45px;
}
.top-left {
	flex-grow: 1.5;
	margin-left: 10px;
}
.top-right {
	flex-grow: 8.5;
}
.choose_image {
	height: 20px;
	width: 20px !important;
	padding-top: 9px !important;
	text-align: center;
}
view > text {
	font-size: 20px;
	margin-left: 3px;
	margin-top: 3px;
}
.input-top {
	width: 80%;
	height: 40px;
	line-height: 40px;
	border: 1px solid #808080;
	border-radius: 5px;
	padding-left: 40px;
}
.search {
	position: absolute;
	width: 25px;
	height: 25px;
	margin-left: 10px;
	line-height: 25px;
	margin-top: 8px;
}
swiper {
	height: 230px;
	width: 90%;
	margin: 0 auto;
	margin-top: 10px;
	border-radius: 15px;
}
swiper-item {
	height: 230px;
	border-radius: 15px;
}
swiper-item > image {
	width: 100%;
	height: 230px;
	border-radius: 15px;
}
.middle {
	width: 100%;
}
uni-grid {
	width: 100%;
	margin: 0 auto;
}
uni-grid-item {
	width: 33.3%;
}
.intro {
	width: 94%;
	margin: 0 auto;
}
.intro-img {
	width: 90%;
	margin: 0 auto;
	height: 150px;
	margin-top: 20px;
	border-radius: 15px;
}
.intro-text {
	width: 95%;
	margin: 0 auto;
	height: 25px;
	line-height: 25px;
	text-align: center;
	vertical-align: middle;
	margin-top: 5px;
	font-size: 18px;
}
</style>
