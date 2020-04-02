<template>
	<view class="plush">
	  <view class="plushList">
		  <image class="robot" src="../../static/img/machine.png" mode=""></image>
		  <div class="preview">
			  <image src="http://39.107.56.148/image/previewImg.png" class="previewImg" mode=""></image>
			  <image @click="showMes" src="../../static/img/previewTit.png" class="tit" mode=""></image>
		  </div>
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
	  <!-- <view id="popup" >
			  <view class="">
				  商品详情
			  </view>
	  </view> -->
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			}
		},
		methods: {
			showMes(){
				
			}
		}
	}
</script>

<style lang='scss'>
    .plush{
		width: 100%;
		background: url('https://cdn.lljgame.com/wechat_carnival%2Fdetail_bg.png') no-repeat;
		background-size: cover;
		/* height: 100%; */
		/* background: red; */
		overflow: hidden;
		 #popup{
			height: 1250rpx;
			width: 100%;
			position: absolute;
			bottom: -1250rpx;
			right: 0;
			background:linear-gradient(180deg,rgba(193,0,228,1) 0%,rgba(96,0,253,1) 57%,rgba(46,0,196,1) 100%);
			transform: translateY(0rpx);
			transition: all .2s ease-in 0ms;
		}
		.plushList{
			width: 100%;
			.robot{
				width: 100%;
				height: 1240rpx;
			}
			.preview{
				width: 420rpx;
				height: 240rpx;
				/* background: red; */
				position: absolute;
				left: 166rpx;
				top: 252rpx;
				overflow: hidden;
				.previewImg{
					width: 100%;
					height: 100%;
				}
				.tit{
					position: absolute;
					bottom: 0;
					right: 0;
					width: 420rpx;
					height: 40rpx;
				}
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
