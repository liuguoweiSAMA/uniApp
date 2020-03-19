<template>
    <view class="content">
		<view class="page-section swiper">
			<!-- <view> -->
				<input type="text" placeholder="请输入您的关键字" class="search">
			<!-- </view> -->
			
			<view class="page-section-spacing">
				<swiper class="swiper" :indicator-dots="indicatorDots" :autoplay="autoplay" :interval="interval" :duration="duration">
					<swiper-item>
						<image class="swiper-image" src="../../static/img/tab1.jpg" style="width: 100%;"></image>
					</swiper-item>
					<swiper-item>
						<image class="swiper-image" src="../../static/img/tab2.jpg" style="width: 100%;"></image>
					</swiper-item>
					<swiper-item>
						<image  class="swiper-image"src="../../static/img/tab1.jpg" style="width: 100%;"></image>
					</swiper-item>
				</swiper>
			</view>
		</view>
		1
    </view>
</template>
<style lang='scss'>
	*{
		margin: 0;
		padding:  0 0;
	}
	.content{
		padding: 0 14.4px;
	}
	.swiper-image{  
	     width:100%;  
		 border-radius: 10px;
	     /* height:300upx; */
	 }
	 .search{
		 /* border-image:linear-gradient(90deg, rgba(251,0,126,1), rgba(253,109,126,1)) 1 1; */
		background:rgba(255,255,255,1);
		border-radius:20px;
		margin-bottom: 15px;
		border:1px solid #FB007E; 
		font-size: 12rpx;
		height: 30px;
		padding-left: 20px;
		margin-top: 19.2px;
	 }
	.ser-input{
		border: 1px solid pink;
		border-radius: 25px;
		font-size: 10px;
	}
</style>
<script>
    import {
        mapState
    } from 'vuex'

    export default {
		data(){
		  return {
			  indicatorDots: true,
			  autoplay: true,
			  interval: 2000,
			  duration: 500
		  }
		},
        computed: mapState(['forcedLogin', 'hasLogin', 'userName']),
		methods:{
			onNavigationBarSearchInputClicked: async function(e) {
				this.$api.msg('点击了搜索框');
			},
		}
        // onLoad() {
       //      if (!this.hasLogin) {
       //          uni.showModal({
       //              title: '登录',
       //              content: '您未登录，需要登录后才能继续',
       //              /**
       //               * 如果需要强制登录，不显示取消按钮
       //               */
       //              showCancel: !this.forcedLogin,
       //              success: (res) => {
       //                  if (res.confirm) {
							// /**
							//  * 如果需要强制登录，使用reLaunch方式
							//  */
       //                      if (this.forcedLogin) {
       //                          uni.reLaunch({
       //                              url: '../login/login'
       //                          });
       //                      } else {
       //                          uni.navigateTo({
       //                              url: '../login/login'
       //                          });
       //                      }
       //                  }
       //              }
       //          });
       //      }
        // }
    }
</script>

<style>
    .hello {
        display: flex;
        flex: 1;
        flex-direction: column;
    }

    .title {
        color: #8f8f94;
        margin-top: 50upx;
    }

    .ul {
        font-size: 30upx;
        color: #8f8f94;
        margin-top: 50upx;
    }

    .ul>view {
        line-height: 50upx;
    }
</style>
