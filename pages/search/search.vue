<template>
	<view>
		<uni-grid column="2" :showBorder="false" style="height:100%;padding: 0;" :square="false">
			<uni-grid-item v-for="(item, index) in list" :key="index" style="width: 50%;margin-bottom: 10px;">
				<navigator url="search_detail">
					<view class="comment">
						<image :src="item.src" style="width: 90%;height: 300px;border-radius: 7px;margin-left: 5%;"></image>
						<text class="text">{{ item.text }}</text>
					</view>
					<view class="detail">
						<view class="id">
							<image src="../../static/mine/head.jpg" class="head"></image>
							<text>{{item.id}}</text>
						</view>
						<view class="like">
							<image src="../../static/search/like.png" class="like_png" @click="click_like()"></image>
							<text>{{item.like_number}}</text>
						</view>
					</view>
				</navigator>
			</uni-grid-item>
		</uni-grid>
	</view>
</template>

<script>
import uniGrid from '@/components/uni-grid/uni-grid.vue';
import uniGridItem from '@/components/uni-grid-item/uni-grid-item.vue';

export default {
	data() {
		return {
			list: [
				{ text: '今天新教的天气真好', src: '../../static/index/canteen.jpg',like_number:25,id:'小明' },
				{ text: '今天新教的天气真好', src: '../../static/register/entrance.png',like_number:22,id:'小红' },
				{ text: '今天新教的天气真好', src: '../../static/index/library.jpg',like_number:26,id:'小王' },
				{ text: '今天新教的天气真好', src: '../../static/index/canteen.jpg',like_number:56,id:'小明' },
				{ text: '今天新教的天气真好', src: '../../static/register/entrance.png',like_number:45,id:'小明' },
				{ text: '今天新教的天气真好', src: '../../static/index/library.jpg',like_number:89,id:'大明' },
				{ text: '今天新教的天气真好', src: '../../static/register/entrance.png',like_number:23,id:'小明' },
				{ text: '今天新教的天气真好', src: '../../static/index/canteen.jpg',like_number:25,id:'小明' },
				{ text: '今天新教的天气真好', src: '../../static/register/entrance.png',like_number:45,id:'小明' },
				{ text: '今天新教的天气真好', src: '../../static/index/library.jpg',like_number:23,id:'小明' }
			]
		};
	},
	methods: {
		click_like(){
			this.list.like_number++;
		}
	},
	components: {
		uniGrid,
		uniGridItem
	}
};
</script>

<style>
.text {
	font-size: 18px;
	width: 90%;
	margin-left: 5%;
}
.detail {
	width: 90%;
	margin-left: 5%;
	display: flex;
	flex-direction: row;
	margin-top: 5px;
}
.head {
	height: 25px;
	width: 25px;
	border-radius: 50%;
}
.id {
	width: 80%;
	font-size: 18px;
	display: flex;
	flex-direction: row;
}
.like {
	width: 30%;
	font-size: 18px;
	display: flex;
	flex-direction: row;
}
.like_png {
	width: 20px;
	height: 20px;
	margin-top: 1px;
	margin-right: 5px;
}
</style>
