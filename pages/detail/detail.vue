<template>
	<view>
		<view class="top" style="height: 200px;width: 100%;">
			<image src="../../static/detail/scenc.png"></image>
			<navigator url="../comment/comment">
				<view class="top_icon"></view>
			</navigator>
		</view>
		<view class="intro">
			成都市，简称“蓉”，别称“锦城”、“锦官城”，自古被誉为“天府之国”，位于四川盆地西部，成都平原腹地，是中国副省级城市之一，西南地区的中心城市之一，四川省政治、经济、文化中心，中国大陆地区机构、央企、外企西部或西南区域总部驻地主要城市之一。2007年，重庆市和四川省成都市的全国统筹城乡综合配套改革试验区获国务院批准。2007年，成都市被国家确定为中国最佳旅游城市之一。
			2010年成都市生产总值（GDP）5551.3亿，为全国省会城市第3名，大陆城市12位。 2009年，世界优秀旅游目的地城市中 …
			成都市，简称“蓉”，别称“锦城”、“锦官城”，自古被誉为“天府之国”，位于四川盆地西部，成都平原腹地，是中国副省级城市之一，西南地区的中心城市之一，四川省政治、经济、文化中心，中国大陆地区机构、央企、外企西部或西南区域总部驻地主要城市之一。2007年，重庆市和四川省成都市的全国统筹城乡综合配套改革试验区获国务院批准。2007年，成都市被国家确定为中国最佳旅游城市之一。
			2010年成都市生产总值（GDP）5551.3亿，为全国省会城市第3名，大陆城市12位。 2009年，世界优秀旅游目的地城市中 …
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

<style>
image {
	width: 100%;
	height: 100%;
	background: #2c405a;
}
.top_icon {
	height: 50px;
	width: 50px;
	border-radius: 50%;
	border: 1px solid #808080;
	background: url(../../static/detail/comment.png) no-repeat;
	background-position: center;
	background-size: 25px;
	background-color: #5BC19A;
	position: absolute;
	top: 175px;
	right: 25px;
}
.top_txt {
	color: #fff;
	position: absolute;
	top: 170px;
	left: 25px;
	font-size: 18px;
}
.intro{
	width: 90%;
	margin: 0 auto;
	border: 1px solid #999999;
	border-radius: 5px;
	margin-top: 10px;
	
}
</style>
