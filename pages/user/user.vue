<template>
    <view class="content">
		<view class="container">
			<view class="CaPut">
				<view class="CaPutDiv">
					<view class="ImgBorder">
						<image src="../../static/img/ping.jpg" mode=""></image>
					</view>
				</view>
				<!-- <image src="../../static/img/ping.jpg" mode=""></image> -->
			</view>
			<view class="contents">
				<ul class="ul">
					<li @click="coupon"><image class="icon"  src="http://39.107.56.148/image/youhui.png" mode=""></image>我的优惠卷<image class="right" src="http://39.107.56.148/image/right.png" mode=""></image></li>
					<!-- <li><image class="icon" src="http://39.107.56.148/image/xiaofie.png" mode=""></image>消费记录<image class="right" src="http://39.107.56.148/image/right.png" mode=""></image></li> -->
					<!-- <li><image class="icon" src="http://39.107.56.148/image/tiqu.png" mode=""></image>提取记录<image class="right" src="http://39.107.56.148/image/right.png" mode=""></image></li> -->
					<li @click="number"><image class="icon" src="http://39.107.56.148/image/shouji.png" mode=""></image>手机号<image class="right" src="http://39.107.56.148/image/right.png" mode=""></image></li>
					<li @click="site"><image class="icon" src="http://39.107.56.148/image/dizhi.png" mode=""></image>地址管理<image class="right" src="http://39.107.56.148/image/right.png" mode=""></image></li>
					<li><image class="icon" src="http://39.107.56.148/image/xieyi.png" mode=""></image>使用协议<image class="right" src="http://39.107.56.148/image/right.png" mode=""></image></li>
				</ul>
			</view>
		   <view class="button">
			   联系客服
		   </view>
		</view>
    </view>
</template>

<script>
    export default {
        methods: {
			coupon(){
				uni.navigateTo({
					url: '/pages/coupon/coupon'
				})
			},
			number(){
				uni.navigateTo({
					url: '/pages/number/number'
				})
			},
			site(){
				uni.navigateTo({
					url: '/pages/site/site'
				})
			}
        },
		onShow(){
			uni.setTabBarItem({
				index: 0,
				text: '首页',
				"iconPath": "static/img/hidden_index2.png",
				"selectedIconPath": "static/img/hidden_index1.png"
			})
			uni.setTabBarItem({
			  index: 1,
			  text: '娃柜',
			 "iconPath": "static/img/hidden_case2.png",
			  selectedIconPath: 'static/img/hidden_case2.png'
			})
			uni.setTabBarItem({
			  index: 2,
			  text: '我的',
			 "iconPath": "static/img/hidden_user1.png",
			  selectedIconPath: 'static/img/hidden_user1.png'
			})
			uni.setTabBarStyle({
			  color: '#FF0000',
			  selectedColor: '#FFFFFF',
			  backgroundColor: '#2E00C4',
			  borderStyle: 'white'
			})
		}
    }
</script>

<style lang='scss'>
	.content{
		width: 100%;
		/* height: 100%; */
		background: linear-gradient(180deg,rgba(174,0,233,1) 0%,rgba(96,0,253,1) 57%,rgba(46,0,196,1) 100%);;
		.container{
			width: 100%;
			height: 100%;
			background: url("http://39.107.56.148/image/bg1.png") no-repeat 100% 100%;
			background-size: cover;
			display: flex;
			flex-direction: column;
			align-items: center;
			.CaPut{
				height: 384rpx;
				width: 100%;
				display: flex;
				flex-direction: column;
				align-items: center;
				justify-content: center;
				.CaPutDiv{
					width: 310rpx;
					height: 200rpx;
					background: url("http://39.107.56.148/image/head_bg1.png") no-repeat 100%;
					background-size: cover;
					display: flex;
					align-items: center;
					justify-content: center;
					.ImgBorder{
						width: 161rpx;
						height: 161rpx;
						border-radius: 50%;
						border: 3px solid #d27df3;
						overflow: hidden;
						padding: 2px;
						image{
							width: 100%;
							height: 100%;
							border-radius: 50%;
						}
					}
				}
				
			}
			.contents{
				width: 690rpx; 
				height: 600rpx;
				background: url("http://39.107.56.148/image/user_bg.png") no-repeat;
				background-size: contain;
				.ul{
				  display: flex;
				  flex-direction: column;
				  justify-content: center;
				  align-items: center;
				  list-style: none;
				  margin: 0;
				  padding: 0;
				  margin-top: 25rpx;
				  li{
					  height: 140rpx;
					  line-height: 92rpx;
					  margin-top: 5rpx;
					  font-size: 24rpx;
					  color: #FFFFFF;
					  width: 600rpx;
					  font-weight:600;
					  /* background: red; */
					  /* background: url("http://39.107.56.148/image/rigt.png")  no-repeat; */
					.icon{
						float: left;
						width: 44rpx;
						height: 44rpx;
						margin-top: 28rpx;
						margin-right: 20rpx;
					}
					.right{
						width: 28rpx;
						height: 28rpx;
						float: right;
						vertical-align: middle;
						margin-top: 30rpx;
					}
				  }
				}
			}
			.button{
				width: 690rpx;
				height: 96rpx;
				background:linear-gradient(90deg,rgba(255,0,124,1) 0%,rgba(255,117,126,1) 100%);
				border-radius: 24px;
				text-align: center;
				line-height: 96rpx;
				font-size: 28rpx;
				color: #FFFFFF;
				margin-top: 108rpx;
			}
		}
	}
</style>
