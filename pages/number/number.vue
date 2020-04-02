<template>
	<view class="number">
		<view class="numberMess">
			<view style="width: 100%;text-indent: 40rpx;">新手机号</view>
			<view>
			   <input type="text" style="font-size: 24rpx;font-weight:400;padding-left: 20rpx;" placeholder="请输入您的手机号" value="" />
			</view>
			<view style="width: 100%;text-indent: 40rpx;">
				验证码
			</view>
			<view style="display: flex;">
				<input type="text" style="width: 400rpx;font-size: 24rpx;font-weight:400;padding-left: 20rpx;"  placeholder="短信验证码" value="" />
				<view @click="codes" v-show="show"  class="codes" >
					获取验证码
				</view>
				<view @click="codes"  v-show="!show"  class="codes"  >
					{{num}}后重新发送
				</view>
				<!-- <text @touchmove.stop="" v-show="show" style="position: absolute;right: 10px;top: 22px;color: #FB007E;height: 60rpx;">/text>
				<text v-show="!show" style="position: absolute;right: 10px;top: 22px;color: #FB007E;">{{num}}后重新发送</text> -->
			</view>
		</view>
		<view class="button">
			确认更换
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				num: 60,
				show: true
			}
		},
		methods: {
			codes(){
				console.log(11)
				this.show =! this.show
				if(!this.show){
					var a = setInterval(()=>{
						this.num--
						if(this.num<0){
							clearInterval(a)
							this.show = true
							this.num = 60
						}

					},1000)
					
				}
			}
		}
	}
</script>

<style lang='scss'>
	.number{
		width: 100%;
		padding: 30rpx;
		.numberMess{
			background: #F8F8F8;
			border-radius:4px;
			width: 100%;
			display: flex;
			flex-direction: column;
			justify-content: center;
			align-items: center;
			font-size: 28rpx;
			font-weight:600;
			padding-top: 20rpx;
			input{
				border: 1px solid #E9E9E9;
				height: 80rpx;
				width: 610rpx;
				margin: 30rpx 0;
				border-radius:4px;
				border-right: none;
			}
			.codes{
				color: #FB007E;
				border: 1px solid #E9E9E9;
				text-align: center;
				border-left: none;
				width: 210rpx;
				height: 80rpx;
				margin-top: 30rpx;
				line-height: 80rpx;
			}
		}
		.button{
			height: 96rpx;
			background:linear-gradient(90deg,rgba(255,0,124,1) 0%,rgba(255,117,126,1) 100%);
			border-radius: 24px;
			text-align: center;
			line-height: 96rpx;
			color: #FFFFFF;
			margin-top: 60rpx;
		}
	}
</style>
