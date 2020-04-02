<template>
	<view class="site">
		<view style="position: relative;width: 100%;height: 230rpx;"  >
			<view class="card" :class="{'active' : tabIndex == true}"  @touchmove="handletouchmove" @touchstart="handletouchstart" @touchend="handletouchend">
				<view class="up">
					<view class="name">
						奶瓶 176xxxx6735
					</view>
					<view class="address">
						北京市朝阳区星源公寓2505
					</view>
				</view>
				<view class="down">
					默认地址
				</view>
			</view>
			<view class="delete">
				<image @click="deleteIcon" src="../../static/img/delete.png" mode=""></image>
			</view>
		</view>
		<view class="button">
			添加地址
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				flag: 0,
				text: '',
				lastX: 0,
				lastY: 0,
				tabIndex: false
			}
		},
		methods: {
			deleteIcon(){
				uni.showModal({
				    title: '',
				    content: '是否删除地址信息',
					// mask: true,
				    success: function (res) {
				        if (res.confirm) {
				            console.log('用户点击确定');
				        } else if (res.cancel) {
				            console.log('用户点击取消');
				        }
				    }
				});
			},
			handletouchmove: function(event) {
				// console.log(event)
				if (this.flag !== 0) {
					return;
				}
				let currentX = event.touches[0].pageX;
				let currentY = event.touches[0].pageY;
				let tx = currentX - this.lastX;
				let ty = currentY - this.lastY;
				let text = '';
				this.mindex = -1;
				//左右方向滑动
				if (Math.abs(tx) > Math.abs(ty)) {
					if (tx < 0) {
						text = '向左滑动';
						this.flag = 1;
						this.tabIndex = true
						// this.item.X = 120
						console.log('向左')
					//	this.getList();  //调用列表的方法
					} else if (tx > 0) {
						text = '向右滑动';
						this.tabIndex = false
						this.flag = 2;
					}
				}
				//上下方向滑动
				else {
					if (ty < 0) {
						text = '向上滑动';
						this.flag = 3;
					//	this.getList();  //调用列表的方法
					} else if (ty > 0) {
						text = '向下滑动';
						this.flag = 4;
					}
				}
	
				//将当前坐标进行保存以进行下一次计算
				this.lastX = currentX;
				this.lastY = currentY;
				this.text = text;
			},
			handletouchstart: function(event) {
				// console.log(event)
				this.lastX = event.touches[0].pageX;
				this.lastY = event.touches[0].pageY;
			},
			handletouchend: function(event) {
				this.flag = 0;
			},
		}
	}
</script>

<style lang='scss'>
	.site{
		width: 100%;
		background: #F8F8F8;
		padding: 30rpx;
		
		.delete{
			width: 120rpx;
			height: 230rpx;
			background: #E9E9E9;
			position: absolute;
			right: 0;
			top: 0;
			z-index: 8;
			image{
				width: 36rpx;
				height: 36rpx;
				position: absolute;
				right: 43rpx;
				top: 98rpx;
			}
		}
	  .card{
		width: 100%;
		height: 230rpx;
		background: white;
		transform: translateX(0rpx);
		transition: all .2s ease-in 0ms;
		/* padding: 0rpx 40rpx; */
		position: absolute;
		left: 0;
		top: 0;
		z-index: 10;
		.up{
			height: 142rpx;
			border-bottom: 2rpx solid #E9E9E9;
			.name{
				color: #000000;
				font-size: 28rpx;
				font-weight:600;
				padding: 30rpx 40rpx;
				padding-bottom: 22rpx;
			}
			.address{
				color: #333333;
				font-size: 24rpx;
				padding-left: 40rpx;
			}
		}
		.down{
		  color: #000000;
		  font-size: 24rpx;
		  line-height: 80rpx;
		  text-indent: 40rpx;
		}
	  }
	  .button{
		  background:linear-gradient(90deg,rgba(255,0,124,1) 0%,rgba(255,117,126,1) 100%);
		  height: 96rpx;
		  border-radius:24px;
		  line-height: 96rpx;
		  text-align: center;
		  font-size: 28rpx;
		  color: #FFFFFF;
		  margin-top: 60rpx;
	  }
	  .active{
		  transform: translateX(-120rpx);
		  transition: all .2s ease-in 0ms;
	  }
	}
</style>
