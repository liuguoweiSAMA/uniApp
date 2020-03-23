<template>
	<view class="details">
		<view class="titImg">
			<image src="https://cdn.lljgame.com/15840137762444a2a723bc50c2f5390f0173ffa8b479.png" mode=""></image>
		</view>
		<view class="productList" >
			<view class="headline">
				<text>商品详情</text>	
			</view>
			<scroll-view class="menus" scroll-x="true" scroll-y="true">
			<view class="proList">
				<view class="card">
					<view>
						<image src="../../static/img/productDetail.png" mode=""></image>
					</view>
					<view>
						<view style="margin-top: 10rpx;height: 60rpx;width: 150rpx;white-space: pre-wrap;">
							GON'S旱獭圣诞系列
						</view>
						<text style="margin-top:30rpx;display: inline-block;font-size: 32rpx;">￥68</text>
					</view>
				</view>
				<view class="card">
					<view>
						<image src="../../static/img/productDetail.png" mode=""></image>
					</view>
					<view>
						<view style="margin-top: 10rpx;height: 60rpx;width: 150rpx;white-space: pre-wrap;">
							GON'S旱獭圣诞系列
						</view>
						<text style="margin-top:30rpx;display: inline-block;font-size: 32rpx;">￥68</text>
					</view>
				</view>
				<view class="card">
					<view>
						<image src="../../static/img/productDetail.png" mode=""></image>
					</view>
					<view>
						<view style="margin-top: 10rpx;height: 60rpx;width: 150rpx;white-space: pre-wrap;">
							GON'S旱獭圣诞系列
						</view>
						<text style="margin-top:30rpx;display: inline-block;font-size: 32rpx;">￥68</text>
					</view>
				</view>
				<view class="card">
					<view>
						<image src="../../static/img/productDetail.png" mode=""></image>
					</view>
					<view>
						<view style="margin-top: 10rpx;height: 60rpx;width: 150rpx;white-space: pre-wrap;">
							GON'S旱獭圣诞系列
						</view>
						<text style="margin-top:30rpx;display: inline-block;font-size: 32rpx;">￥68</text>
					</view>
				</view>
				<view class="card">
					<view>
						<image src="../../static/img/productDetail.png" mode=""></image>
					</view>
					<view>
						<view style="margin-top: 10rpx;height: 60rpx;width: 150rpx;white-space: pre-wrap;">
							GON'S旱獭圣诞系列
						</view>
						<text style="margin-top:30rpx;display: inline-block;font-size: 32rpx;">￥68</text>
					</view>
				</view>
				<view class="card">
					<view>
						<image src="../../static/img/productDetail.png" mode=""></image>
					</view>
					<view>
						<view style="margin-top: 10rpx;height: 60rpx;width: 150rpx;white-space: pre-wrap;">
							GON'S旱獭圣诞系列
						</view>
						<text style="margin-top:30rpx;display: inline-block;font-size: 32rpx;">￥68</text>
					</view>
				</view>
				<view class="card">
					<view>
						<image src="../../static/img/productDetail.png" mode=""></image>
					</view>
					<view>
						<view style="margin-top: 10rpx;height: 60rpx;width: 150rpx;white-space: pre-wrap;">
							GON'S旱獭圣诞系列
						</view>
						<text style="margin-top:30rpx;display: inline-block;font-size: 32rpx;">￥68</text>
					</view>
				</view> 
				<view class="card">
					<view>
						<image src="../../static/img/productDetail.png" mode=""></image>
					</view>
					<view>
						<view style="margin-top: 10rpx;height: 60rpx;width: 150rpx;white-space: pre-wrap;">
							GON'S旱獭圣诞系列
						</view>
						<text style="margin-top:30rpx;display: inline-block;font-size: 32rpx;">￥68</text>
					</view>
				</view>
				<view class="card">
					<view>
						<image src="../../static/img/productDetail.png" mode=""></image>
					</view>
					<view>
						<view style="margin-top: 10rpx;height: 60rpx;width: 150rpx;white-space: pre-wrap;">
							GON'S旱獭圣诞系列
						</view>
						<text style="margin-top:30rpx;display: inline-block;font-size: 32rpx;">￥68</text>
					</view>
				</view>
				<view class="card">
					<view>
						<image src="../../static/img/productDetail.png" mode=""></image>
					</view>
					<view>
						<view style="margin-top: 10rpx;height: 60rpx;width: 150rpx;white-space: pre-wrap;">
							GON'S旱獭圣诞系列
						</view>
						<text style="margin-top:30rpx;display: inline-block;font-size: 32rpx;">￥68</text>
					</view>
				</view>
			</view>
			</scroll-view>
		</view>
	</view>
</template>

<script>
	// import indexBackgroundImage from "@/static/img/bgClolor.png"
	export default {
		data() {
			return {
				// indexBackgroundImage:indexBackgroundImage
			}
		},
		methods: {
			
		}
	}
</script>

<style lang='scss'>
	*{
		margin: 0;
		padding: 0;
	}
	html, body {
		height: 100%;
	}
  .details{
	width: 100%;
	height: 100%;
	/* overflow: hidden; */
	background: url('https://cdn.lljgame.com/wechat_carnival%2Fdetail_bg.png') no-repeat; 
	background-size: cover;
	.productList{
		/* padding:  0 30rpx; */
		background: url('http://m.qpic.cn/psc?/V12lxWdB1s9Mfe/n.zGh5iTxIbbdjg4.d1VA5Hzvcxs13k6XcmFi673BijAipeD0hcNmBzsGaxzxp*cvt0PL9nPy*cthjnlQArtgQ!!/mnull&bo=3AXEBtwFxAYDByI!&rf=photolist&t=5') no-repeat;
		/* background: red; */
		background-size: 100% 100%;
		height:calc(100vh - 600rpx);
		width: 100%;
		.menus{
			 height:calc(100vh - 700rpx);
			 overflow: scroll;
		}
		.headline{
			display: flex;
			flex-direction: column;
			align-items: center;
			font-size: 32rpx;
			/* background: red; */
			color: #FFFFFF;
			padding-top: 30rpx;
		}
		.proList{
			display: flex;
			flex-direction: row;
			justify-content:space-around;
			/* align-items: center; */
			/* padding: 0 30rpx; */
			/* padding-left: 30rpx; */
			/* padding-right: 30rpx; */
			/* justify-content: center; */
			flex-wrap: wrap;
			width: 100%;
			
			/* background: red; */
			/* height: calc(900rpx - 600rpx); */
			
		}
		.card{
			width: 330rpx;
			height: 150rpx;
			display: flex;
			flex-direction: row;
			font-size: 24rpx;
			background:rgba(0,0,0,0.3);
			border-radius:10px;
			margin-top: 40rpx;
			color: #FFFFFF;
			image{
				width: 150rpx;
				height: 150rpx;
				margin-right: 10rpx;
			}
		}
	}
	.titImg{
		display: flex;
		flex-direction: column;
		align-items: center;
		height: 600rpx;
		image{
			width: 600rpx;
			height: 600rpx;
		}
	}
  }
</style>
