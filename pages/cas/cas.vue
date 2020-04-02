<template>
	<view class="cas">
		<view class="titTab">
			<text @click="tab1(1)" style="margin-left: 70rpx;" :class="{active: isActive == 1}">
				全部
			</text>
			<text @click="tab1(2)" :class="{active: isActive == 2}">
				未提取
			</text>
			<text @click="tab1(3)" style="margin-right: 70rpx;" :class="{active: isActive == 3}">
				已提取
			</text>
		</view>
		<view class="faherShelves">
			<view class="shelves">
				<table></table>
				<view></view>
				<view class="cabinet" style="">
					<br>
					<view class="productId" style="">
							<image src="../../static/img/product2.png" style="width: 150rpx;height: 150rpx;" mode=""></image>
						    <view style="font-size: 20rpx;color: #333333;margin-left: 6rpx;">长草颜团子</view>
							<radio-group @click="radioChange" >
								<radio color="#fc007c" :checked="checkedRadio"   class="radio"/>
							</radio-group>
					</view>
				</view>
				<image src="../../static/img/bottom.png" style="width: 100%;height: 34rpx;" mode=""></image>
			</view>
		</view>
		<view class="extract" v-if="buy">
			<radio-group @click="radioChanges" style="margin-left: 34rpx;">
				<radio color="#fc007c" :checked="buyRadio" class="radio"/>
			</radio-group>
			<text class="checkAll">
				全选
			</text>
			<text class="Pinkage">
				（试运营期间2个即可免邮）
			</text>
			<button type="default">
				提&nbsp;取
			</button>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				isActive: 1,
				buy: false,
				checkedRadio: false,
				buyRadio: false
			}
		},
		methods: {
			tab1(val){
				this.isActive = val
			},
			radioChange(evt){
				this.checkedRadio = !this.checkedRadio
				this.buy = !this.buy
			},
			radioChanges(){
				this.buyRadio = !this.buyRadio
			}	
		},
		onShow() {
			uni.setTabBarItem({
				index: 0,
				text: '首页',
				"iconPath": "static/img/hidden_index2.png",
				"selectedIconPath": "static/img/hidden_index1.png"
			})
			uni.setTabBarItem({
			  index: 1,
			  text: '娃柜',
			 "iconPath": "static/img/hidden_case1.png",
			  selectedIconPath: 'static/img/hidden_case1.png'
			})
			uni.setTabBarItem({
			  index: 2,
			  text: '我的',
			 "iconPath": "static/img/hidden_user2.png",
			  selectedIconPath: 'static/img/hidden_user2.png'
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
	*{
		margin: 0;
		padding: 0;
	}
	body,html{
		width: 100%;
		height: 100%;
		margin: 0;
		padding: 0;
		
	}
	.cas{
		/* background: url('') no-repeat; */
		/* background: red; */
		background:linear-gradient(180deg,rgba(193,0,228,1) 0%,rgba(96,0,253,1) 57%,rgba(46,0,196,1) 100%);
		/* background: url(../../static/img/showBg.png); */
		background-size: cover;
		padding:0 26rpx;
		width: 100%;
		/* height: 100%; */
		.extract{
			display: flex;
			align-items: center;
			/* margin-top: 48rpx; */
			.checkAll{
				font-size: 28rpx;
				color: #FFFFFF;
				/* margin-left: 20rpx; */
			}
			.Pinkage{
				font-size: 20rpx;
				color: #F8F8F8;
				font-weight:400;
			}
			button{
				width: 280rpx;
				height: 96rpx;
				border-radius:24px;
				color: #FFFFFF;
				font-size: 30rpx;
				line-height: 96rpx;
				background:linear-gradient(90deg,rgba(255,0,124,1) 0%,rgba(255,117,126,1) 100%);
			}
		}
		.titTab{
			width: calc(100% + 52rpx);
			margin-left: -26rpx;
			height: 128rpx;
			background: url("https://cdn.lljgame.com/wechat_carnival%2FshowCase_title.png") no-repeat;
			background-size: cover;
			font-size: 28rpx;
			color: #FFFFFF;
			line-height: 80rpx;
			display: flex;
			justify-content: space-evenly;
			font-weight:400;
			/* padding: 0 -26rpx; */
			 /* position:absolute; */
			 .active{
				 height: 70rpx;
				 color:#F8F8F8;
				 font-weight:600;
				 border-bottom:4rpx solid #FFFFFF;
			 }
		}
		.faherShelves{
			
			width: 100%;
			height: calc(100% - 264rpx) ;
			/* margin-top: 20rpx; */
			.shelves{
				 background: url("https://cdn.lljgame.com/wechat_carnival%2FshowCase_bg.png") 0 -55rpx no-repeat;
				 background-size: cover;
				 width: 100%;	
				 height: 100%;
				 .cabinet{
					 display: flex;
					 flex-direction: row; 
					 flex-wrap: wrap ;
					 margin-left: 20rpx;
					 margin-top: 20rpx;
					 .productId{
						 width: 150rpx;
						 height: 206rpx;
						 border-radius:10px;
						 background: white;
						 margin-left: 9rpx;
						 margin-right: 8rpx;
						 margin-top: 20rpx;
						 position: relative;
					 }
					 .radio .uni-radio-input.uni-radio-input-checked{
						 border: none !important;
					 }
					 .radio{
						 width: 36rpx;
						 height: 36rpx;
						 position: absolute;
						 left: 10rpx;
						 top: 0rpx;
					 }
				 }
				 /* .uni-radio-input uni-radio-input-checked{ */
					 /* border-color:red !important; */
					 /* background-color:red !important; */
				 /* } */
				 /* border: 10px solid white; */
				 /* background: red; */
			}
		}
	}
</style>
