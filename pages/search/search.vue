<template>
	<view class="hotSearch">
		<view style="position: relative;" >
			<image src="../../static/img/search.png" style="width: 32rpx;height: 32rpx;position: absolute;left: 30rpx;top: 24rpx;" mode=""></image>
			<input type="text" placeholder="请输入您的关键字" class="search">
		</view>
		<view>
			<text style="font-size: 32rpx;font-weight:600;margin-bottom: 30rpx;display: inline-block;">热门标签</text>
			<view class="hotLable">
				<text>
					长草颜团子
				</text>
				<text>
					情人节
				</text>
			</view>
		</view>
		<view>
			<view>
				<text style="font-size: 32rpx;font-weight:600;margin-bottom: 30rpx;display: inline-block;">搜索历史</text>
				<image src="../../static/img/delete.png" mode="" class="delete" @click="Btndelete"></image>
			</view>
			<view class="hotLable">
				<text>
					长草颜团子
				</text>
				<text>
					情人节
				</text>
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
			Btndelete(){
				uni.showModal({
				    title: '',
				    content: '是否清空历史记录',
					// mask: true,
				    success: function (res) {
				        if (res.confirm) {
				            console.log('用户点击确定');
				        } else if (res.cancel) {
				            console.log('用户点击取消');
				        }
				    }
				});
			}
		}
	}
</script>

<style lang='scss'>
	.hotSearch{
		width: 100%;
		height: 100%;
		padding: 0 30rpx;
		.delete{
			width: 36rpx;
			height: 36rpx;
			float: right;
			vertical-align: middle;
			margin-top: 15rpx;
		}
		.search{
				 /* border-image:linear-gradient(90deg, rgba(251,0,126,1), rgba(253,109,126,1)) 1 1; */
				background:rgba(255,255,255,1);
				border-radius:20px;
				margin-bottom: 15px;
				border:1px solid #FB007E; 
				font-size: 24rpx;
				height: 80rpx;
				padding-left: 82rpx;
				margin-top: 19.2px;
				/* width: 100%; */
			 }
			 .hotLable{
				 text{
					 width: 184rpx;
					 height: 60rpx;
					 background: #E9E9E9;
					 border-radius:15px;
					 font-size: 24rpx;
					 display: inline-block;
					 line-height: 60rpx;
					 text-align: center;
					 margin-bottom: 20rpx;
					 margin-right: 20rpx;
				 }
			 }
	}
 
</style>
