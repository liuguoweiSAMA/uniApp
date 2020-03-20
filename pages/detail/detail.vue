<template>
	<view class="details">
		<view class="titImg">
			<image src="https://cdn.lljgame.com/15840137762444a2a723bc50c2f5390f0173ffa8b479.png" mode=""></image>
		</view>
		<view class="productList">
			<view class="headline">
				<text>商品详情</text>	
			</view>
			<!-- <scroll-view scroll-x="true" style="overflow-y: scroll;"> -->
			<view class="proList">
				<view class="card">
					<view>
						<image src="../../static/img/productDetail.png" mode=""></image>
					</view>
					<view>
						<view style="margin-top: 10rpx;height: 60rpx;">
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
						<view style="margin-top: 10rpx;height: 60rpx;">
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
						<view style="margin-top: 10rpx;height: 60rpx;">
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
						<view style="margin-top: 10rpx;height: 60rpx;">
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
						<view style="margin-top: 10rpx;height: 60rpx;">
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
						<view style="margin-top: 10rpx;height: 60rpx;">
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
						<view style="margin-top: 10rpx;height: 60rpx;">
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
						<view style="margin-top: 10rpx;height: 60rpx;">
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
	export default {
		data() {
			return {
				
			}
		},
		methods: {
			
		}
	}
</script>

<style lang='scss'>
	html, body {
		height: 100%;
	}
  .details{
	width: 100%;
	height: 100%;
	overflow: hidden;
	background: url('https://cdn.lljgame.com/wechat_carnival%2Fdetail_bg.png') repeat; 
	background-size: cover;
	.productList{
		padding:  0 30rpx;
		background: url('https://cdn.lljgame.com/wechat_carnival%2Fdetail_bg_bottom.png');
		background-size: cover;
		height: 645rpx;
		
		/* background: red; */
		.headline{
			display: flex;
			flex-direction: column;
			align-items: center;
			font-size: 32rpx;
			color: #FFFFFF;
			padding-top: 30rpx;
		}
		.proList{
			display: flex;
			flex-direction: row;
			justify-content: space-between;
			flex-wrap: wrap;
			height: 550rpx;
			overflow: scroll;
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
		image{
			width: 600rpx;
			height: 600rpx;
		}
	}
  }
</style>
