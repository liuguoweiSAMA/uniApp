<template>
	<view class="plush">
	  <view class="plushList">
		  <image src="../../static/img/machine.png" mode=""></image>
	  </view>
	  <view style="display: flex;justify-content:space-evenly;">
		  <view class="noes">
			  夹一次
			  <view style="font-size: 24rpx;">
				  ￥59
			  </view>
		  </view>
		  <view class="five">
			  夹五 次
			  <view style="font-size: 24rpx;">
				  ￥59
			  </view>
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
    .plush{
		width: 100%;
		background: url('https://cdn.lljgame.com/wechat_carnival%2Fdetail_bg.png') no-repeat;
		background-size: cover;
		 /* background: red; */
		.plushList{
			width: 100%;
			image{
				width: 100%;
				height: 1240rpx;
			}
		}
		.noes{
			width: 230rpx;
			height: 102rpx;
			background: url('https://cdn.lljgame.com/wechat_carnival%2Fplay_pay.png') no-repeat;
			background-size: cover;
			text-align: center;
			/* font-family:HYQiHei-HES,HYQiHei; */
			font-weight: bold;
			font-size: 36rpx;
		}
		.five{
			width: 230rpx;
			height: 102rpx;
			background: url('https://cdn.lljgame.com/wechat_carnival%2Fplay_pay.png') no-repeat;
			background-size: cover;
			text-align: center;
			/* font-family:HYQiHei-HES,HYQiHei; */
			font-weight: bold;
			font-size: 36rpx;
		}
	}
	
</style>
