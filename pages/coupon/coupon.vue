<template>
	<view class="coupon">
	   <view class="title">
		   <text style="display: inline-block;margin-top: -35rpx;">提示：</text>
		   <text style="display: inline-block;width: 590rpx;">
			   未完成或支付中断时，优惠券将在2分钟后自动返回至您的账户
		   </text>
	   </view>
	   <view class="cards">
		   <view class="discount">
			   8.5折
		   </view>
		   <view class="mes">
			   <view class="name">
				   LLJ夹机占新人专享劵
			   </view>
			   <view class="ones">
				   仅限单次抓取使用
			   </view>
			   <view class="time">
				   截止:2020-20-22 08:12:23
			   </view>
		   </view>
		   <view class="button">
			   使用
		   </view>
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
	.coupon{
		width: 100%;
		height: 100%;
		padding: 20rpx;
		/* background: #F8F8F8; */
		display: flex;
		flex-direction: column;
		.title{
			color: #C100E4;
			font-size: 24rpx;
			height: 96rpx;
			background: #f7edf7;
			padding: 16rpx 20rpx;
			display: flex;
			flex-direction: row;
			align-items: center;
			/* text-align: center; */
			/* line-height: 96rpx; */
		}
		.cards{
			background: #F8F8F8;
			height: 160rpx;
			margin-top: 30rpx;
			display: flex;
			flex-direction: row;
			align-items: center;
			.discount{
				height: 112rpx;
				width: 120rpx;
				padding-left: 32rpx;
				line-height: 100rpx;
				border-right: 2rpx dashed #C8C7CC;
				color: #FB007E;
				font-size: 40rpx;
				font-weight: 600;
			}
			.mes{
				display: flex;
				flex-direction: column;
				padding-left: 30rpx;
				line-height: 38rpx;
				.name{
					font-size: 28rpx;
					font-weight: 600;
				}
				.ones{
					color: #FB007E;
					font-size: 24rpx;
					font-weight:400;
				}
				.time{
					color: #999999;
					font-size: 24rpx;
				}
			}
			.button{
				background:linear-gradient(90deg,rgba(255,0,124,1) 0%,rgba(255,117,126,1) 100%);
				width: 112rpx;
				height: 64rpx;
				border-radius: 24px;
				font-size: 28rpx;
				color: #FFFFFF;
				text-align: center;
				line-height: 64rpx;
				margin-left: 76rpx;
			}
		}
	}
</style>
