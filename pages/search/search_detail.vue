<template>
	<view class="all">
		<view class="message">
			<view class="head_detail">
				<image src="../../static/mine/head.jpg" mode="" class="head"></image>
				<view class="detail">
					<view>小明</view>
					<view>2020-01-08</view>
				</view>
			</view>
			<image src="../../static/mine/collect/pho1.jpg" mode="" class="photo"></image>
			<view class="text">第一次来成都理工大学，感觉这个新教图书馆真的好棒，里面位置多，大家都很安静，自己做自己的事情，成都理工大学牛逼！！！</view>
			<view class="like">
				<image :src='like_src' mode="" class="like_png" @click="like_click()"></image>
				<view class="like_num">{{like_num}}</view>
			</view>
		</view>
		<view style="font-size: 25px;margin-left: 5%;margin-top: 20px;">评论</view>
		<view class="comment">
			<view class="write">
				<image src="../../static/mine/head.jpg" mode="" class="head"></image>
				<input type="view" value="" placeholder="快来留下你的评论~" class="input" v-model="tmp.content" />
			</view>
			<button class="btn" @click="handin">提交</button>
			<view class="hr"></view>
			<view class="com_history">
				<view class="comment_all" v-for="(list, index) in lists" :key="index">
					<view class="comment_detail">
						<image src="../../static/mine/head.jpg" mode="" class="head"></image>
						<view class="comment_msg">
							<view>{{ list.id }}</view>
							<view>{{ list.date }}</view>
						</view>
						<view class="comment_like">
							<image :src="list.src" mode="" class="like_png" @click="comment_like_click(index)"></image>
							<view class="comment_like_num">{{ list.like_num }}</view>
						</view>
					</view>
					<view class="comment_view">{{ list.content }}</view>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
export default {
	data() {
		return {
			like_src:'../../static/search/like.png',
			like_num:36,
			tmp: { id: '小明', date: '2020-01-08', like_num: 0, content: '',src:'../../static/search/like.png' },
			lists: [{ id: '小明', date: '2020-01-08', like_num: 5, content: '评论写的真棒，我如果有你这么会说，我就不会单身了！！',src:'../../static/search/like.png',index:0 }]
		};
	},
	methods: {
		handin() {
			if (this.tmp.content === '') {
				console.log('null');
			} else {
				this.lists.push(this.tmp);
				this.tmp = { id: '小明', date: '2020-01-08', like_num: 5, content: '' };
			}
		},
		like_click(){
			if(this.like_src=='../../static/search/like.png'){
				this.like_src='../../static/search/like_red.png';
				this.like_num++;
			}else{
				this.like_src='../../static/search/like.png';
				this.like_num--;
			}
		},
		comment_like_click(index){
			if(this.lists[index].src=='../../static/search/like.png'){
				this.lists[index].src='../../static/search/like_red.png';
				this.lists[index].like_num++;
			}else{
				this.lists[index].src='../../static/search/like.png';
				this.lists[index].like_num--;
			}
		}
	}
};
</script>

<style>
.btn {
	height: 25px;
	line-height: 20px;
	width: 60px;
	padding: 0;
	border: 1px solid #fff;
	border-radius: 5px;
	background: #d9d9d9;
	color: #ffffff;
	font-size: 15px;
	margin-left: 84%;
	margin-top: 5px;
}
.message {
	width: 100%;
	margin-top: 10px;
}
.head {
	width: 35px;
	height: 35px;
	border-radius: 50%;
	margin-top: 5px;
	margin-left: 5%;
}
.head_detail {
	display: flex;
}
.detail {
	width: 100px;
	font-size: 16px;
	margin: 5px;
}
.photo {
	width: 90%;
	margin-left: 5%;
	border-radius: 10px;
}
.text {
	font-size: 18px;
	width: 90%;
	margin-left: 5%;
}
.like {
	display: flex;
	flex-direction: row;
	font-size: 16px;
	margin-left: 85%;
}
.like_png {
	width: 20px;
	height: 20px;
	margin-right: 5px;
}
.write {
	display: flex;
	flex-direction: row;
	margin-top: 10px;
}
.input {
	width: 80%;
	height: 40px;
	margin-left: 10px;
	background-color: #f9f9f9;
	border-radius: 10px;
	padding: 5px;
}
.hr {
	width: 90%;
	margin-left: 5%;
	height: 2px;
	background-color: #f3f3f3;
	margin-top: 8px;
}
.comment_detail {
	display: flex;
	flex-direction: row;
	margin-top: 15px;
}
.comment_msg {
	width: 100px;
	font-size: 16px;
	margin-left: 10px;
}
.comment_like {
	display: flex;
	flex-direction: row;
	font-size: 16px;
	margin-left: 55%;
	margin-top: 10px;
}
.comment_view {
	width: 90%;
	margin-left: 7%;
	font-size: 18px;
	margin-top: 10px;
}
</style>
